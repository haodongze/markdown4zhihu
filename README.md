# markdown4zhihu
将Markdown文件一键转换为知乎编辑器支持模式

## 使用方法
首先，您应当仿照本仓库建立一个类似的您自己的仓库，它包括一个Data文件夹与根目录下的zhihu-publisher.py。当然，您也可以选择直接folk本仓库到您自己的账号下。

然后，打开zhihu-publisher.py文件，在文件开头有这么一句：GITHUB_REPO_PREFIX = "https://raw.githubusercontent.com/miracleyoo/Markdown4Zhihu/master/Data/"请修改miracleyoo为您自己的GitHub用户名，如果仓库名字也有变化，请做出相应微调。

这里我们假设您的文件名为一个测试文档.md，并将其和同名图片文件夹放到Data目录下，接着打开terminal(Linux/MacOS)或Git Bash(Windows)(或其他任何支持Git命令的终端)，输入以下命令：

python zhihu-publisher.py --input="./Data/一个测试文档.md"

OK，all set. 在Data目录下，你可以看到一个一个测试文档_for_zhihu.md的文件，将它上传至知乎编辑器即可。
