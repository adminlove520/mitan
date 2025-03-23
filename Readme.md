## 密探 -- 渗透测试工具 v1.2.2 版

### 1.缘起

  对于学习网络安全的小白来说，在渗透实战过程中容易没有方向，密探借鉴FindSomeThing、SuperSearchPlus ，御剑文件扫描、dirsearch、JSFinder、fofaviewer等工具，开发这款“密探”渗透测试工具，希望能够为大家提供帮助，并向上述工具的开发者致敬！！

###  2.功能介绍

  密探-主要包含资产信息收集，IP端口查询，备案信息查询，子域名爆破（支持多级递归），搜索引擎语法自动生成（**FOFA,Hunter,Quake,ZoomEye,google,github**），资产测绘（**FOFA，hunter，Quake，ZoomEye , 零零信安** 的查询及结果导出），指纹识别、敏感信息（**暴露接口并可以自动探测未授权**），文件扫描（包含**目录，备份文件，spring信息泄漏，自定义字典**等）、渗透技能路线备忘录，常用网络安全网站导航等功能。

  

​      **github下载地址：https://github.com/kkbo8005/mitan/releases**   

​     **不太会用的师傅可以先了解了解操作 【密探B站视频】** https://space.bilibili.com/552795114 



​       **本工具仅供安全测试人员运用于授权测试, 禁止用于未授权测试, 违者责任自负。作者不对您使用该工具所产生的任何后果负任何法律责任。**  

​       **本工具在扫描模块使用多线程，在测试过程中根据目标的实际情况进行调整，切勿进行大线程低延时的大规模快速扫描，以免对目标服务造成不利影响。**

​       **特别注意，各位师傅使用本工具请从github下载，从其他渠道下载工具，若被下毒与本作者无关，未经作者允许，严禁对本工具进行编译，二开 从事非法活动或商业行为**

### 3.更新日志

| 2025.3.23 | 优化了代理池功能、增加了Sessionkey三要素的加解密功能、优化了资产测绘模块的零零信安结果的右键功能，优化了资产测绘界面的常用语法显示，可以通过双击或则右键功能添加到搜索框中完成对应引擎的语法输入。 |
| --------- | ------------------------------------------------------------ |
| 2025.1.5  | 修复了信息查询的备案信息查询，子域名查询接口失效的问题，升级了ZoomEye最新v2版API接口，新增了零零信安的信息系统，域名，移动应用3个资产测绘查询接口，并完善响应的批量导出功能。优化导出界面默认全选所有查询结果。优化了一些使用过程中的其他bug. |
| 2024.11.3 | 接口扫描从敏感信息里面拆分出来成为独立模块，敏感信息对抓取的数据进行分tab展示，并可以合并导出，增加工具箱大模块（swagger接口抓取功能，其他功能后续增加），通过swagger抓取接口后联动接口扫描模块进行未授权接口扫描。优化目录扫描的WAF识别功能，若遇到WAF相关关键字，自动放弃扫描，提高扫描效率，备案信息查询修改为站长工具，爱站的聚合查询。支持填写cookie进行查询，优化子域名cookie查询并支持分页抓取。基础信息增加飞鸟平台的分支机构，对外投资，APP，小程序的查询（需要填写cookie token) |
| 2024.9.28 | 增加批量信息、权重模块查询及导出模块（线程不要太大)，其他信息收集模块的表格列表增加选择列，可以自定义行进行功能联动。修复主题信息查询中包含（）括号不能查询的bug，文件扫描长度增加长度区间或则*的通配符判断，端口扫描字典配置到dict目录里面的端口port配置文件便于修改，icon hash 优化编辑复制功能。优化部分使用中遇到的其他bug. 基本信息模块的备案信息右键菜单增加了“复制全表”功能。 |
| 2024.8.30 | 资产测绘增加语法批量查询，备案信息自动生成批量查询语法，资产测绘导出增加去重算法,资产测绘联动指纹识别、敏感信息、文件扫描的去重，增加了fofa,quake的备案号显示，增加Iconhash 本地文件计算，文件扫描、敏感信息（接口）扫描增加自定义header头，增加端口扫描功能（未实现端口指纹识别）并实现联动，优化多处多线程处理流程。优化接口扫描的结果json过大影响列表高度，改为弹窗显示json数据, 优化了各个模块的长度排序。 |
| 2024.8.5  | 增加选择3套皮肤的功能，增加了资产测绘的icon hash计算，增加了jeecg,ruoyi,springblade,apipath的未授权路径扫描字典，增加渗透备忘的编辑功能，可以自定义备忘录的目录及对markdown文档的编辑和浏览，解决基本信息查询单位名称卡死的bug，敏感信息披露接口查询增加了对delete等危险接口的过滤功能，优化了敏感信息js接口抓取。 |
| 2024.7.10 | 所有多线程扫码模块增加线程的暂停，恢复功能，优化停止任务的退出机制，子域名爆破的title乱码问题，指纹识别模块增加高亮显示，子域名爆破泛解析和任务量不匹配的bug，信息查询和资产测绘能改有下拉选择框记录历史记录(右键可清除历史记录），资产测绘自定义每次最大的查询数量，修复了一些其他使用中发现的bug。 |
| 2024.6.18 | 主要增加了子域名爆破功能，子域名爆破可设置递归层级，资产测绘代理功能分拆出来独立设置，为了满足大量的查询需求，资产测绘每个测绘引擎可单独为每个测绘引擎设置每页数据条数（Zoomeye不支持)，然后是各个模块的序号列排序bug， 资产测绘增加copy标题和按标题查询，修复了指纹识别标题乱码的bug，修复子域名爆破的时候调整无法获取到title,增加了对跳转的页面获取title，同步修复子域名title乱码的问题 |
| 2024.5.31 | 资产测绘增加了对ZoomEye的支持，优化了导出资产的报错的bug, 信息查询增加了单位名称/IP的查询，在备案，IP反查等列表增加了“信息查询”等右键菜单。子域名增加rapiddns,alienvault聚合查询结果。修复了资产测绘联动到指纹识别，敏感信息，文件扫描等没带端口的bug。优化显示界面自适应问题。搜索语法增加一些网上搜集的搜索语法。 |
| 2024.5.19 | 优化指纹识别的增加任务文件中包含多个空行导致的线程假死bug，增加状态码过滤，增加指纹识别去重，优化适当调整窗口高度，解决分辨率不够,看不全的问题，优化文件扫描，敏感信息的任务初始化操作步骤。修复文件接口扫描导出因返回包太大无法导出的bug，修复了资产测绘条件语句中包含保留词无法导出的bug，增加首页重要信息的复制功能。 |
| 2024.5.15 | 增加了将工具里面的配置项保存到配置文件，启动加载功能，调整了资产测绘的导出方式，优化文件扫描过滤功能，优化了扫描线程BUG,优化主界面域名信息查询的正则表达式.优化quake注册会员、高级会员的domain查询字段的bug,优化了使用中的一些细节bug |
| 2024.5.8  | 修正使用中各位师傅提的bug，基本信息模块新增软件著作权，子域名，IP反查域名解析记录，资产测绘增加配置Hunter的多KEY轮询查询功能，文件目录扫描增加了按域名+压缩文件后缀的组合方式。 |
| 2024.5.6  | 增加权重信息查询，增加资产测绘的自动加载查询，优化指纹扫描，接口扫描，文件目录扫描功能，增加密码字典功能。优化网站导航信息 |
| 2024.4.24 | 界面功能增加指纹识别扫描模块，支持从资产测绘联动到指纹识别，从指纹识别联动敏感信息、文件扫描模块 |
| 2024.4.20 | 增加资产测绘模块，调整界面布局，资产测绘支持fofa,hunter,quake3个引擎的查询，并支持右键菜单与敏感信息扫描、文件扫描模块的联动功能 |
| 2024.4.13 | 优化了接口未授权扫描的界面卡顿问题以及接口抓取完成自动触发接口未授权扫描计算bug |
| 2024.4.11 | 将敏感信息界面重构了，增加了接口抓取及未授权接口探测功能。（正则表达式感觉还不够完美，下一版再优化一下） |
| 2024.4.7  | 优化文件扫描的多线程扫描功能，增加网站导航地址               |

###  4.如何运行

 在jdk8环境下（在jdk8以上的高版本请参考常见问题1的处理方案）运行以下语句运行:

```
java -jar mitan-jar-with-dependencies.jar
```

​	若不想输入这么长太长语句，可以通过以下脚本的方式启动：

1.   Mac/Linux 环境下，可以通过sh文件启动，需要在控制台窗口先给予**start.sh**权限。

```
chmod +x start.sh
```

赋予权限后，每次在控制台窗口执行如下命令打开工具

```
./start.sh
```

   2. windows系统直接双击"**start.bat**" 文件启动工具

   运行成功显示以下界面：



- **界面风格：**

![image-20241103122359066](Readme.assets/image-20241103122359066.png)

![image-20241103122425059](Readme.assets/image-20241103122425059.png)

![image-20241103122446061](Readme.assets/image-20241103122446061.png)

-  **资产测绘**

![image-20250323224307099](Readme.assets/image-20250323224307099.png)

- **敏感信息（接口未授权）**

![image-20250323224357396](Readme.assets/image-20250323224357396.png)

- **备份扫描**

![image-20240531190411178](Readme.assets/image-20240531190411178.png)

- **目录扫描**

![image-20240531180350510](Readme.assets/image-20240531180350510.png)

- **批量权重查询**

![image-20250104143232200](Readme.assets/image-20250104143232200.png)

- **工具箱**

![image-20250104143249724](Readme.assets/image-20250104143249724.png)

- **渗透备忘**

![image-20240805142840478](Readme.assets/image-20240805142840478.png)

**代理池**

![image-20250222215943011](Readme.assets/image-20250222215943011.png)

**关于与更新** 

![image-20250222220137975](Readme.assets/image-20250222220137975.png)

### 5.常见问题

#### （1）运行时错误提示: 缺少 JavaFX 运行时组件的解决方法。

 **JavaFX 从 Java 11 开始从 JDK中移除，JDK11以上的需要单独下载和配置javaFx。**

##### 1. 下载 JavaFX SDK

首先，从 [Gluon](https://gluonhq.com/products/javafx/) 网站 下载对应操作系统的 JavaFX SDK。

##### 2. 解压到目录

将下载的 JavaFX SDK 解压到一个目录中（例如 `C:\javafx-sdk-21`）。

##### 3. 运行 JAR 文件时指定 JavaFX 模块路径

在运行你的 JAR 文件时，需要指定 JavaFX 模块的路径。假设你的 JavaFX SDK 解压在 `C:\javafx-sdk-21`，你可以使用以下命令来运行你的 JAR 文件：

```
java --module-path "C:\javafx-sdk-21\lib" --add-modules javafx.controls,javafx.fxml -jar mitan-jar-with-dependencies.jar
```

在这个命令中：

- `--module-path "C:\javafx-sdk-21\lib"` 指定了 JavaFX 模块的路径。

- `--add-modules javafx.controls,javafx.fxml` 添加了所需的 JavaFX 模块，根据你的应用程序可能需要添加其他模块。

  

  **感谢 p1at0x ，s0nd9r师傅在Issues中提出的解决方案，可自行根据操作系统修改start.bat或start.sh脚本文件，解决快速启动。**

  

#### （2） 若遇到界面乱码问题，建议指定编码方式进行启动。

```
java "-Dfile.encoding=UTF-8" -jar mitan-jar-with-dependencies.jar
```

 **可自行根据操作系统修改start.bat或start.sh脚本文件，解决快速启动。**



#### （3） 关于ZoomEye查询提示“request invalid, validate usage and try again” 的解决方法

​     出现上述提示，是因为ZoomEye 注册用户的API查询权益分不够（个人版会员以上不会出现此问题）， 具体会员权益点击https://www.zoomeye.org/pricing 查看即可，想获取权益积分，可以关注ZoomEye公众号或加入官方社群。



###  6.互相交流

​      密探版本在不断更新，希望大家多多帮助完善提升。 密探渗透工具在开发过程中得到“长风安全”，“湘安无事“两个团队的师傅对工具的完善提供大量帮助，同时感谢**ZoomEye官方**在测试过程中提供**开发者权益支持**，有更好的想法也可以➕V：kkbo680  进入密探工具交流群（**密探工具交流群已超200人，加群二维码已扫不了，+V时请备注“加群”**），提供宝贵意见。 

![image-20240406180609618](Readme.assets/image-20240406180609618.png)

![image-20250104001005725](Readme.assets/image-20250104001005725.png)
