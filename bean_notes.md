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