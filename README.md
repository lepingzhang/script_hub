# wechat-gptbot 脚本调用插件

1. 本项目作为 `wechat-gptbot` 插件，可以根据关键字调用不同的执行脚本;
2. 你可以参考现有的脚本样例添加你自己的脚本。

## 安装指南

### 1. 添加插件源
在 `plugins/source.json` 文件中添加以下配置：
```
{
  "news_hub": {
    "repo": "https://github.com/lepingzhang/script_hub.git",
    "desc": "根据关键词调用不同的脚本执行任务"
  }
}
```

### 2. Windows设置一个具体的路径
将该路径作为较为脚本执行路径填入`config`中。

### 3. 插件配置
在 `config.json` 文件中添加以下配置：
```
"plugins": [
  {
    "name": "script_hub",
    "commands": {
      "整理题库：": "auto_QA.py"
    }
  }
]
```

### 4. 支持添加多个脚本
不同的脚本可能需要适当调整插件代码。
