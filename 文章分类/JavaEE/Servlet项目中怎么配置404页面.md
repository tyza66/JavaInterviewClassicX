# Servlet项目中怎么配置404页面
- 可以在Web内容目录（如WebContent、webapps）下创建一个新的HTML页面，命名为error.html或error.jsp，用于作为404页面
- 还可以在web.xml中配置<error-page>标签
    ```
    <error-page>  
    <error-code>404</error-code>  
    <location>/error/404.html</location>  
    </error-page>
    ```