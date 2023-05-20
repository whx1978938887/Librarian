## 项目概述
图书馆管理系统是图书馆管理员用于管理图书馆相关业务的管理系统。本系统包含的功能有书籍搜索、借阅记录、发起订单、借阅管理、订单管理、书籍管理、用户管理和角色管理。该项目图书馆管理系统的后台。 
图书馆管理系统的前端项目下载：[点击此处](https://github.com/whx1978938887/Librarian-page)

## 功能概述
书籍搜索：用户对图书馆中具有的图书按条件进行搜索，对查询的图书可以发起借阅，然后等待管理员的审核。  
借阅记录：用户在书籍搜索中借阅的记录可以在此处进行查看，对借阅的图书可以进行归还操作。  
发起订单：用户通知发起订单，通知系统管理员需要在系统中上架的图书，然后等待管理员的审核情况。  
借阅管理：分为审核和修改两大子模块。审核是同意或者撤销来自用户的借阅或归还申请，而修改则是修改借阅记录的具体信息。  
订单管理：分为审核和修改两大子模块。审核是同意或驳回来自用户的订单请求，而修改则是修改订单的具体信息。  
书籍管理：管理员在此处对书籍搜索中的图书信息进行修改。  
用户管理：管理员修改用户承担的角色。  
角色管理：管理员修改系统的角色信息，包括对角色信息的增删改查操作。  

## 部分功能展示
书籍搜索  
[![p959e7n.png](https://s1.ax1x.com/2023/05/20/p959e7n.png)](https://imgse.com/i/p959e7n)
借阅管理  
[![p959nkq.png](https://s1.ax1x.com/2023/05/20/p959nkq.png)](https://imgse.com/i/p959nkq)
书籍管理  
[![p959ut0.png](https://s1.ax1x.com/2023/05/20/p959ut0.png)](https://imgse.com/i/p959ut0)
用户管理  
[![p959Vmj.png](https://s1.ax1x.com/2023/05/20/p959Vmj.png)](https://imgse.com/i/p959Vmj)
角色管理  
[![p959Z0s.png](https://s1.ax1x.com/2023/05/20/p959Z0s.png)](https://imgse.com/i/p959Z0s)

## 系统架构
系统采用Vue+SpringBoot的前后端分离架构开发。系统后台使用的技术有：  
1.SpringBoot  
2.Spring Security  
2.MySQL  
3.Redis  
4.RabbitMQ  
5.Swagger2  


## 项目运行
前置说明：系统运行需要MySQL、Redis和RabbitMQ中间件环境，需要自行搭建。

### 1.项目下载/克隆  
在项目需要保存的路径下，使用git命令`git clone https://github.com/whx1978938887/Librarian-server.git .`将项目克隆到本地  
或者在github直接下载Zip文件到本地进行解压   

### 2.创建数据库  
项目使用flyway数据库版本管理，创建数据库即可，数据库表会在项目首次运行时自动创建。

### 3.修改配置  
将application.yml中中间件的地址和端口修改为自己运行的地址和端口，若Redis、Rabbit和MySQL是在本地运行，将地址改为localhost即可。修改数据库名称，并将数据库的用户名和密码修改为自己的用户名和密码。配置邮箱验证的公用邮箱，并配置授权码。

### 4.项目运行
运行LibrarianApplication类，项目开始运行。

> 初始管理员用户名为zhangsan，密码为1234