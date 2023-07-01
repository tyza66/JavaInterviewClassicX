# Spring Boot的自动装配原理
- @Import注解+@Configuration注解+Spring Spi
- 自动装配由各自的stater实现，使用@Configuration+@Bean定义配置类，放到了META-INF/spring.factories下
- 使用Spring Spi扫描META-INF/spring.factories下的配置类，将配置类导入到容器中
- 使用@Import注解导入自动配置类