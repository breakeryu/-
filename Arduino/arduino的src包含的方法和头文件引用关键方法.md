ArduinoIDE使用文件夹方式和引用头文件方法

# 1.在ArduinoIDE中怎么用文件夹形式来保存源文件和头文件呢？

首先，在Arduino的1.6.10版本之后，官方给出来了工程代码中使用文件夹形式的方法，该方法必须使用src文件夹。

给出一个工程文件夹例子：

```none
project folder
|- project.ino
|- types.h
|- demo.cpp
|- demo.h
| -src folder
   	| -sub1 folder
   	|  	| -gadget1.c
   	|  	| -gadget1.h
   	|  	| -gadget2.c
   	|  	| -gadget2.h
   	| -blarg folder
      	| -foobar.c
      	| -foobar.h
```

# 2.如何调用在src中的文件呢？

使用下列中引用形式来进行调用头文件：

- ```cpp
  #include "src/bar.h"
  ```

- ```cpp
  #include "src/sub1/gadget1.h"
  ```

# 3.参考源

https://arduino.stackexchange.com/questions/54651/arduino-ide-and-subfolders

https://github.com/arduino/Arduino/issues/5186



