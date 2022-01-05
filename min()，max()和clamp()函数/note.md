### min()函数包含一个或多个逗号分隔的计算（表达式），然后以最小的表达式的值作为返回值
```
width: min(50vw, 500px)
50vw根据浏览器视窗的宽度，比如在1200px时候  width:min(600px, 500px) 此时width: 500px
当浏览器视窗在760px,width:min(380px, 500px) 此时width: 380px

.container { width: 1024px; max-width: 100%; }
===
.container { width: min(1024px, 100%) }


如果使用了clamp()函数的话，相当于使用了min()和max()函数

```
