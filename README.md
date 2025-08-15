<div align="center">
  <h1>AI-Voice-Typing</h1>
  <h3><strong>免费、高精度、可完全自定义的开源语音输入法</strong></h3>
    <a href="https://www.icloud.com/shortcuts/f4e92192603e47c6bd29cee019295e88" target="_blank"><img src="https://img.shields.io/badge/下载快捷指令-DD6666?style=for-the-badge&logo=apple&logoColor=white" alt="下载快捷指令" width="150"></a>
  
</div>
<br>
  <p align="center">
    <img src="https://raw.githubusercontent.com/lixiaojie001/images/main/20250814212314.png" width="80%" />
  </p>
  


## 🚀 介绍

基于 **Gemini** 的 **AI 语音输入快捷指令**，**完全开源、免费、可自定义词汇和规则，高识别精度**，**可用性超越现有语音输入法**。 **告别昂贵订阅软件**（Whisper Flow、AQUA Voice）和**传统语音输入法**（百度语音、讯飞语音）无法识别个性化词汇的局限，仅需 **免费 Gemini API Key**，就可使用 **超级AI语音输入法**。


**🎯 特别适用于：**
- **代码开发**（Cursor、Claude Code等IDE）
- **公司内部写作**（行业黑话、专业术语多的场景） 
- **专业领域写作**（学术研究、技术文档等）

## ✨ 核心功能

- **🎯 超高精度识别**：基于AI的多模态能力构建，理解语义和提示词的基础上识别输出。
- **⚙️ 高度定制**：自定义词汇和规则，适应个人语言习惯。
    ```markdown
    ## 自定义词汇示例
    qspace,n+1,实付GMV,反奶大法,硅基流动,商品魔方,宇树科技,仓店,tavily,水族异宠,by天SQL(读作色口),笑尿,claude code(即使听起来是cloud code，也要返回claude code), think ,think hard,think harder,ultrathink（不是奥创think）,gemini(不是接麦),粗线框,自有品牌
    
    ## 自定义规则示例
    - 数字使用阿拉伯数字123，除非是第一，第二，第三的描述
    - 数字计算，加减乘除等于使用符号， 比如4/3=0.75
    ```
- **🧠 上下文感知**：剪切板文本作语境参考，提升识别精度。
- **🔄 跨平台同步**：iPhone 和 Mac 配置无缝同步。
- **🌐 中英翻译**：集成快速翻译功能。在录音结尾说"Chinese to English"即可自动翻译成英文。
- **📖 完全开源**：代码透明，无隐私风险，支持社区改进。
- **⚡ 无需下载**：基于快捷指令实现，无需下载任何第三方App，轻量便捷。

## 🛠️ 快速开始

### 前置条件

1. **Gemini API Key**

### 安装配置

1. 下载安装快捷指令
2. 填入 Gemini API Key
3. 配置自定义词汇和规则

## 💡 Best Practice

### Mac 端

推荐配合 **Raycast** 使用：
1. 设置全局快捷键
2. 新建 Raycast Command，使用下列脚本：
    ```applescript
    #!/bin/bash

    # Required parameters:
    # @raycast.schemaVersion 1
    # @raycast.title voiceinput
    # @raycast.mode silent

    # Optional parameters:
    # @raycast.icon 🤖

    # Documentation:


    #!/bin/bash

    shortcuts run "AI-Voice-Typing v1"

    osascript -e '
    tell application "System Events"
        set frontApp to name of first application process whose frontmost is true
        tell application process frontApp
            set frontmost to true
            try
                set value of attribute "AXMain" of window 1 to true
                set value of attribute "AXFocused" of window 1 to true
            end try
        end tell
    end tell'

    osascript -e 'tell application "System Events" to keystroke "v" using command down'

    ```
3. **💡 提示**：录音时按空格键停止。若无效请开启系统设置中的键盘导航（系统设置 → 键盘 → 键盘导航）。

### iOS 端

- 通过"操作按钮"或辅助功能快速唤起
- 内容自动复制到剪切板

## ⚠️ 限制

- **响应时间**：比传统输入法稍长，但精度更高。随着AI大模型持续迭代，响应速度将进一步提升。

## 🤝 贡献

完全开源，欢迎"魔改"！
- **分享工作流**：可搭配其他快捷指令实现更多功能，如与 OmniFocus、Reminder、备忘录等结合实现高效语音输入
- **推荐模型**：如果发现更快更好且支持 HTTP 格式的AI模型，欢迎推荐和集成


