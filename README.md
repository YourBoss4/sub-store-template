# sub-store-template
#Sub-Store #sing-box #singbox #配置 #示例

🔗 Sub-Store 文件动态生成 📦 sing-box 配置示例

🆕 新增远程脚本链接 可配置参数自定义将哪些节点插入哪些 outbound 中, 增加了详细日志, 可查看规则解析结果和整体流程

💃 亚托莉佬的模板和远程脚本 https://github.com/xishang0128/sub-store-template

远程文件填 链接1 https://raw.githubusercontent.com/xishang0128/sub-store-template/main/sing-box.json
或  链接2 https://raw.githubusercontent.com/xishang0128/sub-store-template/main/sing-box-resolve.json
脚本操作填链接 https://raw.githubusercontent.com/xishang0128/sub-store-template/main/sing-box.js#type=1&name=name // "1" 表示组合订阅, name 为订阅的 "名称", 具体看文件中的说明

如果出现死活无法拉取外部资源的情况 可参考 📦 https://t.me/zhetengsha/1287
修改亚托莉佬示例配置中的外部资源逻辑为 使用 GitHub 加速服务 并 直连

⚠️ 此脚本与此模板配套 如果要用自定义模板/有自定义脚本的需求 可使用👇🏻的方案

1.1 使用远程模板

远程链接 中 第一行为 sing-box 模板文件链接
例: https://a.com/sing-box.tpl.json

1.2 或者使用本地模板
本地文本 中为  sing-box 模板文件的内容

使用脚本操作 填入链接:
https://raw.githubusercontent.com/xream/scripts/main/surge/modules/sub-store-scripts/sing-box/template.js#type=组合订阅&name=机场&outbound=🕳ℹ️all|all-auto🕳ℹ️hk|hk-auto🏷ℹ️港|hk|hongkong|kong kong|🇭🇰🕳ℹ️tw|tw-auto🏷ℹ️台|tw|taiwan|🇹🇼🕳ℹ️jp|jp-auto🏷ℹ️日本|jp|japan|🇯🇵🕳ℹ️sg|sg-auto🏷ℹ️^(?!.*(?:us)).*(新|sg|singapore|🇸🇬)🕳ℹ️us|us-auto🏷ℹ️美|us|unitedstates|united states|🇺🇸

示例表示:
读取 名称为 "机场" 的 组合订阅 中的节点(单订阅不需要设置 type 参数)
把 所有节点插入匹配 /all|all-auto/i 的 outbound 中(跟在 🕳 后面, ℹ️ 表示忽略大小写, 不筛选节点不需要给 🏷 )
把匹配 /港|hk|hongkong|kong kong|🇭🇰/i  (跟在 🏷 后面, ℹ️ 表示忽略大小写) 的节点插入匹配 /hk|hk-auto/i 的 outbound 中
...

⚠️ 如果 outbounds 为空, 自动创建 COMPATIBLE(direct) 并插入 防止报错

可选参数: includeUnsupportedProxy 包含官方/商店版不支持的协议 SSR. 用法: &includeUnsupportedProxy=true 

如果想完全手写 可参考 https://t.me/zhetengsha/1066

❗️ 相关内容

🐱 快速生成 clash.meta(mihomo) 配置示例

📦 动态生成 sing-box 配置

📦 快速生成 sing-box 机场入口+落地节点 代理链 示例

👏 欢迎评论 & 转发(请保留来源)

1⃣折腾啥 👥 频道 | 👥 群组