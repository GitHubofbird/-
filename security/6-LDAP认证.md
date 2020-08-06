* LDAP认证

  ```java
  @Autowired
private DataSource dataSource; 
  
  @Autowired public void configureGlobal（AuthenticationManagerBuilder auth）throws Exception{
    auth
      .ldapAuthentication（）.
        userDnPatterns（ “ uid = {0}，ou = people”）.
        groupSearchBase（ “ ou = groups”）; 
  }
  ```
