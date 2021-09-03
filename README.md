# Forum_PHP

## 将forum文件放入phpStudy（或具有类似功能的应用）的WWW目录（或具有类似功能的目录）内，再将forum.sql导入到MySQL中即可使用

管理员账号：admin &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 密码：admin

### 主要功能：
- **登录、注册**
> 分析：用户首先点击页面上方的“登录/注册按钮”进入登录/注册界面，若此时用户尚未拥有账号，可以点击页面下部的“注册”按钮进入注册界面，填写相关信息后，系统会将新用户的信息提交到数据库的user表中，随后用户会被重定向至登录界面，此时用户通过自己的账号密码登录系统。在用户提交了账号和密码字段后，系统会将这两个字段和数据库user表内的数据比较，若匹配成功则允许登录，若不成功则拒绝登录。


- **发帖功能**
> 分析：论坛主页面单击“发帖按钮”后会进入发帖界面，在发帖界面输入相关信息（如标题，类型，正文）后，系统会将相关信息提交到数据库的message表中。随后用户会被重定向到论坛主页面。