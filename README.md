
## 一、MergePicture 拼接图片
将n组像素大小相同的图片合成n张图片;典型的应用场景是，有n张图片，
经过m种不同的方法得到m种结果，然后需要每m种结果对应的第x（1~n）
张图片合并为一张图片，就可以使用这个程序。

## 二、如何使用

* 下载源码，解压进入目录执行命令:  
```
cd run
cmake ..
make
./MergePicture -c 8 -m 2 -n 2 -t src.txt -s merge -p ./图片组1 ./图片组2 ./图片组3 ./图片组4
```
执行完上面的命令没有报错，run目录内会有一个叫做merge
的文件夹，如果里面有8张图片，说明程序已经可以正常运行。
* 调用方法  
```
./MergePicture -c number -m number -n number -t txtName -s save_path -p path1 path2 ... pathm*n
 ```
* 参数解释  
-c 要合并图片的组数;  
-m 合并后横向包含几张图片;  
-n 合并后纵向包含几张图片;  
-t 这m\*n个目录中列出图片名字的txt文件名，每个
目录中的txt文件名字都需要相同;  
-s 指定保存路径;  
-p 指定m\*n个包含图片名称的txt文件路径;若路径数量不
够m\*n，则会用黑色图片补足。-p这个参数必须在前面的参
数之后指定，是最后一个参数。  

* 调用demo:  
```
./MergePicture -c 8 -m 2 -n 2 -t src.txt -s merge -p ./图片组1 ./图片组2 ./图片组3 ./图片组4
```

## 三、关于作者
```javascript
  var whoAmI = {
    name   : "Mannix1994",
    gitee  : "https://gitee.com/Mannix1994",
    github : "https://github.com/Mannix1994"
  }
```