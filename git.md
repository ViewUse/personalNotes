# github ssh key
## 生成 ssh key
- 打开github,点击头像下拉框
- 点击**Settings**选项
- 点击页面左侧 **SSH and GPG keys** 选项
- 点击页面右侧*小字体* **generating SSH keys**
- 选中 **Generating a new SSH key and adding it to the ssh-agent**选项
- 复制提示的命令到系统的gitBash中执行,按提示走完
- 最后在GitBash中输入命令: cat directory/.ssh/id_rsa.pub, 出现一串字母，复制它
- 回到**SSH and GPG keys** 页面,点击右上角的 **New SSH key** 按钮
- 填上标题，粘贴刚才复制的一串字母到 *key* 栏中，点击 **add SSH key** 按钮,如不出意外,此时将创建成功

## 本地repository 与 github-repository 关联
- github **new repository**
- 填上相应信息得到 SSH 地址,如:git@github.com:user/test.git
- 在本地执行以下命令
```shell
    mkdir test & cd test
    echo "# my-blog" >> README.md
    git init
    git add README.md
    git commit -m "first commit"
    git remote add origin git@github.com:user/test.git
    git push -u origin master //向github推送数据
    git pull origin master //从github拉数据下来
```

## git 命令
```shell
    git config -l //查看git global配置信息
```