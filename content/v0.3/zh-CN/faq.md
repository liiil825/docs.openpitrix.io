---
title: "常见问题"
---

1、作为新手，如何从一个最简单的例子入手？
我们提供了一个如何准备一个基于 OpenPitrix 应用开发规范的示例，建议从 [ WordPress 实战](openpitrix-developer-quick-start/#wordpress-实战) 入手，从零开始准备一个配置包并上传到 OpenPitrix 中，后续可参考 [用户指南](../user-guide) 熟悉应用的全生命周期管理。

2、应用如何语言国际化？
如果您想要适应不同的语言，需要在提交的应用中包含一个 locale 文件夹，并添加对应语言的翻译文件，如：

- locale/en.json 英文翻译文件
- locale/zh-cn.json 中文翻译文件

具体配置请参考文档 [国际化](../openpitrix-specification/#国际化) 。

3、上传配置包或新的版本时报错：配置验证失败，报 “创建资源失败” 错误？
需要检查 package.json 或 config.json 文本内容，是否有中文符号或其他不符合 json 格式的部分，可以通过在线工具验证合法性，比如 jsonlint。 

如果报 “应用名称已存在” 或 “应用版本已存在” ，则需要修改配置文件（package.json 或 Chart.yaml）的应用名称或版本号。版本号匹配应用配置包中配置文件的 `version` 字段，配置文件中的 `version` 字段的值（版本号）不能与该应用已上传的版本号重复，且应用名 (`name` 字段的值) 不能与仓库中的已有应用的名称重复，修改后重新生成一个配置包即可上传成功。

如果有其他疑问，您也可以通过提问形式与我们联系探讨。