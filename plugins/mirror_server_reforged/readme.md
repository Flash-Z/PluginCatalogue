**English** | [中文](readme-zh_cn.md)

\>\>\> [Back to index](/readme.md)

## mirror_server_reforged

### Basic Information

- Plugin ID: `mirror_server_reforged`
- Plugin Name: MirrorServerReforged
- Version: 1.0.3
  - Metadata version: 1.0.3
  - Release version: 1.0.3
- Total downloads: 412
- Authors: [GamerNoTitle](https://github.com/GamerNoTitle)
- Repository: https://github.com/EMUnion/MirrorServerReforged
- Labels: [`Management`](/labels/management/readme.md)
- Description: A reforged version of [MCDR-Mirror-Server](https://github.com/GamerNoTitle/MCDR-Mirror-Server), which is a plugin for MCDR-Reforged 2.0+.

### Dependencies

| Plugin ID | Requirement |
| --- | --- |
| [mcdreforged](https://github.com/Fallen-Breath/MCDReforged) | \>=2.0.0 |

### Requirements

| Python package | Requirement |
| --- | --- |

### Introduction

# MirrorServerReforged

![MirrorServerReforged](https://socialify.git.ci/EMUnion/MirrorServerReforged/image?description=1&font=Inter&forks=1&issues=1&language=1&owner=1&pattern=Circuit%20Board&stargazers=1&theme=Light)

A reforged version of [MCDR-Mirror-Server](https://github.com/GamerNoTitle/MCDR-Mirror-Server), which is a plugin for MCDR-Reforged 2.0+.

I'll simply introduce it.

## Getting Started

This plugin will initalize when the first run, it will do the following opeartions
- Create `MirrorServerReforged.json` in your `config` folder and fill the default config in it
- Create`Mirror` folder to store your files of mirror server
- Create `./server/world/`/`./world` in `Mirror` folder (This depends on whether you use MCDR or not, use as default)

But these operations are not enough, what you need to do are as following
- Put your server core and dependencies into `./Mirror/server` folder
- Edit start command and rcon information in file `config.yml` in the folder`./Mirror/`
- Edit the content in `./Mirror/server/server.properties`. What you need to pay attention to is the ports of the mirror server and rcon related information in order to avoid encountering to the main server

## Config

If you want to change the config of this plugin, you can change the content of `MirrorServerReforged.json` in `config` folder

```json
{
  "world":[
    "world"
  ],
  "command":"python3 -m mcdreforged",
  "rcon":{
    "enable":false,
    "host":"localhost",
    "port":25565,
    "password":"password"
  }
}
```

Now, I'll introduce the content of the config file:
- `world` is a list include all your world's folders. For `Vanilla` type server, this can leave it as default. But for `Bukkit`/`Waterfall`/`Catserver` or other server cores like them that have more than one world folder, you need to input them in the list follow after `world`. E.G.: The `Bukkit` server has folders `world`, `world_nether`, `world_the_end`, then it should be filled with `['world','world_nether','world_the_end']`.
- `command` Start command. Here we use this command as you use MCDR in your mirror server as default. For `Vanilla` or `Bukkit-Like` server, you need to change it to the suitable one. E.G.: `java -Xmx16G -Xms1G -jar server.jar nogui`
- `rcon` will contain all the rcon-related config and this feature will only be used to turn off the mirror server remotely.
    - `enable` is the switch of rcon feature, it should be `true` or `false`. Rcon will not be able to use if this is set to `false`, especially the command `!!msr stop`
    - `host` is the address of your mirror server, change it as your need.
    - `port` is the port of your mirror server, change it as your need.
    - `password` is the password of the rcon feature on your mirror server, change it as your need.

## Command List

```
!!msr help - Display help message
!!msr sync - Sync the world to the mirror server
!!msr reload - Reload config
!!msr start - Start mirror server
!!msr stop - Stop mirror server (Rcon feature enable is needed)
!!msr init - Initalize mirror server (Use it only when you use MCDR in your mirror server)
!!msr status - Checkout the status of your mirror server
```
### Download

> :warning: Warning: Read the README file in plugin repository before using it.

| File | Version | Upload Time | Size | Downloads | Operations |
| --- | --- | --- | --- | --- | --- |
| [MirrorServerReforged-v1.0.3.mcdr](https://github.com/EMUnion/MirrorServerReforged/releases/tag/1.0.3) | 1.0.3 | 2022/02/11 13:32:32 | 8.22KB | 374 | [Download](https://github.com/EMUnion/MirrorServerReforged/releases/download/1.0.3/MirrorServerReforged-v1.0.3.mcdr) |
| [MirrorServerReforged-v1.0.2.mcdr](https://github.com/EMUnion/MirrorServerReforged/releases/tag/1.0.2) | 1.0.2 | 2022/02/05 07:17:57 | 8.16KB | 13 | [Download](https://github.com/EMUnion/MirrorServerReforged/releases/download/1.0.2/MirrorServerReforged-v1.0.2.mcdr) |
| [MirrorServerReforged-v1.0.1.mcdr](https://github.com/EMUnion/MirrorServerReforged/releases/tag/1.0.1) | 1.0.1 | 2022/01/25 01:25:31 | 8.13KB | 22 | [Download](https://github.com/EMUnion/MirrorServerReforged/releases/download/1.0.1/MirrorServerReforged-v1.0.1.mcdr) |
| [MirrorServerReforged-v1.0.0.mcdr](https://github.com/EMUnion/MirrorServerReforged/releases/tag/1.0.0) | 1.0.0 | 2022/01/24 10:55:37 | 8.38KB | 3 | [Download](https://github.com/EMUnion/MirrorServerReforged/releases/download/1.0.0/MirrorServerReforged-v1.0.0.mcdr) |

