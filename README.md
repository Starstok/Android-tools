## 使用说明如下：

#### 1）dex文件工具使用
Linux / Mac下使用,必须安装java

把apk或者jar包里的classes.dex文件放在work目录下

反编译的dex文件在work/out/classes目录

回编译生成的文件classes_new.dex

使用脚本命令：
> sh baksmali.sh 

使用脚本命令：
> sh smali.sh 

反编译命令：
> java -jar tools/bin/baksmali.jar work/classes.dex -o work/out/classes/

回编译命令：
> java -jar tools/bin/smali.jar work/out/classes/ -o work/classes_new.dex


#### 2）apk文件工具使用
Apktool.jar的用法也是一样

把需要反编译的apk文件放在work目录，生成在根目录

使用脚本命令：
> sh apktool.sh

反编译命令：
> java -jar bin/apktool.jar d xxx.apk

回编译命令：
> java -jar bin/apktool.jar b xxx

注明：xxx是apk的名字


#### 3）apk签名工具使用
signapk.jar使用：

把需要签名的apk文件，改名为old.apk放在work目录下，生成new_signed.apk

使用脚本命令：
> sh signapk.sh

签名命令：
> java -jar bin/signapk.jar platform.x509.pem platform.pk8 old.apk new_signed.apk


#### Apktool网站
https://ibotpeaches.github.io/Apktool/

Apktool官方文档
https://ibotpeaches.github.io/Apktool/install/

