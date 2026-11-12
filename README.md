# potplayer-subtitle-translate

PotPlayer 的实时字幕翻译扩展，通过 OpenAI 兼容 API 翻译当前显示的字幕。

## 文件

| 文件 | 用途 |
| --- | --- |
| `SubtitleTranslate - ChatGPT.as` | 扩展脚本 |
| `SubtitleTranslate - ChatGPT.ico` | 面板图标 |

## 安装

两个文件一起放到 PotPlayer 安装目录下的 `Extension\Subtitle\Translate\`，重启 PotPlayer 后在字幕翻译扩展里选中它。

## 配置

首次使用在 PotPlayer 的「账户信息」面板填模型名、API 地址与 key。本地 LM Studio / Ollama 这类无需鉴权的服务，key 留空或填 `nullkey`。配置会持久化，之后选中插件直接生效；面板设置的优先级高于文件里的 `GPT_pre_*` 默认值。

## 许可

源文件中未见明确许可声明，按原样收录。
