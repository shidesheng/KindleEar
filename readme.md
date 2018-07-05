Readme of english version refers to [Readme_EN.md](https://github.com/cdhigh/KindleEar/blob/master/readme_EN.md)

# 简介
这是一个运行在Google App Engine(GAE)上的Kindle个人推送服务应用，生成排版精美的杂志模式mobi/epub格式自动每天推送至您的Kindle或其他邮箱。

此应用目前的主要功能有：  

* 支持类似Calibre的recipe格式的不限量RSS/ATOM或网页内容收集
* 不限量自定义RSS，直接输入RSS/ATOM链接和标题即可自动推送
* 多账号管理，支持多用户和多Kindle
* 生成带图的杂志格式mobi或带图的有目录epub
* 自动每天定时推送
* 强大而且方便的邮件中转服务
* 和Evernote/Pocket/Instapaper等系统的集成

> 注：如果您要求不高，自定义RSS推送功能足以应付一般应用，如果要求排版和完美，可以参照books目录下的文件范本自己添加一个文件再重新上传即可，books目录下的书籍文件都不是随意预置的，每个文件都至少演示一个适用的books编写技巧。
在您懂python的前提下，您可以完全的操控网页，可以生成您需要的最完美的MOBI/EPUB文件。

# 标准部署步骤
1. [申请google账号](https://accounts.google.com/SignUp) 并暂时 [启用不够安全的应用的访问权限](https://www.google.com/settings/security/lesssecureapps) 以便上传程序。  

2. [创建一个Application](https://console.developers.google.com/project)，注意不用申请GCE，那个是60天试用的，而GAE是限额范围内永久免费的。  

3. 安装 [Python 2.7.x](https://www.python.org/downloads/)。  

4. 安装 [GAE SDK](https://cloud.google.com/appengine/downloads)。  

5. 下载 [KindleEar](https://github.com/cdhigh/KindleEar/archive/master.zip) ，解压到一个特定的目录。

6. 在以下三个文件中修改一些参数：  

  文件              |  待修改内容  | 说明                   |  
-------------------|-------------|-----------------------|  
app.yaml           | application | 你的ApplicationId      |  
module-worker.yaml | application | 你的ApplicationId      |  
config.py          | SRC_EMAIL   | 创建GAE工程的GMAIL邮箱   |  
config.py          | DOMAIN      | 你申请的应用的域名        |  

执行upload.sh
