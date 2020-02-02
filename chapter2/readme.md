## usage

### create

创建一个目录，在下面创建`README.md`和`SUMMARY.md`；

- README.md : 书的介绍，可以随便写
- SUMMARY.md : 书的目录，具体格式参照本文档的`SUMMARY.md`

创建好之后，运行`gitbook init`，会自动按照`SUMMARY.md`中的描述，生成各个章节对应的目录和文档名。如果目标文件已经存在不会覆盖。

### config

书的根目录下的`book.json`可以用来配置书的元信息以及插件。
`book.json`中配置的插件需要提前装好，关于插件的安装在下一章。

book.json example:

```json
{
    "title": "gitbook example",
    "description": "Tutorial of Gitbook",
    "author": "Bowen",
    "output.name": "site",
    "language": "zh-hans",
    "gitbook": "3.2.3",
    "root": ".",
    "links": {
        "sidebar": {
            "博客": "https://www.jianshu.com/u/92b7d9879f20"
        }
    },
    "plugins": [
        "code",
        "-search",
        "search-pro",
        "-github",
        "splitter",
        "tbfed-pagefooter",
        "-donate",
        "-sharing",
        "sharing-plus",
        "prism",
        "-highlight",
        "styles-less",
        "toggle-chapters",
        "multipart",
        "ancre-navigation"
    ],
    "pluginsConfig": {
        "github": {
            "url": "https://github.com/ccock"
        },
        "code": {
            "copyButtons": true
        },
        "tbfed-pagefooter": {
            "copyright": "Copyright © CCOCK 2020",
            "modify_label": "本书发布时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "prism": {
            "css": [
                "prismjs/themes/prism-dark.css"
            ],
            "lang": {
                "flow": "typescript"
            }
        }
    }
}
```

`plugins`中配置了所有插件，暂时不使能的前面加`-`。
`pluginsConfig`中是插件的配置。

### cmd

```sh
# help
gitbook -h

# init a book
gitbook init

# run local http server for book review
gitbook serve

# build book
gitbook build
```

`gitbook serve` 和`gitbook build`命令会检查配置的每个插件是否都已安装。
插件的安装见下章。

`gitbook serve`会将书默认以HTTP的方式发布在本机4000端口，可以打开浏览器查看书的内容。

### cover

gitbook 的封面可以通过插件auto cover自动生成，也可以自己配置。

如果要使用自定义的封面，在书籍的根目录下放置 cover.jpg，如果想要缩略图可以放置 cover_small.jpg，文件格式必须为 jpg。

一个好的封面需要:

大小要求 cover.jpg 1800x2360 pixels , cover_small.jpg 200x262
不要有边框
有清晰的标题
任何小的标题需要清晰可见
