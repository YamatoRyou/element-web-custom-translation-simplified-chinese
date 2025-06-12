# 适用于 Element Web / 桌面客户端的自定义简体中文翻译
## 说明
此仓库提供一个订阅, 用于改善 Element Web (含桌面客户端) 的简体中文翻译.  

相关项目主页:  
Web 客户端: https://github.com/element-hq/element-web  
桌面客户端: https://github.com/element-hq/element-desktop  

**截至 2025 / 06 / 12, 基于字符串数量统计翻译率约 88%.**  
**自定义翻译会因修正而随时做出更改.**

## 订阅方法
`config.json` 并非 Element 必需文件, 但若要使用自定义翻译则其必须存在.  
此文件的参考格式请参阅 (英文文档): https://github.com/element-hq/element-web/blob/develop/config.sample.json  
此文件可用的配置项请参阅 (英文文档): https://github.com/element-hq/element-web/blob/develop/docs/config.md  
对于桌面客户端, 此文件在不同操作系统上的默认存储路径请参阅 (英文文档): https://github.com/element-hq/element-desktop?tab=readme-ov-file#user-specified-configjson

### 桌面客户端
1. 确定 `config.json` 的路径 (如果使用了额外启动参数例如 `--user-data-dir`, 则取决于这些参数);
2. 编辑此文件, 添加以下内容:  
   **此 URL 可能会改变.**
```
{
  "custom_translations_url": "https://raw.githubusercontent.com/YamatoRyou/element-web-custom-translation-simplified-chinese/refs/heads/main/ew_tr_zh_Hans_new.json"
}
```
3. 保存修改并重启 Element.

### Web 客户端 (Docker)
1. 确定 `config.json` 的路径;
2. 编辑此文件, 添加以下内容:  
   **此 URL 可能会改变.**
```
{
  "custom_translations_url": "https://raw.githubusercontent.com/YamatoRyou/element-web-custom-translation-simplified-chinese/refs/heads/main/ew_tr_zh_Hans_new.json"
}
```
3. 保存修改并重启容器, 如有必要请使用 Element 自带的 "清除缓存并重载" 功能.

## 反馈
自定义翻译基于 Element 版本 1.11.101 给出的 key (反馈时使用的版本不能低于此), 目前的方向是优先翻译轻易可见的任何位置.
如果发现肉眼可见未翻译的字符串; 翻译结果中存在错别字或未被实时替换的变量名, 请提交以下信息 (非常重要, 直接决定翻译效果):
- 当前显示在 UI 上的英文字符串 (格式: `aaa_bbb|ccc_ddd|eee`)
- 当前显示在 UI 上需要修正的翻译结果
- 该字符串出现位置的完整截图 (确定其上下文)
- 使该字符串出现的步骤

## 目前已知不翻译的字符串
**此列表可能不完整.**
以下字符串由于疑似被硬编码; 难以确定其实际含义或具有标志性等原因导致被跳过; 暂时无法翻译或无法调整其格式:  
- 时间线 -> 日期跳转选项:
  `Last week`
  `Last month`  
  以上字符串未接入自定义翻译, 且被强制使用官方的简体中文翻译. 无法被覆盖.

- 房间信息 -> 投票:
  `Active polls`
  `Past polls`  
  以上字符串未接入自定义翻译, 无法被覆盖.
  
- 设置 -> 外观:
  `Hey you. You're the best!`  
  以上字符串满足覆盖条件, 但暂不翻译.
  
- 设置 -> 通知:
  `People`  
  以上字符串未接入自定义翻译, 无法被覆盖.
  
- 设置 -> 关于:
  `Privacy Policy`
  `Cookie Policy`  
  以上字符串未接入自定义翻译, 无法被覆盖.
  
- 设置 -> 实验室:
  `Markdown` (标志性名词, 不翻译)  
  `Dynamic room predecessors` (难以确定实际含义, 不翻译)  
  `late-arriving room archives` (难以确定实际含义, 不翻译)  
  `Element Call` (标志性名词, 不翻译)  
  `Emoji`  (标志性名词, 不翻译)  

**不要反馈上述字符串.**
