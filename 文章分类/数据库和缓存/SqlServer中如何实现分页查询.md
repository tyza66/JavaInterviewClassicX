# SqlServer中如何实现分页查询
- 方法一：三次倒序+top
- 方法二：top+自增主键
- 方法三：用row_number关键字（只有SqlServer2015以上版本才有row_number() over(order by id)函数）
- 方法四：offset / fetch next（2012版本及以上才有）
    ```
    set statistics time on;
    -- 分页查询（通用型）
    select * from student
    order by sno 
    offset ((@pageIndex-1)*@pageSize) rows
    fetch next @pageSize rows only;
    -- 分页查询第2页，每页有10条记录
    select * from student
    order by sno  
    offset 10 rows
    fetch next 10 rows only ;
    ```