# <http://TecWriterWang.github.io>

# 安装步骤如下

## 先下载hugo安装包，直接在github (https://github.com/gohugoio/hugo/releases) 可以下载最新的安装包。安装参考: https://gohugo.io/getting-started/

1. 下载压缩包后解压到任意目录。

2. 在你准备运行Hugo的位置新建Hugo文件夹，在新建的Hugo目录下分别新建bin文件夹和Sites文件夹，将解压后的所有文件复制到bin目录下。

3. **配置PATH路径**。将bin目路的径添加到系统变量的PATH下。设置完成后，打开cmd命令行运行下面的命令来查看是否配置好，若配置成功后则会显示hugo版本。

    ```cmd
    hugo version
    ```

4. **创建新的bolg文件夹**。通过cmd命令进入Sites文件夹，使用下面的命令在Sites目录下创建一个blog文件夹。

    ![新建文件夹](https://raw.githubusercontent.com/TecWriterWang/TecWriterWang.github.io/master/%E6%96%B0%E5%BB%BA%E4%B8%80%E4%B8%AABlog%E6%96%87%E4%BB%B6%E5%A4%B9.png)

    ```cmd
    cd Sites文件夹位置
    hugo new site filename(文件夹名)
    ```

5. **新建一个blog文章**。cmd先进入新建的blog文件夹中，使用下面命令创建一个md文件（使用floder/file.md 表示在post目录下新建一个file.md文件，新建的folder文件夹默认存储在新建的blog文件夹下的content文件夹内）

    ![文章](https://github.com/TecWriterWang/TecWriterWang.github.io/blob/master/%E5%9C%A8Blog%E7%9B%AE%E5%BD%95%E4%B8%8B%E6%96%B0%E5%BB%BA%E4%B8%80%E4%B8%AAmd%E6%96%87%E4%BB%B6.png)

      ```cmd
      hugo new floder/file.md
      ```

      ```content guide
      打开file.md会看到 两条 --- 间的信息是文章的配置信息，有的信息是自动生成的 (如：title、date 等)，简单介绍以下各项配置,以下项目是自动生成的:
        title: # 文章标题
        date: # 写作时间
        draft: # 是否为草稿，如果为 true ,则需要在cmd命令中加入 --buildDrafts 参数才会生成这个文档，改为false，就不需要以下项目需要自行添加.
        description: # 描述
        tags: # 标签，用于文章分类
      ```

6. 下载theme，theme地址链接：<https://github.com/gohugoio/hugoThemes> ，然后在hugo的github官网找到想要的theme，然后复制其链接，在cmd中先进入themes文件夹，然后使用下面命令，即可自动下载AllinOne主题。（下载完成后现将下载的主题文件夹名更改成主题名字，有些下载的主题文件夹会自动带上hugo）git clone https://github.com/orianna-zzo/AllinOne.git

    ![theme](https://github.com/TecWriterWang/TecWriterWang.github.io/blob/master/%E4%B8%8B%E8%BD%BDblog%E7%9A%84%E4%B8%BB%E9%A2%98.png)

    ```cmd
    cd themes文件夹地址
    git clone URL
    ```

7. github的pages设置，新建一个仓库命名为自己的username.github.io 并设置github pages（这一步可以使仓库直接作为网页来访问，）将生成的网址复制到config.toml文件中 的baseurl。

8. 配置config.toml文件，使用vscode打开该文件，将github生成的网址复制到（baseurl：）项目后，（theme：）填写主题文件夹名称，默认情况下会有draft，将其改为false，或者直接删除。其他属性的自行参考官网文档。（**可以直接将下载的themes中examplesite文件夹下config.toml复制到网站根目录下。**）

9. cmd进入到该blog根目录下，将主题应用到网站并且可以查看，只能在本地地址1313访问新建的.md blog。关闭hugo server后就不能继续访（必须先将新建的blog先打开设置表头，将draft设置为 false，这一步是不将blog设置为草稿）。

    ![hugo](https://github.com/TecWriterWang/TecWriterWang.github.io/blob/master/%E5%B0%86blog%E7%9A%84%E4%B8%BB%E9%A2%98%E6%8E%A8%E9%80%81%E5%88%B0%E6%9C%AC%E5%9C%B0.png)

    ```cmd
    cd C:\Hugo\Sites\Test-blog
    hugo server -t themename
    ```

10. 还是在网站根目录下，cmd运行hugo，则会在blog文件夹下生成public文件夹。若想在远程也访问，只需在public文件夹下运行git bash，（参考<https://github.com/TecWriterWang/git/blob/master/readme.txt>）将public文件夹设为git本地仓库，最后再与github的对应仓库远程连接，就实现了github+hugo组成的一个个人网页blog。

11. blog目录下的config.toml，配置用于blog网页排版，涉及的内容较多，需要查看文档以了解具体语法。

