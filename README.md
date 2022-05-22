## 创建一个新的notebook
![在这里插入图片描述](https://img-blog.csdnimg.cn/989f49c6f6e441718e303a08af566e93.png)

输入一行代码，查看效果：
![在这里插入图片描述](https://img-blog.csdnimg.cn/7da45aa3425940f59eb925fd4c390076.png)

分析历年财富500强的数据：
![在这里插入图片描述](https://img-blog.csdnimg.cn/d1c491022bb04d728a54e82a4801f092.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/1c81a13c3b1447cfa346dbb15fc46785.png)

检查数据条是否加载完成：
![在这里插入图片描述](https://img-blog.csdnimg.cn/020bfed42c1c432aaedd5f9543b4d6e7.png)

从1955到2055总共有25500条目录，然后，检查属性列的类型：
![在这里插入图片描述](https://img-blog.csdnimg.cn/f91e9f1dfb664beb9c10c5c9db8eebf8.png)

其他属性列都正常，但是对于profit属性，期望的结果是float类型，因此其可能包含非数字的值，利用正则表达式进行检查。
![在这里插入图片描述](https://img-blog.csdnimg.cn/f318d006ba9847b78de34821523aa736.png)

确实存在这样的记录，profit这一列为字符串，统计一下到底存在多少条这样的记录：
![在这里插入图片描述](https://img-blog.csdnimg.cn/fd2820e201c94161930a1141b737c9dd.png)

总体来说，利润（profit）列包含非数字的记录相对来说较少。更进一步，使用直方图显示一下按照年份的分布情况：
![在这里插入图片描述](https://img-blog.csdnimg.cn/de457ed50305404fb2d09a01af8ecaa4.png)

可见，单独年份这样的记录数都少于25条，即少于4%的比例。这在可以接受的范围内，因此删除这些记录。
再次检查数据记录的条目数：
![在这里插入图片描述](https://img-blog.csdnimg.cn/41ff604e669c4906aacb2d4ef4f2dcf2.png)
![在这里插入图片描述](https://img-blog.csdnimg.cn/160f3554277340bfb10221b8d5206986.png)

可见，上述操作已经达到清洗无效数据记录的效果。
## 使用matplotlib进行绘图
接下来，以年分组绘制平均利润和收入。首先定义变量和方法。
![在这里插入图片描述](https://img-blog.csdnimg.cn/2d09e1d39fc24230ac43f3052ee14a5c.png)

看起来像指数增长，但是1990年代初期出现急剧的下滑，对应当时经济衰退和网络泡沫。再来看看收入曲线。
![在这里插入图片描述](https://img-blog.csdnimg.cn/465c81bec7eb4fac9eeeac5eb446084d.png)

公司收入曲线并没有出现急剧下降，可能是由于财务会计的处理。对数据结果进行标准差处理。
![在这里插入图片描述](https://img-blog.csdnimg.cn/3fedfa48bd9c4759974684d2f42c8095.png)

导出：
![在这里插入图片描述](https://img-blog.csdnimg.cn/72613b5aa4bb4b64bcbe937ff853b3e0.png)
