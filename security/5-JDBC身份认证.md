* JDBC身份认证

  ```java
  @Autowired
private DataSource dataSource;
  
  @Autowired
  public void configureGlobal(AuthenticationManagerBuilder auth) throws Exception{
    auth.
        jdbcAuthentication()
            .dataSource(dataSource)
            .withDeafultSchema()
            .withUser("user").password("password").roles("USER").and()
            withUser("admin").password("password").roles("USER","ADMIN");
  }
  ```

