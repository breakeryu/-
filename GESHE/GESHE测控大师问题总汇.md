GESHE测控大师问题总汇

# 一.设备脚本

## 1.怎么用按键设计串口串口设备打开关闭？

## 实现步骤解析

步骤：先命名控件，再生成事件。

首先，先定义控件，更改控件名称，这里我定义button_openSerial的按键控件。

![image-20220302171454836](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302171454836.png)

接着点击事件，双击Click事件，创建一个事件。

![image-20220302171549016](C:\Users\Hasee\AppData\Roaming\Typora\typora-user-images\image-20220302171549016.png)

接下来，编写脚本。

这里用到的几个控件帮助：获取画面控件的方法以及修改控件属性；项目上下文和设备会话。

1.获取串口状态：Context.GetDeviceSession("串口").State可以检测串口是否打开，打开为1

2.关闭/开启串口：

- 打开设备  `Context.GetDeviceSession("串口").Open();`

- 关闭设备  `Context.GetDeviceSession("串口").Open();`

3.获取画面控件：

获取画面创建的按键控件：

`Button btn = Context.GetSchemaElement<Button>(sender,"button_openSerial");`

接下来改变按键控件的显示文本信息：

` btn.Content = Context.GetDeviceSession("串口").State ? "关闭串口" : "打开串口";`

## 完整实现脚本

>  // 串口打开按键回调函数
>    **public** void **button_openSerial_Click**(Object sender, System.Windows.RoutedEventArgs e)
>    {
>
> **if** (Context.**GetDeviceSession**("串口").State)
>  {
>    Context.**GetDeviceSession**("串口").**Close**();
>  }
>  **else**
>  {
>    **if** (Context.**ShowDeviceDialog**("串口"))
>    {
>      Context.**GetDeviceSession**("串口").**Open**();
>    }
>  }
>
>  Button btn = Context.GetSchemaElement<Button>(sender,"button_openSerial");
>  btn.Content = Context.**GetDeviceSession**("串口").State ? "关闭串口" : "打开串口";
>
>    }

