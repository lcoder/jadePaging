###jade 分页模版

```javascript
var config = {
	preHTML: '预置html代码' ,	// 分页代码前的html代码（未转义）
	count: 200 ,				// 总共几条数据
	limit: 10 ,					// 每页几条数据
	offset: 100					// 从第几条数据开始读区limit条数据 ( 这个参数用来计算当前第几页 )
								// 当前第几页 var now = Math.ceil( ( offset + 1 ) / limit ) ;
} ;
```
>
```jade
// 需要paging的jade页面需要包含include jadePageing.jade文件来引用mixin
+paging( config )
```
![jade分页代码样例](http://oco9w3mgp.bkt.clouddn.com/blog_images/jadePaging.png)

生成的html代码每个a标签的href默认带有`?page=`page参数，用来跳转。