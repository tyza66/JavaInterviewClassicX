# IOC中有哪些常见注解
- IOC中表示将当前类实例化的对象交给IOC容器来管理的注解有这四个：@Component表示组件类、@Service表示服务类、@Repository表示数据访问类、@Controller表示控制类
- @Autowired是自动装配注解，可以用在构造器参数上、可以用在成员变量上、可以用在set方法上
- @Qualifier：限定符注解，可以和@Autowired一起使用，指定注入的属性名称
- @Scope：作用域注解，可以指定Bean的作用域，如单例(singleton)或原型(prototype)
- @ImportResource：XML配置文件引入注解，可以指定需要加载的XML配置文件路径