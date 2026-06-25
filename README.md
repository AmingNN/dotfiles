# Dotfiles

使用 [chezmoi](https://www.chezmoi.io/) 管理个人 dotfiles，用于在多台机器之间同步开发环境、Shell 配置、终端配置和常用工具配置。

## 简介

这是我的个人点文件备份仓库，主要用于：

* 备份常用配置文件
* 在新机器上快速恢复开发环境
* 在多台设备之间同步配置
* 通过 `chezmoi` 持续管理和更新 dotfiles

## 快速使用

### 常规环境

适用于自己的长期使用机器。安装并保留 `chezmoi`，后续可以继续同步和管理配置。

```shell
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --apply <GitHub用户名>
```

### 一次性环境

适用于临时机器。应用配置后会清理 `chezmoi` 相关痕迹，不保留后续管理能力。

```shell
sh -c "$(curl -fsLS get.chezmoi.io)" -- init --one-shot <GitHub用户名>
```

## 后续同步

在已经初始化过的机器上，可以使用以下命令同步最新配置：

```shell
chezmoi update
```

## 说明

该仓库主要面向个人使用，配置内容可能包含强个人习惯。
如需复用，建议先 fork 后按自己的环境进行调整。
