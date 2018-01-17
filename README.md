# Learning-Spring-boot
Knowledge point will be recorded here
# Idea 开启Spring-boot 热部署
1、Setting -> Build,Execution,Deployment -> Complier -> 勾选Build project automatically  
2、Ctrl + shift + A 输入registry ,点击registry -> 选中compiler.automake.allow.when.app.running  
3、pom中添加依赖  
```xml
<dependency>
    <groupId>org.springframework.boot</groupId>
    <artifactId>spring-boot-devtools</artifactId>
    <optional>true</optional>
</dependency>
```
4、build标签里面添加  
```xml
<build>
    <plugins>
        <plugin>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-maven-plugin</artifactId>
            <configuration>
                <fork>true</fork>
            </configuration>
        </plugin>
    </plugins>
</build>
```
#Spring 常用注解
* `Service`: 声明此类是一个业务处理类，通常与@Transactional一起使用
* `Repository`: 声明此类是一个数据库或者其他NoSQL访问类
* `RestController`: 相当于Controller与ResponseBody
* `Component`: 声明此类是一个Spring管理的类，通常无法用于上述注解描述的Spring管理类
* `configuration`: 声明此类是一个配置类，通常与注解Bean配合使用
* `Bean`: 作用在方法上，声明该方法执行的返回结果是一个Spring容器管理的Bean，
* `PostConstruct`: 当Bean被容器初始化后，会调用PostConstruct的注解方法
* `PreDestroy`: 在容器被销毁之前，调用被@PreDestroy注解的方法
* `Qualifier`:注解在类上是给这个bean取名字，在变量前是指定该变量引用这个名字的bean
* `Autoware`: 自动装配，容器根据类型自动选择合适的bean




