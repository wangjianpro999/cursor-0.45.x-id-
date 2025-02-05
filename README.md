# 无广告代码已经更新

## Cursor ID 0.45.x 重置工具开源声明 
## ⚠️ 免责声明 | Disclaimer 
**本项目仅用于学术研究目的**，旨在研究现代IDE软件的设备标识机制。我们强烈建议通过官方渠道获取Cursor的正版授权。
## 📝 项目背景 | Background
本项目提供Windows系统下Cursor IDE 0.45.x系列（0.45.8已验证）的设备标识重置解决方案。该项目采用PyQt6构建GUI界面，通过修改注册表机制和配置文件实现设备指纹重置。
![a7000b7a3f27b29322482ae19496d2c7](https://github.com/user-attachments/assets/0fc581b5-088d-493d-91bf-12268e2eb87a)
## 🛠️ 下载链接
最新版也可以重置
https://ajq.lanzouv.com/iOtwR2mn3yfa
密码:aqqq
### 无广告代码已经更新
![PixPin_2025-02-05_13-56-26](https://github.com/user-attachments/assets/17745383-c21d-4bbd-9755-8d9bdae0104a)


**重要提醒**：使用者需自行承担以下风险：
- 软件授权失效风险
- 账号封禁风险
- 注册表修改导致的系统不稳定

**This is an academic research project** studying device identification mechanisms in modern IDEs. We strongly recommend obtaining official Cursor licenses through proper channels.

**Critical Notice**: Users assume all risks including but not limited to:
- License invalidation
- Account suspension
- System instability from registry modifications

---

## 🛠️ 技术特性 | Technical Features
```python
class IDGenerator:
    # 生成符合Cursor规范的设备ID
    @staticmethod
    def generate_mac_machine_id():
        """生成符合v4规范的UUID"""
        template = "xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx"
        return uuid.uuid4().hex
```

| 功能模块          | 实现原理                     |
|-------------------|----------------------------|
| 设备ID生成器      | 基于RFC4122规范实现v4 UUID  |
| 注册表操作        | 通过winreg模块修改MachineGuid |
| 进程管理          | 使用psutil进行进程监控       |

---

## 📥 安装与使用 | Installation & Usage

### 系统要求 | Requirements
- Windows 10/11 64位
- Python 3.8+
- 管理员权限运行

### 图形界面操作流程
1. 关闭Cursor IDE进程
2. 执行`main.py`启动重置工具
3. 点击"开始重置"按钮
4. 按照提示完成操作

---

## 🔧 技术架构 | Architecture
```mermaid
graph TD
    A[GUI界面] --> B[进程检测模块]
    B --> C[注册表备份模块]
    C --> D[ID生成引擎]
    D --> E[注册表写入模块]
    E --> F[配置文件更新]
```

---

## 🙏 鸣谢 | Acknowledgments
特别感谢 [hamflx/cursor-reset](https://github.com/hamflx/cursor-reset) 项目提供的初始研究思路，本工具在其基础之上进行了以下增强：
- 增加了GUI可视化界面
- 完善了注册表备份/恢复机制
- 添加了进程状态实时监控功能

---

## 📄 许可协议 | License
本项目采用GPLv3协议发布，商业使用需经作者书面授权。

```text
© 2024 ayc404. All rights reserved.
未经明确书面授权，任何企业/个人不得将本项目用于商业用途。
```

---

## 💬 反馈渠道 | Support
遇到技术问题请提交issue，或通过以下方式联系我们：
- 电子邮箱：anjiaqi404@qq.com

---

> 附：本工具包含Easter Egg彩蛋功能，连续点击标题栏五次即可触发特殊动画效果 🎉

### 项目简介
本工具旨在解决 Cursor IDE 的设备 ID 重置问题，支持 Cursor 0.45.x 版本（已在 0.45.8 版本上测试通过）。

⚠️  **注意**：
- 本项目仅提供 Windows 系统下的代码，暂无 macOS 版本。
- macOS 版本的思路和部分代码参考了 [hamflx/cursor-reset](https://github.com/hamflx/cursor-reset) 项目，在此表示感谢。

### ⚠️  免责声明
- 本项目仅供学习和研究，旨在研究 Cursor IDE 的设备识别机制。
- **强烈建议您购买 Cursor 的正版授权**，以支持开发者。
- 使用本工具可能违反 Cursor 的使用条款。作者不对使用本工具导致的任何问题负责，包括但不限于：
    - 软件授权失效
    - 账号封禁
    - 其他未知风险
- 如果您认可 Cursor 的价值，请支持正版，为软件开发者的工作付费。

### 主要功能
本工具的主要功能如下：
- **ID 重置**：生成新的设备 ID，并修改 Cursor 的配置文件和系统注册表（仅 Windows 系统）。
- **ID 备份**：备份当前的设备 ID，以便在需要时恢复。
- **强制关闭**：提供强制关闭 Cursor IDE 的功能，避免重置过程中出现问题。
- **日志记录**：详细记录重置过程中的操作，方便用户查看。
- **彩蛋功能**：有趣的彩蛋，可通过点击标题栏触发。

###  🛠️ 使用方法
#### 1. Windows 系统
- 在 Cursor IDE 中退出当前登录的账号。
- 完全关闭 Cursor IDE。
- 以管理员身份运行本工具。
- 点击“开始重置”按钮，按照提示操作。
- 重置完成后，打开 Cursor IDE 并使用新账号登录（**不要使用之前的账号**）。

#### 2. macOS 系统
- 由于本项目暂无 macOS 版本，请参考 [hamflx/cursor-reset](https://github.com/hamflx/cursor-reset) 项目中的说明进行操作。
- 或者考虑使用我提供的Windows版本（如果方便的话）。

### ⚠️  重要注意事项

#### 1. Windows 系统
- 本工具会修改系统注册表中的 `HKLM\SOFTWARE\Microsoft\Cryptography\MachineGuid`，该值可能被其他软件用作设备标识。如果修改后其他软件的授权失效，请自行承担后果。
- 原始的 `MachineGuid` 会被自动备份到 ` %USERPROFILE%\CursorReset_Backups ` 目录下。
- 如果需要恢复原始 `MachineGuid`，请从备份目录中找到对应的备份文件，然后使用注册表编辑器恢复该值。

#### 2. macOS 系统
- 本项目暂无 macOS 系统支持。
- 请参考 `hamflx/cursor-reset` 项目，使用其脚本。
- 其脚本会创建一个假的 `ioreg` 命令来模拟不同的设备标识。
- 原始的 `IOPlatformUUID` 会被备份到 `~/CursorReset_Backups` 目录下。
-  这个方法不会永久修改系统设置，但需要保持 PATH 环境变量的修改才能持续生效。

### 执行结果
- 备份文件的位置
- 新生成的 `MachineGuid` （Windows）
- 新的 `telemetry.machineId`
- 新的 `telemetry.macMachineId`
- 新的 `telemetry.devDeviceId`
- 新的 `telemetry.sqmId`

### 系统要求

#### 1. Windows 系统
- Windows 操作系统
- 管理员权限
- Cursor IDE 0.45.x 版本（已在 0.45.8 版本测试通过）

#### 2. macOS 系统
- 本项目暂无 macOS 系统支持，请参考 `hamflx/cursor-reset` 项目。
- 需 macOS 10.13 或更高版本
- Python 3
- sudo 权限
- Cursor IDE 0.45.x 版本

### 开源许可
本项目使用 MIT 开源许可，详情请参考 `LICENSE` 文件。

### 感谢
- 感谢 [hamflx/cursor-reset](https://github.com/hamflx/cursor-reset) 项目提供的思路和代码参考。

### 作者
- ayc404

---



# Cursor Identity Reset Utility (光标设备标识重置工具)

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)
![License](https://img.shields.io/badge/License-GPLv3-orange.svg)

## 📝 项目背景 | Background
本项目提供Windows系统下Cursor IDE 0.45.x系列（0.45.8已验证）的设备标识重置解决方案。该项目采用PyQt6构建GUI界面，通过修改注册表机制和配置文件实现设备指纹重置。
![a7000b7a3f27b29322482ae19496d2c7](https://github.com/user-attachments/assets/0fc581b5-088d-493d-91bf-12268e2eb87a)

This project provides a device identity reset solution for Cursor IDE 0.45.x series (verified on 0.45.8) on Windows systems. Built with PyQt6 GUI framework, it modifies both registry entries and configuration files to reset device fingerprints.
---



![PixPin_2025-02-04_03-07-01](https://github.com/user-attachments/assets/09d41b66-77d5-40bb-b4d3-23c66545d5ab)
![PixPin_2025-02-04_03-07-52](https://github.com/user-attachments/assets/64b5750f-809f-4df3-90bc-bc0d58216b14)
![PixPin_2025-02-04_03-08-26](https://github.com/user-attachments/assets/1df2f28d-a985-4742-b2ed-ef228a48a83f)



https://cloud.siliconflow.cn/i/CoW8MS0u

# SiliconCloud 裂变活动火热开启！2000万Tokens等你来领！

大家好！今天我们为大家带来一个超值的活动——**SiliconCloud 裂变活动**，2000万Tokens等你来领！

## 活动详情

**北京时间2024年8月1日起**，每成功邀请一位新用户注册SiliconCloud，您和好友均可获得**2000万Tokens**（价值14元平台配额）。邀请越多，奖励越多，快来体验SiliconCloud的强大功能！

### 活动规则
1. **邀请好友赚Tokens**：每成功邀请一位新用户，您将获得2000万Tokens。
2. **注册即送Tokens**：受邀好友完成注册后，立即获得2000万Tokens。
3. **14元配额**：新用户还可获得14元平台配额，体验流畅的DeepSeek API，告别卡顿网络版本！

## SiliconCloud API亮点

SiliconCloud这次上线的DeepSeek-R1&V3模型，凭借以下特点成为开发者和用户的首选：

1. **基于华为云昇腾云服务**
   首发推出DeepSeek x硅基流动x华为云的R1&V3模型推理服务。

2. **全球顶尖效果**
   通过自研推理加速引擎，部署在华为云昇腾云服务的DeepSeek模型，效果持平全球高端GPU部署。

3. **稳定的生产级服务**
   满足大规模生产环境需求，华为云昇腾云服务提供澎湃、弹性、充足的算力。

4. **零部署门槛**
   开发者可直接调用SiliconCloud API，轻松专注于应用开发，带来更易用的体验。

5. **优惠期价格**
   DeepSeek-V3的价格为￥1/M tokens（输入）& ￥2/M tokens（输出），DeepSeek-R1的价格为￥4/M tokens（输入）& ￥16/M tokens（输出）。

## API应用场景

SiliconCloud API可直接接入多款客户端应用，包括：

- **大模型客户端应用**：ChatBox、Cherry Studio、OneAPI、LobeChat、NextChat
- **代码生成应用**：Cursor、Vindsurf、CIine
- **大模型应用开发平台**：Dify
- **AI知识库**：Obsidian AI、FastGPT
- **翻译插件**：沉浸式翻译、欧路词典

## 立即注册

**点击下方链接，注册SiliconCloud**

或复制链接到浏览器注册：[https://cloud.siliconflow.cn/i/CoW8MS0u](https://cloud.siliconflow.cn/i/CoW8MS0u)

**快来参与裂变活动，邀请好友一起体验SiliconCloud的强大功能吧！**


## 帮帮孩子注册
## 我的助力额度完成一定数量了
## 我会上传没有广告的版本
## 感谢各位
