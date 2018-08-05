## 介绍
微服务-SpringCloud-SpringBoot  
## 第一个应用
https://start.spring.io/  

应用任何一个框架都一样都逻辑：与应用Log4Net类似，建一个类，在构造函数中载入配置，然后就可以从配置中获得一个对象，接下来就是包装api。只不过这里是建一个应用类，在main函数中run，构造了运行时。

import project from external model  

## 配置application.properties/application.yml
server.port=8080  
server.context-path=/xxx  

server:  
  port: 8080  
  context-path: /xxx  
cupSize: B  
@Value("${cupSize}")  属性配置  
private String cupSize;
配置中使用配置  
@Compent  分组配置  
@ConfigurationProperties(prefix = "girl")  
@AutoWired  

application.yml/application-dev.yml/application-prd.yml  
spring:  多环境配置  
  profiles:  
    active: dev  

spring:  
  datasource:  
    url:  
    username:  
    password:  
    driver-class-name:  

## Controller
@Controller  需要模板  
@RestController  @ResponseBody  
@RequestMapping(value={""}, method=RequestMethod.POST)  
@PathVariable("id") int id  /{id}
@RequestParam("id") int id  /?id=100  @RequestParam(Value="id", required=false, defaultValue="0")  
@GetMapping  
@PostMapping  

## 数据库
Spring-Data-Jpa  
POST /cats  @PostMapping  save()  
DELETE /cat/{id}  @DeleteMapping  delete()  
PUT /cat/{id}  @PutMapping  save()  
GET /cat{id}  @GetMapping  fineOne()  
GET /cats  @GetMapping  findAll()  

spring:
  datasource:
    url: jdbc:mysql://127.0.0.1:3306/exp  
    username: root  
    password:    
    driver-class-name: com.mysql.jdbc.Driver  
  jpa:  
    hibernate:  
      ddl-auto: update  
    show-sql: true  

<dependency>  
	<groupId>org.springframework.boot</groupId>  
	<artifactId>spring-boot-starter-data-jpa</artifactId>  
</dependency>  
<dependency>  
	<groupId>mysql</groupId>  
	<artifactId>mysql-connector-java</artifactId>  
</dependency>  

@Entity  
@Id  
@GeneratedValue  

extends JpaRepository<Cat, Integer>  


## 事务/交易
@Service  
@AutoWired  
@Transactional  


