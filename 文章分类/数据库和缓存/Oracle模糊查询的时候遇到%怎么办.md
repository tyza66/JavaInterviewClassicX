# Oracle模糊查询中遇到%怎么办
- 使用escape关键字定义一个转义符，对%进行转义
    ```
    select * from emp where ename like 'giao/%%' escape '/'
    ```