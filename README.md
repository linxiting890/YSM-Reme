# Reme 雷米 · YSM 模型包（Java 版）

> Minecraft Java 版 **Yes Steve Model（YSM）** 文件夹格式模型包
> 原作作者：[是Reme](https://space.bilibili.com/3546650257656003)（单人完成）
> 指导与参考：木土光军76（Bilibili UID `689067975`）
> 授权：**CC BY 4.0** · 详见 [LICENSE](LICENSE) 与 [ATTRIBUTION.md](ATTRIBUTION.md)

Reme（雷米）是作者的早期 YSM 作品，按作者自述「初学五天做出来」、仍在持续调整，个别模组环境下可能存在兼容问题。本仓库以**文件夹格式**开源：模型、动画、贴图的源文件全部可读可改，既能直接放进游戏加载，也能用 Blockbench / 文本编辑器二次编辑。

---

## 1. 模型内容

| 项目 | 内容 |
| --- | --- |
| 模型名称 | Reme 雷米（`ysm.json` 的 `metadata.name`） |
| 适配 | Yes Steve Model 模组，**建议 2.5.0 及以上**（配置使用了 2.5.0 新增的 `gui_foreground` / `gui_background`） |
| 格式 | 文件夹格式（`ysm.json` 索引，`spec: 2`） |
| 缩放 | `height_scale` / `width_scale` 均为 `0.7` |
| 材质 | 4 套：`default`、`Blue`、`Black`、`COS kiplef`（游戏内模型选择界面可切换） |
| 默认材质 | `textures/default.png` |
| 预览动画 | `gui`（`disable_preview_rotation: true`） |
| 轮盘动画 | 基础动作 6 个、坐姿 8 个、舞蹈 14 个 |
| 附加替换 | 箭、浮标（弹射物）；船、矿车（载具） |
| 模组兼容动画 | `tac.animation.json`（适配 TaCZ 永恒枪械工坊） |

### 1.1 外观调节（轮盘「外观」页，共 20 项）

| 控件 | 类型 | 变量 | 可选值 / 范围 |
| --- | --- | --- | --- |
| 高人来了（身高） | 滑条 | `v.g` | -1 ~ 2（步进 0.1） |
| 宽人来了（体宽） | 滑条 | `v.k` | -1 ~ 2（步进 0.1） |
| 平人来了 | 滑条 | `v.p` | -1 ~ 2（步进 0.1） |
| 头部大小 | 滑条 | `v.tbdx` | -0.3 ~ 1（步进 0.1） |
| 帽子 | 单选 | `v.mzv` | 编织帽 / 棒球帽 / 遮阳帽 / 无 |
| 战术背心与挎包 | 单选 | `v.b` | 挎包 / 战术背心 / 无 |
| 护目镜（佩戴） | 开关 | `v.mzx4` | 开 / 关 |
| 护目镜（未佩戴） | 开关 | `v.mzx5` | 开 / 关 |
| 尾巴饰品 | 开关 | `v.ybsp` | 开 / 关 |
| 腰包 | 开关 | `v.b3` | 开 / 关 |
| 鞋子 | 开关 | `v.x` | 开 / 关 |
| 蝴蝶结 | 开关 | `v.hd` | 开 / 关 |
| 腿环 | 开关 | `v.t` | 开 / 关 |
| 发卡 | 开关 | `v.fk` | 开 / 关 |
| 手套 | 开关 | `v.stx` | 开 / 关 |
| 裙子 | 开关 | `v.qzx` | 开 / 关 |
| 短发 | 开关 | `v.dfx` | 开 / 关 |
| 失去妙脆角 | 开关 | `v.szmcj` | 开 / 关 |
| 尾巴哪去了 | 开关 | `v.ybn` | 开 / 关 |
| 失踪的呆毛 | 开关 | `v.dmsz` | 开 / 关 |

### 1.2 表情（轮盘「表情」页）

| 控件 | 档位 |
| --- | --- |
| 眼睛 `v.yjx` | 默认 / 生气 / 哭哭 / `>   <` / `O   O` / 闭眼（共 6 档） |
| 嘴 `v.zmr` | 默认 / 微张 / 倒V嘴 / 猫猫嘴 / 一字嘴 / V字嘴 / X字嘴 / 歪嘴 / 张开（共 9 档） |
| 脸色 `v.lsx` | 默认 / 脸红 / 脸黑（共 3 档） |

### 1.3 动作列表

- **基础动作**：鼓掌、打招呼、行、否、耶好、御笔摇
- **坐姿**：坐下 1–6、随地大小睡、坐在边缘
- **舞蹈**：萝莉摇、鹿乃子虎视眈眈、催眠术、星辉闪耀、橙色正义、互联网过度依存、摇啊摇、摇摇乐、开车车、致命公司摇、快远离互联网、alice didida、谎言舞者、低皮质醇

---

## 2. 目录结构

```
.
├── ysm.json                      # 资源描述文件（固定名称，必须在根目录；不是模型文件）
├── models/                       # 模型 JSON（基岩版 1.12.0 几何）
│   ├── main.json                 #   玩家主模型（约 348 KB）
│   ├── arm.json                  #   第一人称手臂
│   ├── arrow.json                #   箭
│   ├── fishing_bobber.json       #   浮标
│   ├── boat.json                 #   船
│   └── minecart.json             #   矿车
├── animations/                   # 动画 JSON（基岩版 1.8.0）
│   ├── main.animation.json       #   主模型动画（约 184 KB）
│   ├── extra.animation.json      #   轮盘动画（约 1.26 MB）
│   ├── tac.animation.json        #   TaCZ 兼容动画（约 207 KB）
│   ├── arrow.animation.json
│   ├── boat.animation.json
│   └── unknown.animation.json
├── textures/                     # 贴图
│   ├── default.png               #   默认材质（约 8.7 KB）
│   ├── Blue.png / Black.png      #   额外配色
│   ├── COS kiplef.png            #   额外配色（文件名含空格，大小写敏感）
│   ├── arrow.png / boat.png / fishing_bobber.png / minecart.png
│   └── gui/                      #   选择界面背景与前景
├── avatar/                       # 作者头像（模型详情页展示）
├── lang/zh_cn.json、en_us.json    # 模型内文案的中文 / 英文翻译
```

---

## 3. 安装与使用

1. 在客户端（以及需要同步的服务端）安装 **Yes Steve Model** 模组，版本建议 2.5.0+，并确认与你的游戏版本、加载器（Forge / NeoForge / Fabric）匹配。
2. 将本仓库**整个文件夹**放到：

   ```
   .minecraft/config/yes_steve_model/custom/
   ```

   文件夹名即游戏内的模型 ID，可自行改名（例如改成 `Reme`）。
3. 进入游戏后按 `Alt` + `Y`（Forge / NeoForge）或 `Y`（Fabric）打开模型选择界面；也可点击界面右上角「打开模型文件夹」按钮核对放置位置。
4. 三种加载形式均可用：**文件夹**、**zip 压缩包**、**.ysm 加密包**。本仓库给的是文件夹形式，便于修改。

注意事项：

- 放在 `custom/` 下**无需授权**即可使用；放在 `auth/` 下则需要授权。本模型 `"free": false`，即允许被设置为授权模型。
- `.ysm` 是加密格式，导出后**无法再还原为可编辑的源文件**，且高版本导出的包在低版本加载不了。
- 修改 `ysm.json` 时请保持 **UTF-8 无 BOM** 编码。
- TaCZ 兼容动画（`tac.animation.json`）仅在安装 TaCZ 后才会被调用。

---

## 4. 二次编辑

- **模型**：`models/main.json` 是基岩版几何格式，用 Blockbench 的 `文件 → 打开模型` 打开，格式选 **Bedrock Entity Model**（基岩版实体模型）；第一人称手臂 `models/arm.json` 单独打开。**不要试图打开 `ysm.json`**，它是索引文件，Blockbench 会提示「不支持的文件格式」。
- **贴图**：`textures/*.png` 直接用画图软件改；材质显示名取自文件名，改文件名需同步 `ysm.json` 的 `files.player.texture`。
- **动画**：`animations/*.animation.json` 用 Blockbench 以 Bedrock Animation 格式打开。**含 Molang 表达式（如头部跟随视角、`math.sin`）的平滑关键帧，Blockbench 会报 `Smooth keyframes cannot contain math expressions.`，这是 Blockbench 的限制，游戏内正常生效**；改这类动画建议直接编辑 JSON 然后进游戏验证。
- **轮盘与表情**：改 `ysm.json` 的 `properties.extra_animation` / `extra_animation_classify` / `extra_animation_buttons`；`#分类` 前缀表示子菜单，`#按钮` 前缀表示配置面板。
- **提交前自检**（Python 3）：

  ```bash
  python -c "import json;json.load(open('ysm.json',encoding='utf-8'));print('ysm.json OK')"
  ```

  再确认 `ysm.json` 引用的每个路径都真实存在且大小写完全一致（Linux 服务端区分大小写）。

---

## 5. 作者与授权

- **原作作者**：是Reme（Bilibili UID `3546650257656003`），模型、动画、贴图均为其作品。
- **参与人员**：木土光军76（Bilibili UID `689067975`），角色为「指导与提供参考」。
- **授权方式**：原作品声明为 **CC BY**，本仓库据此以 **CC BY 4.0** 开源发布，并已获得原作者许可。
- **本仓库的改动**：仅仓储整理（清理 `.DS_Store`、将两个作者头像重命名为 `avatar/author-reme.png` 与 `avatar/author-2.png` 并同步 `ysm.json`、补充文档与 git 配置），**未修改任何模型 / 动画 / 贴图内容**。
- **再分发要求**（CC BY 4.0）：署名原作者「是Reme」与本仓库链接、附许可证链接、注明是否修改。署名样例见 [ATTRIBUTION.md](ATTRIBUTION.md)。
- **相关链接**：本仓库 [github.com/linxiting890/YSM-Reme](https://github.com/linxiting890/YSM-Reme) · YSM 模组 [Modrinth](https://modrinth.com/mod/yes-steve-model) · 作者爱发电 [afdian.com/a/ysmmod](https://afdian.com/a/ysmmod)

---

## 6. 免责声明

本仓库不包含 Minecraft 原版游戏素材；Yes Steve Model 模组的代码与内置模型版权归其各自作者所有。模型包按 CC BY 4.0「按现状」提供，作者自述模型仍在调整中，使用与修改风险自负。

---

## English Summary

**Reme (雷米)** is an open-source player model pack for **Yes Steve Model (YSM)** on Minecraft Java Edition, released in folder format so every model, animation and texture stays editable.

- **Original author**: 是Reme (Bilibili UID `3546650257656003`); guidance and reference by 木土光军76 (UID `689067975`); declared **CC BY**, published here under **CC BY 4.0** with the author's permission.
- **Compatible with**: YSM 2.5.0+ (uses the 2.5.0 `gui_foreground` / `gui_background` fields); ships a TaCZ-compatible animation.
- **Install**: copy the whole folder into `.minecraft/config/yes_steve_model/custom/`; the folder name becomes the in-game model ID.
- **Features**: 4 texture variants, height / width / head-size sliders, hat and vest radios, 13 accessory toggles, 6 eye states, 9 mouth states, 3 face colours, 6 gestures, 8 sitting poses, 14 dances, plus arrow / bobber and boat / minecart replacements.
- **Editing**: open `models/main.json` (Bedrock geometry) and `animations/*.json` (Bedrock animation) in Blockbench — never `ysm.json`, which is only an index file. Molang-driven smooth keyframes trigger a Blockbench warning but work in game.
- **License**: CC BY 4.0 — attribution required, indicate changes. See [LICENSE](LICENSE) and [ATTRIBUTION.md](ATTRIBUTION.md).
