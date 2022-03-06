推荐一个免费的元器件封装（原理图和PCB、3D）搜索、导出工具

# 1.SnapEDA  WIN桌面版

官方网站：

https://www.snapeda.com/home/?company=none

![image-20220302121000524](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302121000524.png)

首先，我来简单介绍一下这个软件。

SnapEDA 是一个在线设计库和搜索引擎，用于验证、准备使用的电子元件 CAD 模型。

现在我们可以使用他的桌面版来搜索，获取设计封装。重要的一点是，目前该设计软件是完全免费的。

如果有兴趣，可以访问[**这里**](https://www.embedded.com/snapeda-launches-on-desktop-as-users-seek-bridge-with-existing-cad-tools/)来获取更多介绍。

# 2.安装

这一部分，我来向大家介绍如何在WIN上面安装该软件，请注意，目前官方资料只支持WINDOWS。

## 第一步：下载百度网盘安装包

> 链接：https://pan.baidu.com/s/1y9JUyVPrgWFR-fNDglI5mQ 
> 提取码：owj8 

## 第二步：安装两个包

安装包一个是snapEDA，另外一个是Altium的插件。如果你是使用Altium来设计硬件，可以将两个软件都安装；若不是，可以只安装snapEDA。

安装过程不再说明，自行安装即可。

### 注：如果不想要在百度网盘安装，可以参考[这里](https://www.electronics-lab.com/snapeda-desktop-app-is-now-available-for-windows/)，有下载的地址。

![image-20220302142226105](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302142226105.png)

# 3.关联Altium插件，并导出Altium封装

下面举例说明在Altium中使用该软件的方法。目前测试AD19是没有问题的，官方是建议使用AD21及以上。大家可以测试自己的版本能不能够使用。

## 第一步：查看安装环境

首先确保你已经安装了插件和snapEda软件。

## 第二步：关联插件

然后，我们进行关联插件。关联插件的方法非常简单，点击Tools，看到Altium的部分，点击connect即可。关联完成后如下图。

![image-20220302142628961](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302142628961.png)

https://support.snapeda.com/en/articles/5556182-how-to-place-parts-on-altium-using-snapeda-desktop-app

## 第三步：正常使用

在我们想导出/查询某个原件封装时，点击Search Parts，输入元器件型号，例如“USB Type C”。

![image-20220302143115481](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143115481.png)

查询到结果如下:

![image-20220302143143440](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143143440.png)

在右侧Data Available一栏，是原件封装是否存在的标识，一般存在的就是有填充，没有封装的原件，就是空白的。例如下图：

3D封装存在：

![image-20220302143723956](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143723956.png)

3D封装不存在：

![image-20220302143701049](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143701049.png)

确认已有封装，我们就可以点击，等待加载导出界面：

![image-20220302143516577](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143516577.png)

我们选择Place选项，可以直接打开AD软件，导出的封装将自动生成。

![image-20220302143617425](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143617425.png)

![image-20220302143745225](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143745225.png)

![image-20220302143833826](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143833826.png)

导出完成。

接下来看一下导出的原理图封装和PCB封装：

![image-20220302143916543](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143916543.png)

![image-20220302143924656](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143924656.png)

![image-20220302143937008](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302143937008.png)

# 4.结束语

该软件使用方便，可以作为一个封装的查询、导出工具。大家可以尝试和AD等软件配合使用，相信在大家的使用中能发挥更大的作用。
