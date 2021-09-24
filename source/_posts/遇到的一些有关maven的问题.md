---
title: 遇到的一些有关maven的问题
toc: true
date: 2021-09-24 19:41:19
tags:
categories:
---

# 1.xml错误

右键文件夹➡️添加框架的支持➡️maven

不行？ pom.xml添加一个groupID

不行？偏好设置➡️构建，执行，部署➡️Compiler➡️Java Compiler➡️

![image-20201201151904235](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201201151904235.png?lastModify=1632483689)

如上图，project bytecode version修改成5试试，应该就好了，不行的话改成别的数字（反正要满足等于自己的JDK）



第二天搞javax.mail时又出错了，改成这样倒是可以了⬇️

![image-20201201201634418](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201201201634418.png?lastModify=1632483689)

# 2.javax.mail错误

需要去oracle下载包

然后我把pom.xml的javax.mail版本号改为与新下载的一样，但是构建后还是无法找到

然后才发现右边弹出一个蓝色正方形M,点击后就可以了。![image-20201201205050052](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201201205050052.png?lastModify=1632483689)

不过出现了这个![image-20201201201739631](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201201201739631.png?lastModify=1632483689)

第二天，我下载完jdk-7u80(即jdk7的某一具体版本)，打开文件-项目结构，添加下载好的1.7![image-20201202180610843](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201202180610843.png?lastModify=1632483689)



然后在这里改成这样（第一行11改成1.7）![image-20201202180441501](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201202180441501.png?lastModify=1632483689)



这里也改成7

![image-20201202180425456](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201202180425456.png?lastModify=1632483689)

最后再是这里![image-20201202181612059](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201202181612059.png?lastModify=1632483689)

和这里![image-20201202181642839](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201202181642839.png?lastModify=1632483689)

然后按下![image-20201201205050052](file:///Users/bzm/Library/Application%20Support/typora-user-images/image-20201201205050052.png?lastModify=1632483689)运行，ok！
