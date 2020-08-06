* UserDetailsService

> 通过定制暴露`UserDetailsService`为Bean来定制你的身份认证
*仅当AuthenticationManagerBuilder尚未填充且AuthenticationProviderBean未定义为no时使用*

```java
  @Bean
  public SpringDataUserDetailsService springDataUserDetailsService(){
      return new SpringDataUserDetailsService();
  }
```

> 通过将`PasswordEncoder`作为Bean公开来自定义密码的编码方式,例如使用bcrypt

```java
  @Bean
  public BCryptPasswordEncoder passwordEncoder(){
    return new BCryptPasswordEncoder();
  } 
```
