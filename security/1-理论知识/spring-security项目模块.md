### 核心 spring-security-core.jar

 包含身份验证和访问控制类和接口,远程支持和基本配置API. 使用Spring-security的任何应用程序都需要此模块. 支持独立的应用程序,远程客户端,方法(服务层)安全性和JDBC用户配置. 包含包:
  + org.springframework.security.core
  + org.springframework.security.access
  + org.springframework.security.authentication
  + org.springframework.security.provisioning

### 远程处理 spring-security-remoting.jar

 提供与Spring Remoting的集成. 除非你非要编写使用Spring Remoting的远程客户端,否则不需要这样做

主要包:

  + org.springframework.security.remoting

### 网页 spring-security-web.jar

 包含过滤器和相关的Web安全基础结构代码.任何与Servlet API依赖的东西. 如果你需要Spring Security Web认证服务和基于URL的访问控制,则需要它.

主要包:

  + org.springframework.security.web

### 配置 spring-security-config.jar

 包含安全名称空间解析代码和Java配置代码.如果你使用Spring Security XML名称空间精选配置或Spring Security 的java配置支持,则需要它.

主要包是:

  + org.springframework.security.config

### LDAP spring-security-ldap.jar

 LDAP身份验证和配置代码.如果你需要使用LDAP用户条目,则为必须.

顶级软件包:

  + org.springframework.security.ldap

### ACL spring-security-acl.jar

 专门的域对象ACL实现,用于将安全性应用于应用程序中的特定域对象实例.

顶级软件包:

  + org.springframework.security.acls

### CAS spring-security-cas.jar

 Spring Security的CAS客户端集成.如果想通过CAS单点登录服务器使用Spring Security Web认证.

顶级软件包:

  + org.springframework.security.cas

### OpenID spring-security-openid.jar

  OpenID web身份验证支持. 用于根据外部OpenID服务器对用户精选身份验证

顶级软件包;

  + org.springframework.security.openid

### Test spring-security-test.jar

 支持Spring security 进行测试