[English](readme.md) | **中文**

\>\>\> [回到索引](/readme-zh_cn.md)

## qq_chat

### 基本信息

- 插件 ID: `qq_chat`
- 插件名: QQChat
- 版本: 1.0.0
  - 元数据版本: 1.0.0
  - 发布版本: 1.0.0
- 总下载量: 27
- 作者: [Andy Zhang](https://github.com/AnzhiZhang)
- 仓库: https://github.com/AnzhiZhang/MCDReforgedPlugins
- 标签: [`信息`](/labels/information/readme-zh_cn.md), [`管理`](/labels/management/readme-zh_cn.md)
- 描述: QQ 相关实用功能

### 插件依赖

| 插件 ID | 依赖需求 |
| --- | --- |
| [qq_api](/plugins/qq_api/readme-zh_cn.md) | ^1.0.0 |
| [online_player_api](/plugins/online_player_api/readme-zh_cn.md) | ^1.0.0 |

### 包依赖

| Python 包 | 依赖需求 |
| --- | --- |
| [aiocqhttp](https://pypi.org/project/aiocqhttp) |  |

### 介绍

# QQChat

> 用于连接 `Minecraft` 和 `QQ` 的插件

## 配置

`groups`

默认值: `[1234561, 1234562]`

交互的群组列表

`admins`

默认值: `[1234563, 1234564]`

可以私聊执行管理员指令的qq号

`whitelist_add_with_bound`

默认值: `False`

玩家绑定游戏ID时添加白名单

`whitelist_remove_with_leave`

默认值: `True`

玩家退群时移除白名单

`forwards`

默认值: `{'mc_to_qq': False, 'qq_to_mc': False}`

设置是否自动在 Minecraft 和 QQ 之间转发消息

`commands`

默认值: `{'list': True, 'mc': True, 'qq': True,}`

设置是否启用命令

## 功能

### 普通玩家命令

`/help` 查看帮助

`/list` 获取在线玩家列表

`/bound <ID>` 绑定你的游戏ID

`/mc <msg>` 向游戏内发送消息

`!!qq <msg>` 向qq群发送消息

需要注意普通玩家只能在群里执行指令，而管理可以私聊执行 `/list` 和 `/mc`

### 管理员命令

管理员命令只能私聊机器人执行, 管理员QQ号需要添加到配置文件中

#### 基础帮助

`/help` 查看帮助

`/bound` 查看绑定相关帮助

`/whitelist` 查看白名单相关帮助

`/command <command>` 执行任意指令

#### 绑定相关

`/bound list` 查看绑定列表

`/bound check <qq number>` 查询绑定ID

`/bound unbound <qq number>` 解除绑定

`/bound <qq number> <ID>` 绑定新ID

#### 白名单相关

`/whitelist add <target>` 添加白名单成员

`/whitelist list` 列出白名单成员

`/whitelist off` 关闭白名单

`/whitelist on` 开启白名单

`/whitelist reload` 重载白名单

`/whitelist remove <target>` 删除白名单成员

`<target>` 可以是玩家名/目标选择器/UUID

### 下载

> :warning: 注意：使用插件之前，先阅读仓库中的 README。

| 文件 | 版本 | 上传时间 | 大小 | 下载数 | 操作 |
| --- | --- | --- | --- | --- | --- |
| [QQChat-v1.0.0.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/qq_chat-v1.0.0) | 1.0.0 | 2023/02/03 22:36:22 | 3.36KB | 27 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/qq_chat-v1.0.0/QQChat-v1.0.0.mcdr) |

