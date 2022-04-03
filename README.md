### 分页器

### 下载



#### 使用

1. 引入样式文件`<link rel="stylesheet" href="./paginationself.css">`

2. 引入js代码文件` <script src="./paginationself.js"></script>`

3. js代码添加

   ```javascript
   var fy = document.getElementById("fy");//父容器,负责存储分页器
   paginationself(fy, {});
   ```

#### 具体参数

paginationself(fatherDom,options,callback)

1. fatherDom:生成器生成的父容器
2. options对象:参数配置
   - pageInfo对象
     - pagenum:当前页
     - pagesize:一页显示的数据条数
     - totalsize:数据总个数
     - least:当总页数低于least的时候页码全部显示
     - size:一次显示多少页码
   - textInfo对象:设置显示文字
     - first:
     - prev:
     - next:
     - last
3. callback:当用户单击页数的时候触发回调函数,会返回一个用户单击后的页码

#### 参考示例

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="./paginationself.css">
    <style>
        #fy {
            width: 100%;
            height: 50px;
            border: 1px solid #e5e5e5;
            margin: 20px auto;
            display: flex;
            justify-content: center;
            align-items: center;
        }
    </style>
</head>
<body>
    <div id="fy">
    </div>
    <script src="./paginationself.js"></script>
    <script>
        // 使用
        var fy = document.getElementById("fy");
        paginationself(fy, {}, (nowpage) => {
            //此为回调函数,可省略~
        });
        //等同于
        // paginationself(fy,{});
    </script>
</body>
</html>
```

### 效果图

#### 图1
![](https://dreamos.oss-cn-beijing.aliyuncs.com/gitblog/20220403154238.png)
#### 图2
![](https://dreamos.oss-cn-beijing.aliyuncs.com/gitblog/20220403154403.png)
#### 图3

![](https://dreamos.oss-cn-beijing.aliyuncs.com/gitblog/20220403154454.png)

#### 图4
![](https://dreamos.oss-cn-beijing.aliyuncs.com/gitblog/20220403154318.png)
