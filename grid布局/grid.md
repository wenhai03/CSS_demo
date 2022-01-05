#### .grid_container  
```
容器可以设置  overflow: auto;  --grid：grid  --width: 40; width: calc(var(--width) * 1vw)
// 当 width 小于 320px 时，网格容器会出现水平滚动条（因为容器显式设置了overflow: auto）
```

### grid-template-columns
```

有各种不同单位的值，比如 px、%、vw，有关键词 auto，还有网格布局中独有的单位fr

grid-template-rows: 200px auto; auto后面的高度分配剩余空间
这两个属性的值除了 auto 关键词之外，还可以接受以下 CSS 函数 和关键词
grid-template-columns: min-content max-content fit-content(10rem) minmax(10rem,1fr)


grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
grid-template-rows: repeat(2, 12rem 1fr);
这样写auto-fit自动适应父容器的width， 
repeat(2, 12rem 1fr) 2 表示重复整体(12rem 1fr)俩次


grid-template-columns 和 grid-template-rows 两属性分别在 Level 2 和 Level 3 两个规范围中新增了
subgrid 和 masonry 两个属性，可用来创建子网格和瀑布流布局。这两个属性在 CSS 网格布局中是新增的特性，非常的强大也很实用，
能帮助我们实现很多复杂的布局效果


CSS的比较函数clamp()函数，不依赖CSS媒体查询
虽然 min()、max() 和 clamp() 函数非常优秀，但直接用于grid-template-columns或grid-template-rows属性中将是无效的

grid-template-columns: min(80px, 1fr) clamp(300px, 20vw, 1fr) max(auto, 80px)  // 无效



虽然 min()、max() 和 clamp() 函数直接使用grid-template-columns和grid-template-rows（设置网格轨道尺寸的属性）无效，但他们结合 minmax(min, max) 函数中却是有效
.container { grid-template-columns: auto minmax(min-content, max(60ch, 50vw)) 1fr; grid-gap: clamp(1rem, 2vw, 24px); }


```
