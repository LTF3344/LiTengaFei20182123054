1.理论部分，回答以下问题：
1）．试论述类与用例的区别。
答：类是对一组具有相同属性、操作、关系和语义的对象的描述。类是对事物的抽象。而用例是对一组序列动作的描述，系统执行这些动作将对用例的参与者产生可以观察的结果。

2）．试比较边界类与实体类的异同。
答: 实体类是对系统中需要存储的信息和其信息的行为建立模型。实体类具有永久的特性，这类似于数据库中的表一样用于保存系统的业务信息。 边界类位于系统与外界的交接处，它在一个或多个角色和系统之间建立相互作用的模型。

3）．试运用本节所学的静态建模技术找出用户管理模块中的所有的类。
答: 学生是参与者的类，它的属性包括：学号、姓名、账户和密码。
师是参与者的类，它的属性包括：账户和密码、姓名、所教专业。
教务员是参与者的类，它的属性包括：账户和密码、学生及老师所在院系。
系统管理员是管理员类，它的属性包括：账户和密码、姓名、工号。

4）．请找出学生管理系统中学生注册用例的实体类，边界类，控制类。
答: 学生类就是实体类，边界类是注册界面类，控制类应该是注册类，对应的是用例中的注册。具体的有：实体类：Generate Report Cards、Distribute electronically
边界类：View Cards、Logon、Update Cards、Load Cards、Record Cards、Save Cards
控制类：Teacher、Administrator、Student
UML中类有三种主要的版型：边界类、控制类和实体类。引入边界类、控制类及实体类的概念有助于分析和设计人员确定系统中的类。
边界类位于系统与外界的交界处，窗体、报表、以及表示通讯协议的类、直接与外部设备交互的类、直接与外部系统交互的类等都是边界类。通过用例图可以确定需要的边界类，每个Actor/Use Case对至少要一个边界类，但并非每个Actor/Use Case对要唯一的边界类。
实体类保存要放进持久存储体的信息。持久存储体就是数据库、文件等可以永久存储数据的介质。
实体类可以通过事件流和交互图发现。通常每个实体类在数据库中有相应的表，实体类中的属性对应数据库表中的字段。
控制类是控制其他类工作的类。每个用例通常有一个控制类，控制用例中的事件顺序，控制类也可以在多个用例间共用。其他类并不向控制类发送很多消息，而是由控制类发出很多消息。

5）．什么是依赖？它与关联有什么区别？
答: 依赖是一种使用关系，它说明了一个事物声明说明的变化可能影响到使用它的另一个事物，但反之未必。也就是说，服务的使用者以某种方式依赖于服务的提供者。而关联是一种结构关系，它详述了一个事物的对象与另一个事物的对象相互联系。

6)．什么是泛化？泛化是否就是类的继承，如果不是请说明理由。
答: 泛化是一般事物（称为父类或超类）和较特殊事物（称为子类或孩子类）之间的关系。 泛化不是类的继承，类的继承是泛化的一种。

7）．试论述聚合和组合的异同。
答: 聚合描述了整体对象拥有部分对象的关系。组合是聚合的一种形式，它具有强的拥有关系，而且整体与部分的生命周期是一致的。

2.学院公众号中，成绩查询模块可以很方便地使在校学生查询到期末考试成绩，特别是老师将期末成绩提交后，该模块会以弹窗的方式将信息通知到学生，问题：请根据滇池学院微信公众号中，学生成绩查询模块的功能，对该模块进行小组讨论分析，对该功能的类图中以下元素进行必要说明：
（1）该功能一共应该包含哪几个类？
答：该功能一共包括成绩查询、成绩、成绩类型、学科类型、上传成绩五个类。

（2）每个类的属性，方法应该是什么，有什么作用，权限该是什么？
答：成绩查询类包含学号、姓名、学期、成绩四个属性，包含查询、学期筛选、返回三个方法。权限限制学生可以查询。
成绩类包含考试科目、总评成绩、成绩类型、学科类型、实修学分、绩点、学分绩、平时成绩、作业成绩、期中成绩、期末成绩十一个属性，包含成绩下载一个方法。权限限制老师可查询。
成绩类型包含百分制、二级制、五级制三个属性，包含选择成绩类型一个方法。权限允许老师修改。
学科类型包含专业核心、技能素质公选、学科基础、专业选修、专业必修、公共必修、素质选修、综合实践八个属性，包含选择学科类型一个方法。权限允许老师修改
上传成绩类包含专业核心、技能素质公选、学科基础、专业选修、专业必修、公共必修、素质选修、综合实践八个属性，包含上传、修改、退出三个方法。权限允许老师登录。

（3）类之间分别有什么关系？
答：成绩查询类与成绩类是依赖关系，成绩查询类依赖于成绩类，成绩类与上传成绩类是泛化关系，成绩类继承了上传成绩类的属性，成绩类与成绩类型类和学科类型是关联关系。

（4）使用 staruml 画出该功能模块
 

3、网络的普及带给了人们更多的学习途径，随之而来的管理远程网络教学的“远程网络教学系统”诞生了。“远程网络教学系统”的功能需求如下：学生登录网站后，可以浏览课件、查找课件、下载课件、观看教学视频。教师登录网站后，可以上传课件、上传教学视频、发布教学心得、查看教学心得、修改教学心得。系统管理员负责对网站页面的维护、审核不合法课件和不合法教学信息、批准用户注册。
问题：老师需要登录“远程网络教学系统”后才能正常使用该系统的所有功能。如果忘记密码，可与通过“找回密码”功能恢复密码。请使用staruml 画出教师参与者的类图。
 
类有：浏览课件、查找课件、下载课件、观看教学视频。上传课件、上传教学视频、发布教学心得、查看教学心得、修改教学心得。维护、审核、批准。
实现的：学生可以浏览课件、查找课件、下载课件、观看教学视频。老师登录“远程网络教学系统”后使用该系统的所有功能。如果忘记密码，通过“找回密码”功能恢复密码。教师登录网站后，可以上传课件、上传教学视频、发布教学心得、查看教学心得、修改教学心得。系统管理员负责对网站页面的维护、审核不合法课件和不合法教学信息、批准用户注册。











## Welcome to GitHub Pages

You can use the [editor on GitHub](https://github.com/LTF3344/LiTengaFei20182123054/edit/gh-pages/index.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/LTF3344/LiTengaFei20182123054/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
