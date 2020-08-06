* 配置多个HttpSecurity 

> 

```java
  @EnableWebSecurity
  public class MultiHttpSecurityConfig {
    @Bean
    public UserDetailsService userDetailsService() throws Exception {
      InMemoryUserDetailsManager manager = new InMemoryUserDetailsManager();
      manager.createUser(User.withUsername("user").password("password").roles("USER").build());
      manager.createUser(User.withUsername("admin").password("password").roles("USER","ADMIN").build());
      return manager;
    }

    @Configuration
    @Order(1)     //指定WebSecurityConfigurerAdapter应首先考虑的对象(@Order的默认值是last)
    public static class ApiWebSecurityConfigurationAdapter extends WebSecurityConfigurerAdapter {
      protected void configure(HttpSecurity http) throws Exception {
        http
          .antMatcher("/api/**")       //只适用于以/api/开头的Url
          .authorizeRequests()
            .anyRequest().hasRole("ADMIN")
            .and()
          .httpBasic();
      }
    }

    @Configuration   //若不匹配以/api/开头的实例,则匹配此实例
    public static class FormLoginWebSecurityConfigurerAdapter extends WebSecurityConfigurerAdapter {

      @Override
      protected void configure(HttpSecurity http) throws Exception {
        http
          .authorizeRequests()
            .anyRequest().authenticated()
            .and()
          .formLogin();
      }
    }
  }
```