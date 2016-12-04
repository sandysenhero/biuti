# angular 做的一个单页面app 
这是一个电商app，模仿的sasa原生app。你可以从[sasa官网](http://www.sasa.com/)下载app观看。

里面所有数据是从原生app中抓包获取的。如何抓包请自行百度。

本app没有调用任何原生功能，你可以将代码clone，直接本地服务器环境下运行可以看本app的效果。

抓包获取的数据是存放在data文件夹下，根据不同的请求，来请求不同的文件。以模拟真实的环境。

data/banner中是首页轮播图的八张图片。  
data/class中是首页八个按钮对应的数据。  
data/details中是为数不多的几个商品的详情数据。以商品id划分。每个详情中又有三条数据，分别是商品基本信息，评论，促销信息。  如果你用浏览器查看，如果你在详情页刷新，不会有数据渲染，因为打开详情页时带有id参数，刷新则没有，而且会报错。  
data/index是首页对应的数据。  
另外提一点，data/user.json中的帐号（用户名也是本app的参与者），是唯一能登录成功的帐号，条件有限，没有实现注册功能。所有在用户操作中产生的数据都是存储在localstorage中，比如用户购物车，浏览记录，收藏功能等。不同的用户会有不同的显示。你可以在设置中退出帐号。  

app中的css是采用less预编译的。里面声明了较多的变量和规范，但是基本没用到，因为项目实施起来非常放任。  

font文件夹里面是下载的阿里巴巴的图标库。  

js文件夹里面是主要的逻辑代码，引用的外部库或框架都在lib文件夹里面。根据不同的命名可以对应是不同的页面的js。commonjs里面是一些很多页面都可以调用的方法。新手上路，写的不规范，划分也不规范，请谅解。项目的架构信息主要在mainjs里面。  

page文件夹里面是html文件，对应不同的页面或组件。

car：购物车页。  
classinfo：列表页。  
details：详情页。  
home：主页。
limit：限时特卖页。  
list：分类页。  
my：个人中心。

已知缺陷：  
1. 如果商品已被收藏，点进详情页收藏按钮应该是选中状态，由于要重新设计收藏数据的数据结构，没时间做，就没有实现。
2. 收藏和浏览记录的时间排序不对，最新浏览的记录应该在最上面。当初的想法是看能不能不用排序函数，而是根据浏览的系统时间这个默认排序和一些条件判断来实现排序，结果后面测试了一下还是不对，所以有bug，也抽不出时间来完善。
3. 详情页刷新问题上面有提到。  
4. 所有的限时特卖时间是写死了,可能你运行的时候时间已经过了。  
5. 其他的暂时没有发现。  


这个项目从一开始学习抓包，到目前这个状态，花了半个多月的时间，很多的地方是非常不完善，也有很多写法很low，请你们理解。  
学习angular不要用jq成长会快点。


