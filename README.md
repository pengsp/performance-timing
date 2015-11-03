# performance-timing

利用HTML5中的[navigation timing API](http://www.w3.org/TR/navigation-timing/)进行前端性能数据采集

### 浏览器兼容性

请参考：[http://caniuse.com/#feat=nav-timing](http://caniuse.com/#feat=nav-timing)

### 依赖

目前依赖[jQuery](http://jquery.com/)，如果不希望依赖jQuery可以自己去实现函数`$.param`和`$.extend`

### 使用示例

```js
    //支持 AMD 和 CMD，下面代码使用的是全局变量的方式
    Performance.start({
        url: "http://www.xxx.com/a.gif", //后端收集数据的URL，必填
        rate: 0.2, //抽样比例，默认是10%抽样
        data: { //额外需要记录的数据，可以不需要
            ext_domain: "www.xxx.com", //域名，默认是document.domain
            ext_path: "_wap_index" //页面，默认是encodeURIComponent(location.pathname.toLowerCase().replace(/\//g, "_"));
        }
    });
```
