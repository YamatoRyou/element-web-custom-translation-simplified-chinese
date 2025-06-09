# 适用于 Element Web / 桌面客户端的自定义简体中文翻译.
## 说明
此仓库提供一个订阅, 用于改善 Element Web (含桌面客户端) 的简体中文翻译.  
**由于翻译率不足, 翻译仍在准备. 此仓库暂时闲置.**

## 订阅方法
1. 在客户端的 `config.json` 中该添加以下内容 (此文件位于 Elemmenr 个人数据文件夹, 具体取决于操作系统或启动参数):
```
{
  "custom_translations_url": "https://raw.githubusercontent.com/YamatoRyou/element-web-custom-translation-simplified-chinese/refs/heads/main/ew_tr_zh_Hans_new.json"
}
```  
2. 对于桌面客户端需要重新启动, 对于 Web 客户端需要清除缓存并刷新.

## 反馈
自定义翻译基于 Element 版本 1.11.101 给出的 key, 目前的方向是优先翻译轻易可见的任何位置.
如果发现肉眼可见未翻译的字符串请提交以下信息 (非常重要, 直接决定翻译效果):
- 当前显示在 UI 上的英文字符串 (格式: `aaa_bbb|ccc_ddd|eee`)
- 该字符串出现位置的完整截图 (确定其上下文)
- 使该字符串出现的步骤

## 目前已知不翻译的字符串
以下字符串由于疑似被硬编码; 难以确定其实际含义或具有标志性等原因导致被跳过; 暂时无法翻译或无法调整其格式:  
- 房间信息 -> 投票:
  `Active polls`
  `Past polls`  
- 设置 -> 外观:
  `Hey you. You're the best!`  
- 设置 -> 关于:
  `Privacy Policy`
  `Cookie Policy`  
- 设置 -> 实验室:
  `Markdown`
  `Dynamic room predecessors`
  `late-arriving room archives`
  `Element Call`
  `Emoji`

**不要反馈上述字符串.**
