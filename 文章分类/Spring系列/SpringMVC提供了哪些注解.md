# SpringMVC提供了哪些注解
常见的注解有：
    - @Controller：用于标注控制层组件，一般标记在一个类上，使用它标记的类就是一个SpringMVC的Controller对象
    - @RequestMapping：用于处理请求url映射的注解，可用于类或方法上，标记在类上表示类中的所有响应请求的方法都是以该地址作为父路径（或者说一级路径），使用在方法上表示请求的二级访问路径（如果没有在类上说明一级访问路径，那么直接就是一级访问路径）。它的属性有name-方法的注释、value-请求的url、path-请求的url（通常与value作为映射使用）、method-请求的方法类型、params-请求的参数、headers-请求的头信息、consumes-请求的内容类型、produces-请求的返回类型
    - @Resource和@Autowired：都是用于注入依赖对象的，都可以标注在字段或方法上，都可以指定依赖对象的名称，都可以省略不指定名称而自动注入。但是@Autowired是Spring的注解，@Resource是J2EE的注解，@Autowired默认按照类型装配依赖对象，@Resource默认按照名称装配依赖对象
    - @RequestParam：用于将请求参数绑定到控制器方法参数上，它的属性有value-请求参数名、required-是否必须（默认值为true）、defaultValue-默认值
    - @RequestBody：用于获得请求体的内容，直接使用得到是key=value&key=value&...这样的字符串，如果想得到json格式的字符串，需要在方法上加上@RequestBody注解，然后在参数前加上@RequestBody注解，这样就可以得到json格式的字符串，并且将其转换为pojo对象（对象的属性名必须和json对象的各个属性相对应）， 有一个属性required，默认值为true，表示请求体不能为空
    - @ResponseBody：用于将响应体的内容绑定到方法返回值上，它的作用是将controller的方法返回的对象通过适当的转换器转换为指定的格式之后，写入到response对象的body区，通常用来返回JSON数据或者是XML数据，需要注意的是，在使用此注解之后不会再走视图处理器，而是直接将数据写入到输入流中，他的属性有produces-响应的内容类型。可以直接用在Controller类上，表示Controller中的所有方法的返回值都是对象数据，还可以用在Controller类的方法上，表示返回值转换成json对象返回给客户端
    - @PathVariable：用于绑定url中的占位符，比如请求url为http://localhost:8080/user/1，那么可以在方法的参数中加上@PathVariable("id")，这样就可以将url中的id值绑定到方法的参数上，如果url中的占位符名称和方法参数名称一致，那么可以省略@PathVariable中的value属性，它的属性有value-占位符名称、required-是否必须（默认值为true）、defaultValue-默认值
    - @RequestHeader：用于将请求头信息绑定到方法参数上，它的属性有value-请求头名称、required-是否必须（默认值为true）、defaultValue-默认值，使用场景是验证token的时候，可以将token放在请求头中，然后使用@RequestHeader注解将token绑定到方法参数上，然后进行验证
    - @CookieValue：用于将cookie对应名称的值绑定到方法参数上，它的属性有value-请求头名称、required-是否必须（默认值为true）、defaultValue-默认值
    - @ModelAttribute：该@ModelAttribute的所有方法在调用之前，先执行此@ModelAttribute方法，可用于注解和方法参数中，可以把这个@ModelAttribute特性应用在BaseController当中，所有的Controller继承BaseController，即可实现在调用Controller时，即可实现在调用Controller时，先执行@ModelAttribute方法。Controller中使用@RequestAttribute有这三种情况：应用在方法上、应用在方法的参数上、应用在方法上斌给方法使用了@RequestMapping