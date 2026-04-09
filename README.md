# 🌊 Wuwa Mod Fixer

A tool designed for fixing textures, hashes, and vertex groups in modified assets caused by version updates or model changes.

[English](#english-version) | [中文说明](#chinese-version)

---

<a name="chinese-version"></a>
## 中文说明

### ✨ 主要功能
- **自动化修复**：自动识别资源哈希变动并进行替换。
- **派生 Hash 支持**：通过纹理重定向修复高/中画质下的纹理错误。
- **回滚管理**：内置回滚管理器，可随时恢复到修改前的原始状态。
- **跨平台 GUI**：基于 Iced 0.14 构建，支持 Windows、Linux (Steam Deck)。
- **双模式运行**：支持图形界面与传统的控制台模式。

### 🛠️ 编译与打包
确保你已安装 [Rust](https://rustup.rs/) 环境。

#### 本地运行
```bash
cargo run --release
```

#### Windows 打包
```bash
cargo build --release --target x86_64-pc-windows-msvc
```

#### Linux 打包 (Ubuntu/Steam Deck)
需预装 `libx11-dev`, `libwayland-dev` 等依赖。
```bash
cargo build --release
```

### 🚀 命令行参数
程序支持以下启动参数：

| 参数 | 说明 |
| :--- | :--- |
| `--cli` | **进入旧版控制台模式**。 |
| `--dev` | **开发者模式**。强制加载本地配置文件，禁用远程获取逻辑。 |
| `--path <路径>` / `-p <路径>` | 在 CLI 模式下直接指定处理目录。 |
| `--texture-override` | 启用“补全贴图状态”。 |
| `--stable-texture` | 启用“应用稳定纹理”（与 `--texture-override` 互斥，后者会被关闭）。 |
| `--aero-fix` | 启用女漂风主眼部修复（TexCoord 模式）。 |
| `--aero-fix-mirror` | 启用女漂风主眼部修复（Texture mirror 模式）。 |

**示例：**
```bash
# 以开发者模式运行
cargo run -- --dev

# 以控制台模式运行
./Mod_Fixer --cli

# 在 CLI 模式下直接处理指定目录，不再追加询问
./Mod_Fixer --cli "C:/Mods/Wuwa" --texture-override

# 也可以显式使用 --path / -p
./Mod_Fixer --cli --path "C:/Mods/Wuwa" --stable-texture --aero-fix
```

---

<a name="english-version"></a>
## English

### ✨ Features
- **Automated Fixes**: Automatically detects and replaces asset hash changes.
- **Derived Hash Support**: Fixes texture glitches via redirection for different quality settings.
- **Rollback Manager**: Built-in manager to revert modifications to their original state.
- **Cross-platform GUI**: Built with Iced 0.14, supports Windows and Linux (Steam Deck).
- **Dual Mode**: Supports both Graphical User Interface and classic Terminal mode.

### 🛠️ Build & Packaging
Ensure you have [Rust](https://rustup.rs/) installed.

#### Run Locally
```bash
cargo run --release
```

#### Build for Windows
```bash
cargo build --release --target x86_64-pc-windows-msvc
```

#### Build for Linux (Ubuntu/Steam Deck)
Requires dependencies like `libx11-dev`, `libwayland-dev`.
```bash
cargo build --release
```

### 🚀 Command Line Arguments
The application supports the following startup arguments:

| Argument | Description |
| :--- | :--- |
| `--cli` | **Enter Legacy Console Mode**. |
| `--dev` | **Developer Mode**. Forces loading local configuration and disables remote fetch. |
| `--path <path>` / `-p <path>` | Provide the target directory directly in CLI mode. |
| `--texture-override` | Enable "Complete Texture States". |
| `--stable-texture` | Enable "Stable Texture" (mutually exclusive with `--texture-override`; this disables it). |
| `--aero-fix` | Enable Aero FemaleRover eye fix in TexCoord mode. |
| `--aero-fix-mirror` | Enable Aero FemaleRover eye fix in Texture mirror mode. |

**Example:**
```bash
# Run in dev mode
cargo run -- --dev

# Run in console mode
./Mod_Fixer --cli

# Run CLI mode without interactive prompts
./Mod_Fixer --cli "C:/Mods/Wuwa" --texture-override

# Or use --path / -p explicitly
./Mod_Fixer --cli --path "C:/Mods/Wuwa" --stable-texture --aero-fix
```
## ❤️ 赞助支持 / Support

如果这个修复工具拯救了你的 Mod，欢迎请我喝杯咖啡！你的支持是我持续维护更新的最大动力。  
If this tool saved your mods, consider buying me a coffee! Your support is my biggest motivation to keep updating.

[![Ko-fi](https://img.shields.io/badge/Ko--fi-F16061?style=for-the-badge&logo=ko-fi&logoColor=white)](https://ko-fi.com/moonholder)
[![Afdian](https://img.shields.io/badge/Afdian-946CE6?style=for-the-badge&logo=electron&logoColor=white)](https://ifdian.net/a/moonholder)
---
