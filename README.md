# [首页查询更多项目](https://github.com/GraduationProject-springboot) 包安装运行


# 0144springboot在线问卷调查系统的设计与实现

![picture](https://raw.githubusercontent.com/GraduationProject-springboot/.github/main/img/wx.png)

### 点击播放视频 ▼
[![Watch the video](https://i.sstatic.net/Vp2cE.png)](https://www.bilibili.com/video/BV1jqaLe1ECs?p=43)


# 第1章 绪论
## 1.1 课题背景
二十一世纪互联网的出现，改变了几千年以来人们的生活，不仅仅是生活物资的丰富，还有精神层次的丰富。时代进步的标志，就是让人们过上更好的生活。在互联网诞生之前，地域位置往往是人们思想上不可跨域的鸿沟，信息的传播速度极慢，信息处理的速度和要求还是通过人们骑马或者是信鸽传递，这些信息传递都是不可控制的，中间很有可能丢失，信息的传递水平决定了人们生活的水平。现如今，大家都在用互联网来实现自己的目的，从内部管理设置计算机管理，提高内部信息管理水平，从外部市场也可以用计算机获取相关数据进行处理，如今各行各业已经严重依赖于计算机了。

本课题研究和开发在线问卷调查系统，让安装在计算机上的该系统变成管理人员的小帮手，提高问卷调查信息处理速度，规范问卷调查信息处理流程，让管理人员的产出效益更高。
## 1.2 课题意义
传统处理数据，必须是一张张纸，然后处理完毕又是统计在一张张纸上面，不断的重复处理，最终有个结果给最高层作为参考，这个模式在互联网没有出现之前，是一种常见的事情，信息管理的效率提不上去，那就用人才，人多力量大，是一个以前人们的常识。计算机的诞生就是发现了人多力量大的不足，比如高端计算人才的培养已经跟不上使用了，所以人们研究出专门帮助人们计算的机器，就是计算机的前身，到了互联网时代，人们发现完全可以让程序供应商提供解决方案，自己挑选自己合适的方案来提高自己的产出比。于是市面上就出现了各种各样的依靠程序处理信息的解决方案。

本课题研发的在线问卷调查系统，就是提供问卷调查信息处理的解决方案，它可以短时间处理完信息，并且只需要使用者动动鼠标和键盘就能获取自己需要的信息，并且这些信息都有专门的存储设备，而且数据的备份和迁移都可以设定为无人值守，从人力角度和信息处理角度以及信息安全角度，在线问卷调查系统是完胜传统纸质操作的，所以在线问卷调查系统就是如此的值得信赖。
## 1.3 研究内容
本文对在线问卷调查系统的设计与实现分成六个章节进行描述。

第1章：研究在线问卷调查系统的背景，以及开发在线问卷调查系统的意义。

第2章：对开发在线问卷调查系统的环境还有技术进行说明。

第3章：分析在线问卷调查系统的可行性，性能，流程以及功能。

第4章：设计在线问卷调查系统的功能结构，设计数据库E-R图以及对数据表的存储结构进行设计。

第5章：实现在线问卷调查系统的功能并进行功能界面展示。

第6章：对系统测试进行阐述，以及对本系统部分功能进行检测。
# 第2章 开发环境与技术
本章节对开发在线问卷调查系统需要搭建的开发环境，还有在线问卷调查系统开发中使用的编程技术等进行阐述。
## 2.1 Java语言  
Java语言是当今为止依然在编程语言行业具有生命力的常青树之一。Java语言最原始的诞生，不仅仅是创造者感觉C语言在编程上面很麻烦，如果只是专注于业务逻辑的处理，会导致忽略了各种指针以及垃圾回收这些操作，导致出现问题需要解决的时间往往大于正常编程处理业务逻辑的时间，这些是非常浪费时间的。Java语言的创造者就完美的解决了这个问题，把指针处理和垃圾处理全部自动化，虽然这会损失一些性能，但是随着计算机硬件的不断发展，这些性能是可以忽略考虑的。并且C语言是针对硬件开发的语言，在符合条件的硬件上面进行编程可以最大化利用硬件的性能，但是随着硬件的变化或者操作系统的变更，如果还是用C语言的话需要对整个程序进行重新编程，只有随着市场变化而变化的语言才是符合潮流，符合生存规律的语言。Java语言的创造者就针对C语言的缺点专门开发了Java语言。让Java语言不管是在什么样的环境里都是可以运行，因为在Java语言运行外面套了一个壳，也就是虚拟机，只要是Java虚拟机能安装的电脑都可以运行Java的程序。
## 2.2 MYSQL数据库
MySQL数据库是关系型数据库的一种，也是传统的行式数据模式，获取一些数据是先一行一行的获取，然后一行一行的显示，与最近大数据兴起的列式数据库有着明显的不同。行式数据库主要是处理最重要的数据逻辑部分，并且必须是有效数据，这样每一处的数据关联都是不可损坏，如果对数据安全性比较高的肯定是需要选择MySQL数据库，列式数据库的发明仅仅是因为读取效率高，与传统的MySQL数据库比起来在数据写入方面并不会高明到哪里。MySQL虽然比起oracle或者SQL SERVER来讲，安装包只是几十兆甚至几百兆，有点小，但是功能并不会弱到哪里，严格遵循SQL标准语法。MySQL的数据存放形式从大向小的说是数据库最大，然后是表，每个表里面存放数据是有一定的规则的，数据存放是表格形式的，也就是说有横也有竖，横着的为行，一般表示一条数据，每个表都有字段，而字段是以列的形式存在，这样能保证一条数据每一个字段对应的是相同数据类型的数据。表与表之间还可以进行关联，进行分表操作，如果一条数据相关项目属性太多，那么可以把有效的相关联系做成关联，可以设定是否唯一。
## 2.3 IDEA开发工具
IDEA是捷克共和国的Java程序员开发人员创造的一个开发软件，刚开始主要是对于用Eclipse软件他们用得不顺手，所以直接开发了这款软件。之所以不顺手原因在于没有代码提升功能，原因是Eclipse只是把代码提示作为一种插件形式的存在，如果有些程序开发人员不清楚代码提示插件可能会出问题，并且代码提示只是用来作为插件，所以功能上有所欠缺。IDEA不仅仅代码提示做的很好，在代码重构上面更上如虎添翼，程序开发人员可以选择一段代码然后IDEA就会对代码进行分解重构，有效的把代码弄得更够层次感，复用性更高，用着更简洁和方便，大大的减少了代码工作量，提升了代码开发效率。当然，IDEA对于使用者这么好，肯定也是有目的的，原因在于插件越多越友好，就需要花费大量的金钱来使用，所以说IDEA使用主要是看自己喜好。
## 2.4 Spring Boot框架
Spring Boot是一种不需要代码生成的一种框架，并且可以不需要配置任何的XML文件就可以，因为Spring Boot里面自带了很多接口，只需要配置不同的接口就会自动的应用并且识别需要的依赖，在配置方面非常的方便，使用起来感觉像没有用到框架的感觉。Spring Boot有很多默认的配置文件，并且可以对默认的配置文件进行修改，可以设置为自动加载，可以对异常处理分为全局异常处理和默认异常处理。Spring Boot使用过程中就像是使用什么直接注册什么，所谓的注册也就是在对应的类和方法上面进行一个特殊的声明即可。

# 第3章 系统分析
本文作者在确定了研究的课题之后，从各大数字图书馆下载文献来阅读，并了解同类型的网站具备的大致功能，然后与本系统用户的实际需求结合进行分析，得出本系统要研究的具体功能与性能。虽然分析系统这一阶段性工作主要是确定功能，但它却影响着后面系统开发环节的进展，它也是系统开发流程中比较重要的一个环节。
## 3.1 可行性分析
以下部分是从三个角度来进行可行性分析，确保开发成功的前提是有可行性分析，只有进行提前分析，符合程序开发流程才不至于开发过程的中断。
### 3.1.1 技术可行性
在技术实现层次，分析了好几种技术实现方法，并且都有对应的成功案例，也有很多开源模块可以进行参考，所以从技术可行性分析来讲，实现在线问卷调查系统是没有问题的。
### 3.1.2 经济可行性
对于身为学生的开发者而言，在经济资源上面可用者很少，为了开发在线问卷调查系统，通过从技术分析发现可以用自己用的电脑进行开发，并且学校机房的配置也可以达到要求。最重要的是技术资源一般都是开源免费使用的，因此得出结论，经济方面是具有可行性的。
### 3.1.3 操作可行性
在线问卷调查系统的具体实现，本身参考人类的正常操作逻辑，把常用的操作习惯当做主要的导航实现，可以让使用者更快速的理解并且上手操作，实现符合逻辑的操作流程是操作可行性的具体体现。

以上就是从不同的角度来分析，确保了在线问卷调查系统的正常开展。
## 3.2 系统流程
在线问卷调查系统投入使用后，其各个功能的内部操作逻辑需要使用者通过流程图来进行了解。
### 3.2.1 操作流程
使用者在操作在线问卷调查系统中，应该按照本系统提供的操作流程（图3.1即为本系统的操作流程图）进行操作，这样可以减少使用者操作中出现的错误，从而节省进入在线问卷调查系统的时间。

![](/md/blog.001.png)

图3.1 系统操作流程
### 3.2.2 登录流程
在线问卷调查系统通过登录功能（图3.2即为其登录的流程）引导使用者进入指定的功能操作区，也避免非本系统的用户享受本系统提供的服务以及查看本系统提供的信息，从而保障本系统用户的安全使用。

![](/md/blog.002.png)

图3.2 登录流程
### 3.2.3 删除信息流程
在线问卷调查系统在经过长期使用后，会产生很多的数据信息。为了腾出存储空间存放更多的数据，本系统数据库中存储的数据，一些没有参考价值的数据需要进行删除（图3.3即为删除信息的流程），删除数据过程中，为避免误删，使用者要根据系统的提示来决定是否删除数据。

![](/md/blog.003.png)

图3.3 删除信息流程
### 3.2.4 添加信息流程
在线问卷调查系统提供可视化的功能操作区，非常方便使用者进行数据操作，当使用者往系统中录入数据时（图3.4即为添加信息的流程），本系统也会进行数据合法性的判断，符合要求的数据才能够在数据库指定表中进行登记。

![](/md/blog.004.png)

图3.4 添加信息流程
## 3.3 性能需求
在需求分析中就应该对项目所需服务器性能进行分析，这样才符合正常的分析流程。只谈功能需求不谈性能需求，是一件很严重的事情，可能会导致使用过程中出现一系列不可预测的问题，所以性能需求也是需要考虑的重要项。

下面就是从几个方面来进行系统的性能分析，从每个角度来分析系统性能。

(1)系统数据的容量：从数据角度来分析，每个表和每个数据库，达到的数据量到一定的程度，是否需要分表或者是分库，超过了数据的设定限度，可能会导致数据反映迟钝，容错量增加。

(2)数据精度的要求：需要对需求分析里面数据设定环节，考虑相应的数据精度问题，需要发现数据是常用的精度还是非常用的精度，进而设定不同的数值。数据的精度问题，会直接导致设计的性能问题。

(3)时间响应要求：从用户提交操作，到页面反映，中间有个数据处理的问题，如果数据量大，那么考虑索引问题和分库问题，数据量再大就要考虑增加列式数据库的问题，这些都要根据数据量的增加以及逻辑的严密性来进行判断，才能符合用户的要求，毕竟响应时间太久操作起来也不舒服。

系统的性能需求从业务需求之初就能大致了解到性能需求相关的概念，再从系统性能需求来逐条实现，可以让设计的系统有使用价值。
## 3.4 功能需求
在线问卷调查系统根据使用权限的角度进行功能分析，并运用用例图来展示各个权限需要操作的功能。

图3.5即为管理员用例图，管理员权限操作的功能包括对注册用户信息的管理，对问卷，题目，问卷调查，新闻资讯等信息的管理。

![](/md/blog.005.png)

图3.5 管理员用例图

图3.6即为用户用例图，用户权限操作的功能包括参与问卷调查，查看新闻，查看问卷调查记录。

![](/md/blog.006.png)

图3.6 用户用例图
# 第4章 系统设计
系统的设计一切都是为了用户的使用，虽然用户使用过程中可能只是面对着浏览器进行各种操作，但是不代表着系统对于用户在浏览器上的操作不进行处理，所以说，设计一个系统需要考虑到方方面面。
## 4.1 功能结构设计
图4.1即为设计的管理员功能结构，管理员权限操作的功能包括对注册用户信息的管理，对问卷，题目，问卷调查，新闻资讯等信息的管理。

![](/md/blog.007.png)

图4.1 管理员功能结构

图4.2即为设计的用户功能结构，用户权限操作的功能包括参与问卷调查，查看新闻，查看问卷调查记录。

![](/md/blog.008.png)

图4.2 用户功能结构
## 4.2 数据库设计
在线问卷调查系统运行中产生的数据需要按照提前设置的存储规则进行保存，而这个存储规则则是在数据库的设计中进行设置的。通常情况下，为了更好的配合系统运行，也要给用户带来良好的使用体验，设计一个很好的数据库是必须的，因为它能减少用户的等待时间，还可以对系统的请求在最短时间内进行响应。所以，对数据库设计时，需要花费一定的时间来分析系统对于数据存储的要求以及存储的具体数据，然后设计具体的存储规则，保证数据库能够对系统的各种数据请求进行及时回应，缩短数据处理时间，并在一定程度上降低数据冗余，节省存储空间。
### 4.2.1 数据库概念设计
实体-联系图还有一个名称即E-R图，是Entity Relationship Diagram各英文单词首字母的缩写，它这种概念模型通常用于对现实世界进行描述。同时它还是一种能够直观表达数据中实体，联系，属性的有效手段。绘制E-R图能够选择的工具也有很多，但是Office Visio 这款软件在E-R图的绘制上一般都是作为首选工具，因为它是基于可视化处理，使用它创建E-R图非常简单。使用基本的E-R图构成元素，比如椭圆，菱形，矩形，还有实线段来表达对应的信息，椭圆代表属性，即实体的特征，矩形代表实体，即数据库中的一个具体数据表，菱形代表实体中相互关系，实线段主要是完成椭圆，矩形，菱形的连接，基于这样的方式即可完成对本系统的E-R图进行完整绘制。

（1）图4.4即为题目这个实体所拥有的属性值。

![](/md/blog.009.png)

图4.4 题目实体属性图

（2）图4.5即为用户这个实体所拥有的属性值。

![](/md/blog.010.png)

图4.5 用户实体属性图

（3）图4.6即为问卷这个实体所拥有的属性值。

![](/md/blog.011.png)

图4.6 问卷实体属性图

4. 图4.7即为问卷调查记录这个实体所拥有的属性值。

![](/md/blog.012.png)

图4.7 问卷调查记录实体属性图

4. 图4.8即为上面介绍的实体中存在的联系。

![](/md/blog.013.png)

图4.8 实体间关系E-R图
### 4.2.2 数据库物理设计
本小节主要任务即是根据上述内容进行数据存储结构的设计，也就是在数据库中设计存放本系统的数据的数据表，设计数据表时，需要对各个字段进行确定，通常来说，一个实体与一张数据表相对应，实体的属性就用来表示字段名称，不同的字段表示的数据类型以及取值都不相同，这里需要根据系统实际数据的情况进行设置，同时也需要在具体表中确定该表的主键，以及该表各个字段是否能够保持空等进行说明，设计完成一张数据表的结构之后，在保存时同样要命名，尽量选择英文名称进行命名并保存，方便今后系统对数据表进行数据存储访问时，在提高数据存储效率的同时，还不容易导致系统出错。接下来就对设计的数据表进行展示。

表4.1 问卷表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|int(20)|否|
|exampaper\_name|问卷名称 |varchar(200)|否|
|exampaper\_date|时长(分钟)|int(11)|否|
|exampaper\_jieshuyu|结束语|varchar(255)|是|
|exampaper\_types|问卷状态 |int(11)|否|
|create\_time|创建时间|timestamp|否|
表4.2 题目表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|int(20)|否|
|exampaper\_id|所属问卷id（外键）|int(20)|否|
|examquestion\_name|试题名称 |varchar(200)|否|
|examquestion\_options|选项|longtext|是|
|examquestion\_types|试题类型|int(20)|是|
|examquestion\_sequence|试题排序，值越大排越前面|int(20)|是|
|create\_time|创建时间|timestamp|否|
表4.3 问卷调查记录表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|int(20)|否|
|examrecord\_uuid\_number|问卷调查编号|varchar(200)|是|
|yonghu\_id|问卷调查用户|int(20)|否|
|exampaper\_id|所属问卷id（外键）|int(20)|否|
|insert\_time|问卷调查时间|timestamp|否|
|create\_time|创建时间|timestamp|否|
表4.4 管理员表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|bigint(20)|否|
|username|用户名|varchar(100)|否|
|password|密码|varchar(100)|否|
|role|角色|varchar(100)|是|
|addtime|新增时间|timestamp|否|
表4.5 新闻资讯表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|int(11)|否|
|news\_name|新闻资讯名称 |varchar(200)|是|
|news\_types|新闻类型 |int(11)|是|
|news\_photo|新闻资讯图片|varchar(200)|是|
|insert\_time|新闻资讯时间|timestamp|是|
|news\_content|新闻资讯详情|text|是|
|create\_time|创建时间 |timestamp|是|
表4.6 答题详情表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|int(20)|否|
|examredetails\_uuid\_number|问卷编号|varchar(200)|是|
|yonghu\_id|用户id|int(20)|否|
|examquestion\_id|试题id（外键）|int(20)|否|
|examredetails\_myanswer|用户选项|varchar(200)|是|
|create\_time|创建时间|timestamp|否|
表4.7 用户表

|字段|注释|类型|空|
| :-: | :-: | :-: | :-: |
|id (主键)|主键|int(11)|否|
|username|账户|varchar(200)|是|
|password|密码|varchar(200)|是|
|yonghu\_name|用户姓名 |varchar(200)|是|
|sex\_types|性别 |int(11)|是|
|yonghu\_id\_number|身份证号|varchar(200)|是|
|yonghu\_phone|手机号|varchar(200)|是|
|yonghu\_photo|照片|varchar(200)|是|
|create\_time|创建时间|timestamp|是|
第5章 系统实现

编程人员在搭建的开发环境中，运用编程技术实现本系统设计的各个操作权限的功能。在本节中，就展示部分操作权限的功能与界面。
## 5.1 管理员功能实现
### 5.1.1 问卷管理
图5.1 即为编码实现的问卷管理界面，管理员在该界面中可以对已有问卷进行启用或禁用，可以新增问卷，编辑更改已有问卷的资料，包括问卷名称，结束语等信息，可以删除需要删除的问卷，可以根据问卷名称，问卷的状态来获取需要的问卷信息。

![](/md/blog.014.png)

图5.1 问卷管理界面

核心代码：

`    `/\*\*

`    `\* 后端修改

`    `\*/

`    `@RequestMapping("/update")

`    `public R update(@RequestBody ExampaperEntity exampaper, HttpServletRequest request){

`        `logger.debug("update方法:,,Controller:{},,exampaper:{}",this.getClass().getName(),exampaper.toString());

`        `String role = String.valueOf(request.getSession().getAttribute("role"));

`        `if(StringUtil.isEmpty(role))

`            `return R.error(511,"权限为空");

`        `//根据字段查询是否有相同数据

`        `Wrapper<ExampaperEntity> queryWrapper = new EntityWrapper<ExampaperEntity>()

`            `.notIn("id",exampaper.getId())

`            `.andNew()

`            `.eq("exampaper\_name", exampaper.getExampaperName())

`            `.eq("exampaper\_date", exampaper.getExampaperDate())

`            `.eq("exampaper\_types", exampaper.getExampaperTypes())

`            `;

`        `logger.info("sql语句:"+queryWrapper.getSqlSegment());

`        `ExampaperEntity exampaperEntity = exampaperService.selectOne(queryWrapper);

`        `if(exampaperEntity==null){

`            `//  String role = String.valueOf(request.getSession().getAttribute("role"));

`            `//  if("".equals(role)){

`            `//      exampaper.set

`            `//  }

`            `exampaperService.updateById(exampaper);//根据id更新

`            `return R.ok();

`        `}else {

`            `return R.error(511,"表中有相同数据");

`        `}

`    `}

`    `/\*\*

`    `\* 删除

`    `\*/

`    `@RequestMapping("/delete")

`    `public R delete(@RequestBody Integer[] ids){

`        `logger.debug("delete:,,Controller:{},,ids:{}",this.getClass().getName(),ids.toString());

`        `exampaperService.deleteBatchIds(Arrays.asList(ids));

`        `return R.ok();

`    `}

### 5.1.2 问卷调查管理
图5.2 即为编码实现的问卷调查管理界面，管理员在该界面中对用户提交的问卷调查信息进行查看，管理员可以直接查看每条问卷调查的调查详情信息，同时可以删除问卷调查信息。

![](/md/blog.015.png)

图5.2 问卷调查管理界面

核心代码：

/\*\*

`     `\* 批量上传

`     `\*/

`    `@RequestMapping("/batchInsert")

`    `public R save( String fileName){

`        `logger.debug("batchInsert方法:,,Controller:{},,fileName:{}",this.getClass().getName(),fileName);

`        `try {

`            `List<ExampaperEntity> exampaperList = new ArrayList<>();//上传的东西

`            `Map<String, List<String>> seachFields= new HashMap<>();//要查询的字段

`            `Date date = new Date();

`            `int lastIndexOf = fileName.lastIndexOf(".");

`            `if(lastIndexOf == -1){

`                `return R.error(511,"该文件没有后缀");

`            `}else{

`                `String suffix = fileName.substring(lastIndexOf);

`                `if(!".xls".equals(suffix)){

`                    `return R.error(511,"只支持后缀为xls的excel文件");

`                `}else{

`                    `URL resource = this.getClass().getClassLoader().getResource("static/upload/" + fileName);//获取文件路径

`                    `File file = new File(resource.getFile());

`                    `if(!file.exists()){

`                        `return R.error(511,"找不到上传文件，请联系管理员");

`                    `}else{

`                        `List<List<String>> dataList = PoiUtil.poiImport(file.getPath());//读取xls文件

`                        `dataList.remove(0);//删除第一行，因为第一行是提示

`                        `for(List<String> data:dataList){

`                            `//循环

`                            `ExampaperEntity exampaperEntity = new ExampaperEntity();

//                            exampaperEntity.setExampaperName(data.get(0));                    //问卷名称 要改的

//                            exampaperEntity.setExampaperDate(Integer.valueOf(data.get(0)));   //时长(分钟) 要改的

//                            exampaperEntity.setExampaperTypes(Integer.valueOf(data.get(0)));   //问卷状态 要改的

//                            exampaperEntity.setCreateTime(date);//时间

`                            `exampaperList.add(exampaperEntity);


`                            `//把要查询是否重复的字段放入map中

`                        `}

`                        `//查询是否重复

`                        `exampaperService.insertBatch(exampaperList);

`                        `return R.ok();

`                    `}

`                `}

`            `}

`        `}catch (Exception e){

`            `return R.error(511,"批量插入数据异常，请联系管理员");

`        `}

`    `}




`    `/\*\*

`    `\* 前端列表

`    `\*/

`    `@IgnoreAuth

`    `@RequestMapping("/list")

`    `public R list(@RequestParam Map<String, Object> params, HttpServletRequest request){

`        `logger.debug("list方法:,,Controller:{},,params:{}",this.getClass().getName(),JSONObject.toJSONString(params));

`        `// 没有指定排序字段就默认id倒序

`        `if(StringUtil.isEmpty(String.valueOf(params.get("orderBy")))){

`            `params.put("orderBy","id");

`        `}

`        `PageUtils page = exampaperService.queryPage(params);

`        `//字典表数据转换

`        `List<ExampaperView> list =(List<ExampaperView>)page.getList();

`        `for(ExampaperView c:list)

`            `dictionaryService.dictionaryConvert(c, request); //修改对应字典表字段

`        `return R.ok().put("data", page);

`    `}

`    `/\*\*

`    `\* 前端详情

`    `\*/

`    `@RequestMapping("/detail/{id}")

`    `public R detail(@PathVariable("id") Long id, HttpServletRequest request){

`        `logger.debug("detail方法:,,Controller:{},,id:{}",this.getClass().getName(),id);

`        `ExampaperEntity exampaper = exampaperService.selectById(id);

`            `if(exampaper !=null){

`                `//entity转view

`                `ExampaperView view = new ExampaperView();

`                `BeanUtils.copyProperties( exampaper , view );//把实体数据重构到view中

`                `//修改对应字典表字段

`                `dictionaryService.dictionaryConvert(view, request);

`                `return R.ok().put("data", view);

`            `}else {

`                `return R.error(511,"查不到数据");

`            `}

`    `}

### 5.1.3 题目管理
图5.3 即为编码实现的题目管理界面，管理员在该界面中可以导出题目，可以新增题目，可以对指定的题目信息进行修改，删除，同时可以查看用户对各个题目选项的统计信息，该统计信息是以饼图进行展示。

![](/md/blog.016.png)

图5.3 题目管理界面

核心代码：

` `/\*\*

`    `\* 后端详情

`    `\*/

`    `@RequestMapping("/info/{id}")

`    `public R info(@PathVariable("id") Long id, HttpServletRequest request){

`        `logger.debug("info方法:,,Controller:{},,id:{}",this.getClass().getName(),id);

`        `ExamquestionEntity examquestion = examquestionService.selectById(id);

`        `if(examquestion !=null){

`            `//entity转view

`            `ExamquestionView view = new ExamquestionView();

`            `BeanUtils.copyProperties( examquestion , view );//把实体数据重构到view中

`                `//级联表

`                `ExampaperEntity exampaper = exampaperService.selectById(examquestion.getExampaperId());

`                `if(exampaper != null){

`                    `BeanUtils.copyProperties( exampaper , view ,new String[]{ "id", "createDate"});//把级联的数据添加到view中,并排除id和创建时间字段

`                    `view.setExampaperId(exampaper.getId());

`                `}

`            `//修改对应字典表字段

`            `dictionaryService.dictionaryConvert(view, request);

`            `return R.ok().put("data", view);

`        `}else {

`            `return R.error(511,"查不到数据");

`        `}

`    `}

`    `/\*\*

`    `\* 后端保存

`    `\*/

`    `@RequestMapping("/save")

`    `public R save(@RequestBody ExamquestionEntity examquestion, HttpServletRequest request){

`        `logger.debug("save方法:,,Controller:{},,examquestion:{}",this.getClass().getName(),examquestion.toString());

`        `String role = String.valueOf(request.getSession().getAttribute("role"));

`        `if(StringUtil.isEmpty(role))

`            `return R.error(511,"权限为空");

`        `Wrapper<ExamquestionEntity> queryWrapper = new EntityWrapper<ExamquestionEntity>()

`            `.eq("exampaper\_id", examquestion.getExampaperId())

`            `.eq("examquestion\_name", examquestion.getExamquestionName())

`            `.eq("examquestion\_options", examquestion.getExamquestionOptions())

`            `.eq("examquestion\_types", examquestion.getExamquestionTypes())

`            `.eq("examquestion\_sequence", examquestion.getExamquestionSequence())

`            `;

`        `logger.info("sql语句:"+queryWrapper.getSqlSegment());

`        `ExamquestionEntity examquestionEntity = examquestionService.selectOne(queryWrapper);

`        `if(examquestionEntity==null){

`            `examquestion.setCreateTime(new Date());

`            `examquestionService.insert(examquestion);

`            `return R.ok();

`        `}else {

`            `return R.error(511,"表中有相同数据");

`        `}

`    `}
### 5.1.4 用户管理
图5.4 即为编码实现的用户管理界面，管理员在该界面中为用户重置密码，修改用户基本信息，新增用户，删除需要删除的用户信息。

![](/md/blog.017.png)

图5.4 用户管理界面

核心代码：

` `/\*\*

`    `\* 后端修改

`    `\*/

`    `@RequestMapping("/update")

`    `public R update(@RequestBody YonghuEntity yonghu, HttpServletRequest request){

`        `logger.debug("update方法:,,Controller:{},,yonghu:{}",this.getClass().getName(),yonghu.toString());

`        `String role = String.valueOf(request.getSession().getAttribute("role"));

`        `if(StringUtil.isEmpty(role))

`            `return R.error(511,"权限为空");

`        `//根据字段查询是否有相同数据

`        `Wrapper<YonghuEntity> queryWrapper = new EntityWrapper<YonghuEntity>()

`            `.notIn("id",yonghu.getId())

`            `.andNew()

`            `.eq("username", yonghu.getUsername())

`            `.or()

`            `.eq("yonghu\_id\_number", yonghu.getYonghuIdNumber())

`            `.or()

`            `.eq("yonghu\_phone", yonghu.getYonghuPhone())

`            `;

`        `logger.info("sql语句:"+queryWrapper.getSqlSegment());

`        `YonghuEntity yonghuEntity = yonghuService.selectOne(queryWrapper);

`        `if("".equals(yonghu.getYonghuPhoto()) || "null".equals(yonghu.getYonghuPhoto())){

`                `yonghu.setYonghuPhoto(null);

`        `}

`        `if(yonghuEntity==null){

`            `//  String role = String.valueOf(request.getSession().getAttribute("role"));

`            `//  if("".equals(role)){

`            `//      yonghu.set

`            `//  }

`            `yonghuService.updateById(yonghu);//根据id更新

`            `return R.ok();

`        `}else {

`            `return R.error(511,"账户或者手机号或者身份证号已经被使用");

`        `}

`    `}
### 5.1.5 新闻资讯管理
图5.5 即为编码实现的新闻资讯管理界面，管理员在该界面中负责发布新闻资讯，更改新闻资讯的部分信息，删除需要删除的新闻资讯信息。

![](/md/blog.018.png)

图5.5 新闻资讯管理界面

核心代码：

` `/\*\*

`    `\* 后端列表

`    `\*/

`    `@RequestMapping("/page")

`    `public R page(@RequestParam Map<String, Object> params, HttpServletRequest request){

`        `logger.debug("page方法:,,Controller:{},,params:{}",this.getClass().getName(),JSONObject.toJSONString(params));

`        `String role = String.valueOf(request.getSession().getAttribute("role"));

`        `if(StringUtil.isEmpty(role))

`            `return R.error(511,"权限为空");

`        `else if("用户".equals(role))

`            `params.put("yonghuId",request.getSession().getAttribute("userId"));

`        `if(params.get("orderBy")==null || params.get("orderBy")==""){

`            `params.put("orderBy","id");

`        `}

`        `PageUtils page = newsService.queryPage(params);

`        `//字典表数据转换

`        `List<NewsView> list =(List<NewsView>)page.getList();

`        `for(NewsView c:list){

`            `//修改对应字典表字段

`            `dictionaryService.dictionaryConvert(c, request);

`        `}

`        `return R.ok().put("data", page);

`    `}

## 5.2 用户功能实现
### 5.2.1 问卷列表
图5.6 即为编码实现的问卷列表界面，用户在该界面中选择问卷并参与问卷调查。

![](/md/blog.019.png)

图5.6 问卷列表界面

核心代码：

/\*\*

`    `\* 前端列表

`    `\*/

`    `@IgnoreAuth

`    `@RequestMapping("/list")

`    `public R list(@RequestParam Map<String, Object> params, HttpServletRequest request){

`        `logger.debug("list方法:,,Controller:{},,params:{}",this.getClass().getName(),JSONObject.toJSONString(params));

`        `// 没有指定排序字段就默认id倒序

`        `if(StringUtil.isEmpty(String.valueOf(params.get("orderBy")))){

`            `params.put("orderBy","id");

`        `}

`        `PageUtils page = examrecordService.queryPage(params);

`        `//字典表数据转换

`        `List<ExamrecordView> list =(List<ExamrecordView>)page.getList();

`        `for(ExamrecordView c:list)

`            `dictionaryService.dictionaryConvert(c, request); //修改对应字典表字段

`        `return R.ok().put("data", page);

`    `}

`    `/\*\*

`    `\* 前端详情

`    `\*/

`    `@RequestMapping("/detail/{id}")

`    `public R detail(@PathVariable("id") Long id, HttpServletRequest request){

`        `logger.debug("detail方法:,,Controller:{},,id:{}",this.getClass().getName(),id);

`        `ExamrecordEntity examrecord = examrecordService.selectById(id);

`            `if(examrecord !=null){

`                `//entity转view

`                `ExamrecordView view = new ExamrecordView();

`                `BeanUtils.copyProperties( examrecord , view );//把实体数据重构到view中

`                `//级联表

`                    `ExampaperEntity exampaper = exampaperService.selectById(examrecord.getExampaperId());

`                `if(exampaper != null){

`                    `BeanUtils.copyProperties( exampaper , view ,new String[]{ "id", "createDate"});//把级联的数据添加到view中,并排除id和创建时间字段

`                    `view.setExampaperId(exampaper.getId());

`                `}

`                `//级联表

`                    `YonghuEntity yonghu = yonghuService.selectById(examrecord.getYonghuId());

`                `if(yonghu != null){

`                    `BeanUtils.copyProperties( yonghu , view ,new String[]{ "id", "createDate"});//把级联的数据添加到view中,并排除id和创建时间字段

`                    `view.setYonghuId(yonghu.getId());

`                `}

`                `//修改对应字典表字段

`                `dictionaryService.dictionaryConvert(view, request);

`                `return R.ok().put("data", view);

`            `}else {

`                `return R.error(511,"查不到数据");

`            `}

`    `}

### 5.2.2 问卷调查
图5.7 即为编码实现的问卷调查界面，用户在该界面中主要根据问卷调查题目信息进行选项答题，答题结束可以选择界面顶端的结束问卷调查按钮离开问卷调查界面。

![](/md/blog.020.png)

图5.7 问卷调查界面

核心代码：

/\*\*

`    `\* 前端详情

`    `\*/

`    `@RequestMapping("/detail/{id}")

`    `public R detail(@PathVariable("id") Long id, HttpServletRequest request){

`        `logger.debug("detail方法:,,Controller:{},,id:{}",this.getClass().getName(),id);

`        `ExamredetailsEntity examredetails = examredetailsService.selectById(id);

`            `if(examredetails !=null){

`                `//entity转view

`                `ExamredetailsView view = new ExamredetailsView();

`                `BeanUtils.copyProperties( examredetails , view );//把实体数据重构到view中

`                `//级联表

`                    `ExamquestionEntity examquestion = examquestionService.selectById(examredetails.getExamquestionId());

`                `if(examquestion != null){

`                    `BeanUtils.copyProperties( examquestion , view ,new String[]{ "id", "createDate"});//把级联的数据添加到view中,并排除id和创建时间字段

`                    `view.setExamquestionId(examquestion.getId());

`                `}

`                `//级联表

`                    `YonghuEntity yonghu = yonghuService.selectById(examredetails.getYonghuId());

`                `if(yonghu != null){

`                    `BeanUtils.copyProperties( yonghu , view ,new String[]{ "id", "createDate"});//把级联的数据添加到view中,并排除id和创建时间字段

`                    `view.setYonghuId(yonghu.getId());

`                `}

`                `//修改对应字典表字段

`                `dictionaryService.dictionaryConvert(view, request);

`                `return R.ok().put("data", view);

`            `}else {

`                `return R.error(511,"查不到数据");

`            `}

`    `}
### 5.2.3 新闻资讯
图5.8 即为编码实现的新闻资讯界面，用户在该界面中浏览新闻资讯，在界面右上角的搜索框中编辑新闻标题可以获取匹配的新闻资讯信息。

![](/md/blog.021.png)

图5.8 新闻资讯界面

核心代码：

`  `/\*\*

`    `\* 前端详情

`    `\*/

`    `@RequestMapping("/detail/{id}")

`    `public R detail(@PathVariable("id") Long id, HttpServletRequest request){

`        `logger.debug("detail方法:,,Controller:{},,id:{}",this.getClass().getName(),id);

`        `NewsEntity news = newsService.selectById(id);

`            `if(news !=null){

`                `//entity转view

`                `NewsView view = new NewsView();

`                `BeanUtils.copyProperties( news , view );//把实体数据重构到view中

`                `//修改对应字典表字段

`                `dictionaryService.dictionaryConvert(view, request);

`                `return R.ok().put("data", view);

`            `}else {

`                `return R.error(511,"查不到数据");

`            `}

`    `}

### 5.2.4 问卷调查记录
图5.9 即为编码实现的问卷调查记录界面，用户在该界面中可以对参与问卷调查的记录信息进行查看。

![](/md/blog.022.png)

图5.9 问卷调查记录界面

核心代码：

`    `@RequestMapping("/saveExamredetails")

`    `public R saveExamredetails(@RequestBody ExamredetailsEntity examredetails,Integer examrecordId, HttpServletRequest request){

`        `logger.debug("save方法:,,Controller:{},,examredetails:{}",this.getClass().getName(),examredetails.toString());

`        `String role = String.valueOf(request.getSession().getAttribute("role"));

`        `if(StringUtil.isEmpty(role)){

`            `return R.error(511,"权限为空");

`        `}else if(role.contains("用户id")){

`            `examredetails.setYonghuId(Integer.valueOf(String.valueOf(request.getSession().getAttribute("userId"))));

`        `}

`        `examredetails.setCreateTime(new Date());

`        `boolean insert = examredetailsService.insert(examredetails);

`        `if(!insert){

`            `return R.error();

`        `}

`        `return R.ok();

`    `}

# 










