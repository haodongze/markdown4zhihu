# markdown4zhihu
将Markdown文件一键转换为知乎编辑器支持模式

## 使用方法

### 改变markdown的格式
1. 首先，您应当仿照本仓库建立一个类似的您自己的仓库，它包括一个Data文件夹与根目录下的zhihu-publisher.py。当然，您也可以选择直接folk本仓库到您自己的账号下。

2. 然后，打开zhihu-publisher.py文件，在文件开头有这么一句：GITHUB_REPO_PREFIX = "",需要将其修改为github图片文件夹所在的地址。

3. 这里我们假设您的文件名为一个测试文档.md，并将其和同名图片文件夹放到Data目录下，接着打开terminal(Linux/MacOS)或Git Bash(Windows)(或其他任何支持Git命令的终端)，输入以下命令：

python zhihu-publisher.py --input="./Data/一个测试文档.md"

4. OK，all set. 在Data目录下，你可以看到一个测试文档_for_zhihu.md的文件，在GitHub同步后将其上传到知乎编辑器。

### Github上传
现在需要将Data下的图片文件夹和markdown文件（可选）同步到github中。
1. 安装git软件，可以参考其他教程。
2. 进入仓库所在的文件夹，运行git bash命令（windows用户）。
3. 运行 `git init` 命令。
4. 为了把本地的仓库传到github，还需要配置ssh key。不配置怎么能知道是不是本人或者本人机器呢？（电话线的作用）
   `ssh-keygen -t rsa -C "your_email@youremail.com"`
   直接点回车，说明会在默认文件id_rsa上生成ssh key。 

   然后系统要求输入密码，直接按回车表示不设密码（设置也可以）

   重复密码时也是直接回车，之后提示你shh key已经生成成功。

5. `git config --global user.name "your name"`（代表github用户名）
   `git config --global user.email "your_email@youremail.com"`（github邮箱）
   
6. 进入要上传的仓库，添加远程地址
   `git remote add origin git@github.com:XyJianChen/xy.git`

7. 上传到github
   `git add -A` (添加到缓存区)

   `git commit -m "first commit"`(提交到仓库)

   `git push origin master` (将本地仓库推送到远程服务器github上)
