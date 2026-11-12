# potplayer-subtitle-translate

PotPlayer 的实时字幕翻译扩展，通过 OpenAI 兼容 API 翻译当前显示的字幕。

## 文件

| 文件 | 用途 |
| --- | --- |
| `SubtitleTranslate - ChatGPT.as` | 扩展脚本（本地修改版，见下） |
| `SubtitleTranslate - ChatGPT.ico` | 面板图标 |

## 安装

两个文件一起放到 PotPlayer 安装目录下的 `Extension\Subtitle\Translate\`，重启 PotPlayer 后在字幕翻译扩展里选中它。

## 配置

首次使用在 PotPlayer 的「账户信息」面板填模型名、API 地址与 key。本地 LM Studio / Ollama 这类无需鉴权的服务，key 留空或填 `nullkey`。配置会持久化，之后选中插件直接生效；面板设置的优先级高于文件里的 `GPT_pre_*` 默认值。

## 许可与来源

脚本源自 [Felix3322/PotPlayer_ChatGPT_Translate](https://github.com/Felix3322/PotPlayer_ChatGPT_Translate)，上游项目以 **GPL-3.0** 发布（[许可全文](https://github.com/Felix3322/PotPlayer_ChatGPT_Translate/blob/master/LICENSE)）。

本仓库收录的 `SubtitleTranslate - ChatGPT.as` **不是上游原版**，而是基于上游 v1.9.2 的本地修改版，主要改动：清空预置默认值（改为面板持久化，适配 LM Studio / Ollama）、新增采样温度与重试上限、译文历史成对上下文、目标语言切换时清空历史，以及针对字幕场景重写的提示词与语域词表。图标文件未改动。

依据 GPL-3.0，该派生版本同样以 GPL-3.0 授权，保留原作者版权，并在此注明修改。本仓库仅供自用备份，未发布 Release。
