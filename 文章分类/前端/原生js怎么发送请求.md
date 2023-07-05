# 原生js怎么发送请求
- 可以使用XMLHttpRequest对象或者fetch API来发送请求
    ```
    //1.创建XMLHttpRequest对象 为了兼容性，需要判断浏览器是否支持
    let xhr;
    if(window.XMLHttpRequest){
        xhr = new XMLHttpRequest();
    }else{//适用于IE5和IE6的兼容性写法
        xhr = new ActiveXObject("Microsoft.XMLHTTP");
    }
    //2.设置请求参数
    xhr.open("get","./temp/demo01.json",true);
    //3.设置回调函数
    xhr.onreadystatechange = function(){
         if(xhr.readyState == 4 && xhr.status == 200){
            alert(xhr.responseText);
        }
    }
    //4.发送请求
    xhr.send();
    ```

    ```
    fetch('https://example.com/api/data')  
    .then(response => response.json())  
    .then(data => console.log('Success:', data))  
    .catch(error => console.log('Error:', error));
    ```