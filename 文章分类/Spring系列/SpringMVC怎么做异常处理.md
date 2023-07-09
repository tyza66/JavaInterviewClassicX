# SpringMVC怎么做异常处理
- 首先可以在Spring的配置文件中声明异常处理相关的Bean，来指定异常的默认跳转页面
    ```
    <!-- 统一的异常处理跳转到统一的页面处理 -->
    <bean class="org.springframework.web.servlet.handler.SimpleMappingExceptionResolver">
        <!--    出现异常跳转到error页面    -->
        <property name="defaultErrorView" value="error"/>
        <!--    提交异常获取异常信息    -->
        <property name="exceptionAttribute" value="ex"/>
        <property name="exceptionMappings">
            <props>
                <prop key="java.long.Throwable">error.html</prop>
                <!--                不同异常调换到不同页面-->
            </props>
        </property>
    </bean>
    ```

- 还可以直接在Controller中使用@ExceptionHandler指定某种异常的默认处理策略（可以处理自定义异常）
- 还可以在控制器增强类（@ControllerAdvice修饰的类）中，定义全局的异常处理策略（如果想返回JSON对象不要忘记@ResponseBody注解）