## plugin

### 常用插件列表:
- back-to-top-button（返回顶部）
- code（代码添加行号&复制按钮）
- search-pro（高级搜索，支持中文）
- github（在右上角添加github图标）
- splitter（侧边栏宽度可调节）
- tbfed-pagefooter（页面添加页脚，简单的）
- page-copyright（页面页脚版权，复杂的）
- donate（打赏插件）
- sharing-plus（分享当前页面）
- custom-favicon（修改标题栏图标）
- prism（代码高亮）
- todo（复选框）
- pageview-count（阅读量计数）
- auto-scroll-table（表格滚动条）
- image-captions（显示图片名称）
- styles-sass（使用sass替换css）
- styles-less（使用less替换css）
- toggle-chapters（目录折叠）
- multipart（分章节展示）

### config plugin

在`book.json`对应的位置增加插件和插件配置：

```json
{
    "plugins": [
        "code"
    ],
    "pluginsConfig": {
        "code": {
            "copyButtons": false
        }
    }
}
```

### install plugins

以下三种方法皆可：

- 配置book.json, 然后`gitbook install`

- 使用npm安装，命令格式`npm install gitbook-plugin-插件名字`，如`npm install gitbook-plugin-code`

- 从GitHub下载源码，放到`node_modules`文件夹里
