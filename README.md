# chat-history-page

该 $\LaTeX$ 包 `chat-history.sty` 旨在 $\LaTeX$ 文档中生成带头像的聊天气泡. 

![](fig/Snipaste_2024-12-30_23-23-21.png)

## 关于冷笑话集

*群年度冷笑话大全* 作为该包的示例提供. `example` 中包含了群友的冷笑话集的源代码. 编译好的pdf可以在 `output` 中下载并打印.

## 使用步骤

1. **安装包文件**  
   将 `chat-history.sty` 文件放置于工作目录中, 确保 LaTeX 能找到该文件.

2. **使用命令将文本显示为聊天记录**  
   - 使用 `\context{text}` 定义聊天发生的背景.
   - 使用 `\newchatperson{name}{avatar}{nickname}{color}` 定义聊天气泡, 人物出现左侧.
   - 使用 `\newchathost{name}{avatar}{nickname}{color}` 定义聊天气泡, 人物出现右侧.
   - 使用 `\avatarwithtext{x}{y}{image}{name}` 在`tikzpicture`环境中定义头像与文本.

3. **生成文档**  
   - `example/main.tex` 示例中展示了如何使用这些命令生成带头像的聊天记录. **由于同时需要Emoji和中文支持, 请使用LuaLatex编译文档.** 

## 示例 

`example/main.tex` 文件展示了如何使用该包生成群聊内容. 为了方便编辑, 具体的聊天记录分开储存在以年份命名的 `tex` 文件中. **在编译前请确保有相关的字体如`Noto Sans SC`和`Noto Color Emoji`, 或将相关语句替换为自己的字体.**