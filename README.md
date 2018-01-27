## Setting-DNA-substitution-models-in-BEAST1


##### BEAST1软件包里面BEAUti程序图形用户界面只给出了3种最流行的DNA替换模型: TrN、HKY和

GTR。这对于标准的11种替换模型来说还有8种（JC69、TrNef、K80、F81、SYM、TIM、TVM和TVMef）需要自己想办法解决。

我在线上授课的过程中很多的学员问我这样的问题：

* 我用jModelTest2软件检测到的最优替换模型是F81,在哪里设置设个模型？

* 我用PartitionFinder软件检测到的最优替换模型是第一个基因为K80+G；第二个基因是SYM+G；第三个基因是TVM+G；..

  ...，我该如何对每个基因设置指定的模型呢？

##### 我现在把相关的设置总结如下，希望能为您提供一些有用的信息。
		
最优替换模型	  |   BEAUti里面需要选择的替换模型	    |  另外需要在 BEAUti指定的设置
---------------|----------------------------------|-------------------------------------------------------
JC69	         |   JC69	                          |  不需要额外设置
TrN	           |   TN93	                          |  不需要额外设置
TrNef	         |   TN93	                          |  碱基频率设置为 “All Equal”
K80 (K2P)	     |   HKY	                          |  碱基频率设置为 “All Equal”
F81	           |   GTR	                          |  关掉所有替换参数的“operator”
HKY	           |   HKY	                          |  不需要额外设置
SYM	           |   GTR	                          |  碱基频率设置为 “All Equal”
TIM	           |   GTR	                          |  编辑XML文件使其他的替换都和AG替换相等
TVM	           |   GTR	                          |  不勾选AG替换“operator”
TVMef	         |   GTR	                          |  不勾选AG替换“operator”并且碱基频率设置为 “All Equal”
GTR	           |   GTR	                          |  不需要额外设置
               |                                  |                                                     |
               
               
更多有关BEAST的内容可以访问：[李老师的个人QQ空间日志](https://user.qzone.qq.com/2049968646/main) 
