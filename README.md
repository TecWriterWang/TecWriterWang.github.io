# http://TecWriterWang.github.io #blog地址
# 安装步骤如下
## 先下载hugo安装包，直接在github可以下载最新的安装包。安装参考:https://gohugo.io/getting-started/

1.下载后解压安装包到任意任意目录。

2.新建hugo文件夹，在该目录下分别新建bin文件夹和Sites文件夹，将解压后的文件复制到bin目录下。

3.配置path路径，将bin目录路径添加到系统变量的path下。设置完成后，可通过cmd命令：hugo version 查看是否配置好，配置完成后会显示hugo版本。

4.创建新的bolg文件夹，通过cmd命令进入Sites文件夹，使用 hugo new site 文件夹 命令在Sites目录下创建一个blog文件夹。

5.新建一个blog文章。cmd先进入新建的blog文件夹中，使用hugo new flodr/file.md 创建一个md文件（使用flodr/file.md 表示在post目录下新建一个file.md文件，新建的folder文件夹默认存储在新建的blog文件夹下的content文件夹内）
  ```
  打开file.md会看到 两条 --- 间的信息是文章的配置信息，有的信息是自动生成的 (如：title、date 等)，简单介绍以下各项配置
  以下项目是自动生成的:
  title: # 文章标题
  date: # 写作时间
  draft: # 是否为草稿，如果为 true ,则需要在cmd命令中加入 --buildDrafts 参数才会生成这个文档，改为false，就不需要
  以下项目需要自行添加:
  description: # 描述
  tags: # 标签，用于文章分类
  自动生成 和 执行添加 的内容并不是绝对的
  ```
6.下载theme，theme地址链接：https://github.com/gohugoio/hugoThemes ，然后在hugo的github官网找到想要的theme，然后复制其链接，在cmd中先进入themes文件夹，然后使用git clone 主题的网址，例如git clone https://github.com/orianna-zzo/AllinOne.git  即可自动下载AllinOne主题。（下载完成后现将下载的主题文件夹名更改成主题名字，有些下载的主题文件夹会自动带上hugo）

7.github的pages设置，新建一个仓库命名为自己的username.github.io 并设置github pages（这一步可以使仓库直接作为网页来访问，）将生成的网址复制到config.toml文件中 的baseurl。

8.配置config.toml文件，使用vscode打开该文件，将github生成的网址复制到（baseurl：）项目后，（theme：）填写主题文件夹名称，其他的自行参考官网文档。
9.cmd 使用hugo server -t themename 可以自定义主题，只可以可以在本地地址1313访问新建的.md blog。关闭hugo server后就不能继续访（必须先将新建的blog先打开设置表头，将draft设置为 false，这一步是不将blog设置为草稿）。

10.若在网页1313上访问到blog，则会在blog文件夹下生成public文件夹。若想在远程也访问，只需在public文件夹下运行git bash ，将public文件夹设为git本地仓库，最后再与github的对应仓库远程连接，就实现了github+hugo组成的一个个人网页blog，config.toml，配置用于blog网页排版，涉及的内容较多，需要查看文档以了解具体语法。
