## usage

### cmd

```sh
gitbook -h

gitbook init

gitbook serve

gitbook build
```

### config

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
        "donate",
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
            "url": "https://github.com/magicbowen"
        },
        "code": {
            "copyButtons": true
        },
        "tbfed-pagefooter": {
            "copyright": "Copyright © bowen 2019",
            "modify_label": "本书发布时间：",
            "modify_format": "YYYY-MM-DD HH:mm:ss"
        },
        "donate": {
            "wechat": "/assets/images/wxpay.png",
            "alipay": "/assets/images/alipay.png",
            "title": "",
            "button": "赏",
            "alipayText": "支付宝打赏",
            "wechatText": "微信打赏"
        },
        "sharing": {
            "facebook": true,
            "twitter": true,
            "weibo": true,
            "qq": true,
            "all": [
                "douban",
                "google",
                "qzone",
                "linkedin"
            ]
        },
        "prism": {
            "css": [
                "prismjs/themes/prism-solarizedlight.css"
            ],
            "lang": {
                "flow": "typescript"
            }
        }
    },
    "styles": {
        "website": "assets/styles/website.less",
        "ebook": "assets/styles/ebook.less",
        "pdf": "assets/styles/pdf.less",
        "mobi": "assets/styles/mobi.less",
        "epub": "assets/styles/epub.less"
    }
}
```

### cover

gitbook 的封面可以通过插件auto cover自动生成，也可以自己配置。

如果要使用自定义的封面，在书籍的根目录下放置 cover.jpg，如果想要缩略图可以放置 cover_small.jpg，文件格式必须为 jpg。

一个好的封面需要:

大小要求 cover.jpg 1800x2360 pixels , cover_small.jpg 200x262
不要有边框
有清晰的标题
任何小的标题需要清晰可见

### versions

```sh
gitbook ls-remote
```