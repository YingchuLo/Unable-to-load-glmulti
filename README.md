Problem: Unable to load package glmulti 

Answer:

English version:
Before library(glmulti), you need to do:
1.	Install Java on your computer
2.	Library(rJava) in R

Still cannot load package glmulti, please check:
The version of Java and R. Both of them should be constant version, such as both are 64-bit.
Still cannot load package glmulti, here are solution for mac and Win:


1.	(For mac)
In terminal, type:
sudo ln -s $(/usr/libexec/java_home)/jre/lib/server/libjvm.dylib /usr/local/lib 

In R, type: 
library(rJava)
library(glmulti)


2.	(For Win)
In cmd, type:
R CMD javareconf

In R, type:
install.packages("rJava", type = "source")
Sys.setenv(JAVA_HOME=' user/programfile/java')    
library(rJava)
library(glmulti)

Chinese Version中文版本:
在library(glmulti)前，你必須：
1.	安裝Java 軟體在你的電腦上
2.	在r中執行Library(rJava) 

如果仍然不能library(glmulti)，請先檢查Java 和r 的版本必須一致，例如：二者皆為64-bit。 

如果仍然不能library(glmulti)，解決方法如下：


1.	 (mac版本)
在終端 , 輸入:
sudo ln -s $(/usr/libexec/java_home)/jre/lib/server/libjvm.dylib /usr/local/lib 

在 R, 輸入: 
library(rJava)
library(glmulti)


2.	(Win 版本)
在命令提示字元, 輸入:
R CMD javareconf

在r, 輸入:
install.packages("rJava", type = "source")
Sys.setenv(JAVA_HOME=' c:\\Program Files\\Jave\\jdk1.7.0_51\\jre')    
library(rJava)
library(glmulti)


Reference（參考資料）:
•	尼莫船長--稀里糊涂地解决了一个 R 中安装 rjava 的问题—知乎
•	Answer of article “Unable to load rJava on R” made by Qjgods  on overflow website


