server:
  port: ${port:9091}

spring:
  datasource:
    driver-class-name: com.mysql.jdbc.Driver
    url: jdbc:mysql://localhost:3307/springcloud
    username: root
    password: 123456
  application:
    name: user-service
mybatis:
  type-aliases-package: com.itheima.user.pojo
eureka:
  client:
    service-url:
      # defaultZone: http://127.0.0.1:10086/eureka,http://127.0.0.1:10087/eureka
      defaultZone: http://127.0.0.1:10086/eureka
  instance:
    #更倾向使用 ip地址，而不是host名
    prefer-ip-address: true
    # ip地址
    ip-address: 127.0.0.1
    #续约间隔时间,默认30s
    lease-renewal-interval-in-seconds: 5
    # 服务失效时间，默认90s
    lease-expiration-duration-in-seconds: 5
