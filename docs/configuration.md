---
title: "第 3 节 配置: 使用 GlotPress 前需要检查的一些配置项"
post_status: publish
post_name: configuration
lang: zh
taxonomy:
  category: [glotpress]
  post_tag: [gp-start]
source:
  blog_id: 61
  post_id: 9
  guid: "https://wpwenku.com/glotpress/?p=9"
---

### 3.1 配置

安装 GlotPress 后，您必须执行（或之前已执行）的唯一附加步骤是在 WordPress 中配置永久链接。GlotPress 需要朴素“Plain”以外的固定链接设置。
此外，如果您不想通过默认路径 (\glotpress) 访问 GlotPress，您可以通过在wp-config.php文件中添加以下行来更改此设置：
`define('GP_URL_BASE', '');`
您可以替换为任何您喜欢的内容，但请注意选择不会与其他页面或文章发生冲突的内容。
如果您希望从 WordPress 安装的根目录访问 GlotPress，您可以使用：
`define('GP_URL_BASE', '/');`
GlotPress 带有一组默认模板（有点像 WordPress 主题）用于生成它的页面。您可以创建自己的自定义模板，但是您不能将它们存储在插件目录中，否则它们将在您安装的下一次 GlotPress 升级时被覆盖。相反，在您的站点中的其他位置创建一个目录并将模板存储在那里，然后将以下行添加到您的wp-config.php文件中：
`define( 'GP_TMPL_PATH', '/var/www/example.org/gp-templates' );`
