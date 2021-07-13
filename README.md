# markdown4zhihu
将Markdown文件一键转换为知乎编辑器支持模式

## 使用方法
1. 首先，您应当仿照本仓库建立一个类似的您自己的仓库，它包括一个Data文件夹与根目录下的zhihu-publisher.py。当然，您也可以选择直接folk本仓库到您自己的账号下。

然后，打开zhihu-publisher.py文件，在文件开头有这么一句：GITHUB_REPO_PREFIX = "",需要将其修改为github图片文件夹所在的地址。

这里我们假设您的文件名为一个测试文档.md，并将其和同名图片文件夹放到Data目录下，接着打开terminal(Linux/MacOS)或Git Bash(Windows)(或其他任何支持Git命令的终端)，输入以下命令：

python zhihu-publisher.py --input="./Data/一个测试文档.md"

OK，all set. 在Data目录下，你可以看到一个一个测试文档_for_zhihu.md的文件。
2. 现在需要将Data下的图片文件夹和markdown文件（可选）同步到github种。
