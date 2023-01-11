[English](readme.md) | **中文**

\>\>\> [回到索引](/readme-zh_cn.md)

## bot

### 基本信息

- 插件 ID: `bot`
- 插件名: Bot
- 版本: 1.0.5
  - 元数据版本: 1.0.5
  - 发布版本: 1.0.5
- 总下载量: 353
- 作者: [Andy Zhang](https://github.com/AnzhiZhang)
- 仓库: https://github.com/AnzhiZhang/MCDReforgedPlugins
- 标签: [`工具`](/labels/tool/readme-zh_cn.md), [`管理`](/labels/management/readme-zh_cn.md)
- 描述: 最好用的地毯模组假人管理器！

### 插件依赖

| 插件 ID | 依赖需求 |
| --- | --- |
| [mcdreforged](https://github.com/Fallen-Breath/MCDReforged) | ^2.6.0 |
| [dict_command_registration](/plugins/dict_command_registration/readme-zh_cn.md) | ^1.0.0 |
| [minecraft_data_api](/plugins/minecraft_data_api/readme-zh_cn.md) | ^1.4 |
| [more_command_nodes](/plugins/more_command_nodes/readme-zh_cn.md) | ^1.1.0 |

### 包依赖

| Python 包 | 依赖需求 |
| --- | --- |

### 介绍

# Bot

> 最好用的地毯模组假人管理器！

## 依赖

- [MinecraftDataAPI](https://github.com/MCDReforged/MinecraftDataAPI)
- [MoreCommandNodes](https://github.com/AnzhiZhang/MCDReforgedPlugins/tree/master/more_command_nodes)

## 使用方法

`!!bot` 查看帮助

`!!bot list [index] [filter]` 显示假人列表

`!!bot spawn <name>` 上线假人

`!!bot kill <name>` 下线假人

`!!bot action <name> [index]` 执行假人动作

`!!bot info <name>` 查看假人信息

`!!bot save <name> [position] [facing] [dimension]` 保存假人

`!!bot del <name>` 删除保存的假人

`!!bot config <name> <option> <value>` 配置假人

```mermaid
sequenceDiagram
    participant Player/Console
    participant Online Bots
    participant Saved Bots

    Player/Console-->>Online Bots: !!bot spawn (player)
    Saved Bots-->>Online Bots: !!bot spawn
    Online Bots-->>Online Bots: !!bot kill
    Online Bots-->>Saved Bots: !!bot save
    Player/Console-->>Saved Bots: !!bot save [location]
    Saved Bots-->>Saved Bots: !!bot del
```

### list

**index**：列表的页码

**filter**：可用选项为：`--all`、`--online` 或 `--saved`，过滤假人

### spawn

上线假人

```mermaid
flowchart TD
    start([list])
    is_saved{Saved?}
    is_player{Running by Player?}

    start --> is_saved
    is_saved -->|Yes| spawn1(Spawn at Saved Location)
    is_saved -->|No| is_player
    is_player -->|Yes| spawn2(Spawn at player's Location)
    is_player -->|No| error1([Not Saved Error])
```

### kill

下线假人

### action

执行假人动作

当指定 `index` 时，执行特定动作而不是全部动作

### info

查看假人信息

### save

保存假人

```mermaid
flowchart TD
    start([save])
    with_location{Has Location?}
    online{Online or Saved?}
    is_player{Running by Player?}

    start --> with_location
    with_location -->|Yes| save3(Save at Input Location)
    with_location -->|No| online

    online -->|Yes| save1(Save at Bot's Location)
    online -->|No| is_player
    is_player -->|Yes| save2(Save at player's location)
    is_player -->|No| error1([Bot Not Exists])
```

### del

删除保存的假人

### config

配置假人

```mermaid
flowchart LR
    start([config])
    start --> bot_name(name)

    bot_name --> name(name)
    bot_name --> position(position)
    bot_name --> facing(facing)
    bot_name --> dimension(dimension)
    bot_name --> comment(comment)
    bot_name --> actions(actions)
    bot_name --> autoLogin(autoLogin)
    bot_name --> autoRunActions(autoRunActions)

    actions --> append("append &lt;action&gt;")
    actions --> insert("insert &lt;index&gt; &lt;action&gt;")
    actions --> delete("delete &lt;index&gt")
    actions --> edit("edit &lt;index&gt; &lt;action&gt;")
    actions --> clear(clear)
```

## 配置

### gamemode

默认值: `survival`

生成假人的游戏模式

### name_prefix

默认值：无

假人名称前缀

### name_suffix

默认值：无

假人名称前缀

### permissions

使用对应指令的最低权限

### 下载

> :warning: 注意：使用插件之前，先阅读仓库中的 README。

| 文件 | 版本 | 上传时间 | 大小 | 下载数 | 操作 |
| --- | --- | --- | --- | --- | --- |
| [Bot-v1.0.5.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/bot-v1.0.5) | 1.0.5 | 2022/12/29 15:19:31 | 13.55KB | 62 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/bot-v1.0.5/Bot-v1.0.5.mcdr) |
| [Bot-v1.0.4.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/bot-v1.0.4) | 1.0.4 | 2022/12/29 14:53:06 | 13.55KB | 1 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/bot-v1.0.4/Bot-v1.0.4.mcdr) |
| [Bot-v1.0.3.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/bot-v1.0.3) | 1.0.3 | 2022/12/29 15:14:20 | 13.11KB | 2 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/bot-v1.0.3/Bot-v1.0.3.mcdr) |
| [Bot-v1.0.2.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/bot-v1.0.2) | 1.0.2 | 2022/07/22 02:16:19 | 13.06KB | 261 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/bot-v1.0.2/Bot-v1.0.2.mcdr) |
| [Bot-v1.0.1.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/bot-v1.0.1) | 1.0.1 | 2022/07/21 05:06:17 | 13.06KB | 18 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/bot-v1.0.1/Bot-v1.0.1.mcdr) |
| [Bot-v1.0.0.mcdr](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/tag/bot-v1.0.0) | 1.0.0 | 2022/07/21 03:53:18 | 13.05KB | 9 | [下载](https://github.com/AnzhiZhang/MCDReforgedPlugins/releases/download/bot-v1.0.0/Bot-v1.0.0.mcdr) |

