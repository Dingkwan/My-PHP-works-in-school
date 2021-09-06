# Forum_PHP

## 将forum文件放入phpStudy（或具有类似功能的应用）的WWW目录（或具有类似功能的目录）内，再将forum.sql导入到MySQL中即可使用

管理员账号：admin &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; 密码：admin

### 主要功能：
- **登录、注册**
> 分析：用户首先点击页面上方的“登录/注册按钮”进入登录/注册界面，若此时用户尚未拥有账号，可以点击页面下部的“注册”按钮进入注册界面，填写相关信息后，系统会将新用户的信息提交到数据库的user表中，随后用户会被重定向至登录界面，此时用户通过自己的账号密码登录系统。在用户提交了账号和密码字段后，系统会将这两个字段和数据库user表内的数据比较，若匹配成功则允许登录，若不成功则拒绝登录。


- **发帖功能**
> 分析：论坛主页面单击“发帖按钮”后会进入发帖界面，在发帖界面输入相关信息（如标题，类型，正文）后，系统会将相关信息提交到数据库的message表中。随后用户会被重定向到论坛主页面。


- **回复功能**
> 分析：在用户登录了系统的情况下（不登录系统无法使用回复功能），在帖子内容下方的“我的回复”输入框中输入回复，在用户点击“回复”按钮后系统会将回复内容提交到数据库中的reply_message表中。随后用户会被重定向到帖子界面，此时用户可以看到自己刚刚发送的回复。


- **删除帖子功能**
> 分析：用户可以在个人信息界面点击“删除我的帖子”按钮（管理员也可点击“删除帖子”删除论坛上的任一帖子），随后会进入选择帖子界面，界面显示了用户发过的所有帖子，用户选择一张帖子后点击页面下方的“删除”按钮，系统会将删除帖子的语句和删除帖子下回复的语句提交到数据库，实现删除帖子和帖子下回复的功能。随后用户被重定向到删除帖子界面，方便用户的下个删除操作。


- **修改帖子功能**
> 分析：用户在个人信息“点击修改个人信息”按钮后会进入选择要修改的帖子界面，用户选择了要修改的帖子后进入修改帖子的界面，系统会从数据库将这个帖子的原本信息读出来作为输入框的默认值，用户提交修改后系统会将更新后的信息提交到数据库覆盖以前的信息。值得一提的是，若用户更改了帖子的标题，这条帖子下的回复的标题（表reply_message的titile字段的值）也会同步更改。


- **删除回复功能**
> 分析：用户可以在个人信息界面点击“删除我的回复”按钮（管理员也可点击“删除回复”删除论坛上的任一回复），随后会进入选择回复界面，界面显示了用户发过的所有回复，用户选择一张回复后点击页面下方的“删除”按钮，系统会将删除回复的语句提交到数据库，实现删除回复的功能。随后用户被重定向到删除回复界面，方便用户的下个删除操作。


- **修改个人信息功能**
> 分析：用户在个人信息点击界面点击“修改个人信息”后，进入修改信息界面，点击更新后系统会将更新提交到数据库，数据库更新自己的user表中的信息。随后用户被重定向至个人信息界面。


- **查看所有用户信息（管理员功能）**
> 分析：在个人信息界面点击“查看所有用户信息”，系统会访问数据库的user表，将表内的数据全部返回至页面。
