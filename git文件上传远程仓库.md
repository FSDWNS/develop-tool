## 使用git文件上传本地文件夹到github

> ###### 第一步，首先在github上面新建一个仓库，用来存放文件。

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G7.PNG)

> ###### 第二步，将git远程仓库文件拉取到本地。

###### git clone “链接”

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G1.PNG)

###### 就是图中选中的地址。

###### 然后在你的任意盘新建一个文件夹，并在文件夹下打开git bash，（PS:没安装gitbash的要安装gitbash,如果安装完成，点击鼠标右键可显示git bash here和git GUI here）。

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G2.PNG)

###### clone后你会发现生成一个文件夹，里面有README.md和.git文件。

> ###### 第三步，切到文件夹下面

###### 由于我在github上面新建了一个文件夹demo1。此时我要上传文件夹，我需要切换到demo1文件夹下。这个无所谓，如果你没有新建，直接上传文件夹也行，这一步就略过。

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G3.PNG)

> ###### 第四步，使用git add . 添加你的文件夹

###### 注意，这里的add后面空格再一个小点，add.不识别命令，我仿的是一个云播网页，直接拷贝到demo1下面。

![G5](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G5.PNG)

> ###### 第五步，使用git commit -m '  提交信息，随便写    '

> ###### 第六步，使用git push  -u origin xxx推送到远程仓库，master是由于本地仓库与远程仓库的分支关联。

![G6](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G6.PNG)

###### git命令就三句。

```
git add . 
git commit -m '  提交信息，随便写'
git push  -u origin xxx
```

> ###### 看github仓库是否上传成功以及目录

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G8.PNG)

###### 以上就是将本地文件夹推送到远程仓库的基本步骤。有时或许要初始化，但是我省略了这一步，也没有出现问题，git还需要更多的学习。

#### 需要注意的问题：

###### 有的时候每次提交都需要输入用户名和邮箱，所以我建议配置ssh密钥，这样就省得每次登陆验证。

```csharp
git config --global user.name “用户名”
git config --global user.email “邮箱”
```

###### 然后接着输入

```
ssh-keygen -t rsa -C "你的邮箱"
```

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G4.PNG)

###### 然后再你的用户名文件夹下有个.ssh文件夹打开，将id_rsa.pub复制到github下面的SSH keys下面。

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G11.PNG)

![](C:\Users\18522\Desktop\md\dahuashujujiegou_downcc\G10.PNG)

###### 添加后会出现钥匙的形状。

###### 还有一个问题就是我在github上面新建文件夹，因为它上面新建文件夹必须要有文件，因此我新建了README.md问价，我现在不需要了，需要删除它。

```
git rm 文件名
```

###### 个人不建议在github上面建文件夹，直接在本地调整好目录结构即可。

###### 以上就是我上传本地文件的过程，还是要学好linux shell啊，真的很有用，作为刚入门的小白来讲，有时候很容易忘记一些东西，所以写写文档，加强记忆。