# spring boot

[application.properties文档](http://docs.spring.io/spring-boot/docs/current/reference/html/common-application-properties.html)

## 配置相关注解
 * @Configuration 申明这是个配置类
 * @EnableAutoConfiguration spring 会根据引入的jar,maven 配置等信息猜测可能的配置
 * @ImportResource 可以引入xml配置
 * @ComponentScan 相当于xml中的componentscan ，指定在哪里开始扫描bean
 * @SpringBootApplication//相当于@Configuration，@EnableAutoConfiguration，@ComponentScan
 * 
 
## Banner
**banner是启动容器时的输入文字**
可以在classpath目录下增加banner.txt编辑内容作为自己的banner,
也可以使用如下配置去掉banner
```
SpringApplication app = new SpringApplication(AppConfig.class);
app.setShowBanner(false);
```
## propertites中配置random变量
```
my.secret=${random.value}
my.number=${random.int}
my.bignumber=${random.long}
my.number.less.than.ten=${random.int(10)}
my.number.in.range=${random.int[1024,65536]}
```




