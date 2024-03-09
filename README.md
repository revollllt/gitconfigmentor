创建新github仓库

1.本地ssh:
windows下：c:/user/user/.ssh
linux下：~/.ssh
若文件夹中有id_rsa和id_rsa.pub则跳到下一步
若无则
ssh-keygen -t rsa -C "你的邮箱名"
执行后会生成.ssh以及其中的id_rsa和id_rsa.pub

2.github个人ssh
在setting中点击左侧SSH and GPG keys
后点击 New SSH key
将id_rsa.pub中内容复制到Key中，title随便填，然后点击Add SSH key

3.github新建仓库
点击右上角十字后点击New repository
输入仓库名，public和private按要求填
点击最后的Create repository

4.本地仓库(按照Create repository后弹出的网页教程操作，注意一定要确认第2步完成)：
git init
如果没config过的话，name和email没有要求，可随便填
git config --global user.name "your name"
git config --global user.email "your email"
git add .
git commit -m "your commit name"
git remote add origin git@github.com:your_github_name/your_repository_name.git
git push --set-upstream origin master 