### bean加载顺序
* ApplicationContextAware的setApplicationContext 方法
* BeanPostProcessor的postProcessBeforeInitialization方法
* 注解了 @PostConstruct 的方法
* InitializingBean的afterPropertiesSet方法
* bean的指定的初始化方法： init-method
* BeanPostProcessor的postProcessAftrInitialization方法

### @PostConstruct
java注解 Constructor(构造方法) -> @Autowired(依赖注入) -> @PostConstruct -> init

参考[链接](https://blog.csdn.net/Asa_Prince/article/details/118342171)


* 构造函数
* 依赖的bean被初始化完成，并注入到了当前bean 中 （循环依赖时，稍微不同）
* ApplicationContextAware 接口的 setApplicationContext 方法
* @PostConstruct 注解的方法
* InitializingBean 接口的 afterPropertiesSet 方法
* 等所有 bean 初始化完成后，ApplicationListener<ApplicationEvent> 接口的 onApplicationEvent 方法接收 ContextRefreshedEvent 事件。

[参考链接](https://www.letianbiji.com/spring/sca-spring-postcontruct-initializingbean-run-order.html)

