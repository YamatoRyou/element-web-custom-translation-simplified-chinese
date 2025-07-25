# 适用于 Element Web / 桌面客户端的自定义简体中文翻译
## 说明
此仓库提供一个订阅, 用于改善 Element Web (含桌面客户端) 的简体中文翻译.  

相关项目主页:  
Web 客户端: https://github.com/element-hq/element-web  
桌面客户端: https://github.com/element-hq/element-desktop  

**截至 2025 / 06 / 15, 已基本翻译完毕, 进入缓慢校对阶段. 可满足日常使用所需.**  
### 自定义翻译会因修正而随时做出更改, 订阅此翻译即表示你接受此更新策略.

----
## 订阅方法
`config.json` 并非 Element 必需文件, 但若要使用自定义翻译则其必须存在.  
此文件的参考格式请参阅 (英文文档): https://github.com/element-hq/element-web/blob/develop/config.sample.json  
此文件可用的配置项请参阅 (英文文档): https://github.com/element-hq/element-web/blob/develop/docs/config.md  
对于桌面客户端, 此文件在不同操作系统上的默认存储路径请参阅 (英文文档): https://github.com/element-hq/element-desktop?tab=readme-ov-file#user-specified-configjson

### 桌面客户端
1. 确定 `config.json` 的路径 (如果使用了额外启动参数例如 `--user-data-dir`; `--profile` 或 `--config`, 则最终取决于这些参数);
2. 编辑此文件, 添加以下内容:  
   **此 URL 可能会改变.**
```
{
  "custom_translations_url": "https://raw.githubusercontent.com/YamatoRyou/element-web-custom-translation-simplified-chinese/refs/heads/main/ew_tr_zh_Hans.json"
}
```
3. 保存修改并重启 Element.

### Web 客户端 (Docker)
1. 确定 `config.json` 的路径;
2. 编辑此文件, 添加以下内容:  
   **此 URL 可能会改变.**
```
{
  "custom_translations_url": "https://raw.githubusercontent.com/YamatoRyou/element-web-custom-translation-simplified-chinese/refs/heads/main/ew_tr_zh_Hans.json"
}
```
3. 保存修改并重启容器, 如有必要请使用 Element 自带的 "清除缓存并重载" 功能.

## 支持的版本
自定义翻译基于 Element 版本 1.11.101 给出的 key, 当前版本的前后一定范围理论上支持 (过旧的版本可能不行, 比如 1.10.x 甚至更旧).  
语言文件会随官方进度添加新字符串. **未来可能会随官方进度删除届时版本弃用的字符串, 这可能会导致旧版本重新出现翻译缺失. 建议及时更新 Element.**

## 反馈
作者水平有限, 如果发现可见未翻译的字符串; 翻译结果中存在错别字; 不完整的括号或未被实时替换的变量名, 请通过 Issue 提交以下信息 (非常重要, 直接决定翻译效果):
- 当前显示在 UI 上的英文字符串或占位字符串 (格式: `aaa_bbb|ccc_ddd|eee` 或 `aaa_bbb_ccc_ddd`)
- 当前显示在 UI 上需要修正的翻译结果
- 该字符串出现位置的完整截图 (用于确定其所处的上下文)
- 使该字符串出现的步骤

## 目前已知不翻译的字符串
**此列表可能不完整.**  
以下字符串由于疑似被硬编码; 难以确定其实际含义或具有标志性等原因导致被跳过; 暂时无法翻译或无法调整其格式:  
- 时间线 -> 日期跳转选项:
  `Last week`
  `Last month`  
  **需要在实验室启用 "跳转到日期".**  
  以上字符串未接入自定义翻译, 且被强制使用官方的简体中文翻译. 无法被覆盖.
  
- 设置 -> 外观:
  `Hey you. You're the best!`  
  以上字符串满足覆盖条件, 但~~夹带私货~~.
  
- 设置 -> 关于:
  `Privacy Policy`
  `Cookie Policy`  
  以上字符串未接入自定义翻译, 无法被覆盖.
  
- 设置 -> 实验室:
  `Markdown` (标志性名词, 不翻译)  
  `Element` (标志性名词, 不翻译)  
  `Element Call` (标志性名词, 不翻译)  
  `Emoji`  (标志性名词, 不翻译)  

- 时间线上的日期; 星期 (未接入自定义翻译, 且被强制使用官方的简体中文翻译. 无法被覆盖).  
- 某些已置入编辑框的占位字符串, 此类字符串可以由用户自行修改而不影响 Element 运行.

**不要反馈上述字符串.**

## 特定单词在本案中采用的翻译
`bridge`: 桥接器  
`room`: 房间  
`event`: 事件  
`space`: 空间  
`homeserver`: 主服务器  
`Integration`: 集成 (可能会更改)  
`power level`: 权力值 (可能会更改)  
`composer`: 编辑器  
`thread`: 消息列 (可能会更改)  
`DM (Direct message)`: 私聊  
`Secret storage`: 秘密存储  
`Thread`: 消息列 (可能会更改)  
`others`: 其它 (面向除人员外的所有对象); 其他 (仅面向人员)  
`passphrase`: 口令 (与密码的区别是更复杂, 由多个单词或不以半角空格分隔的字符串组成)  
`Timeline`: 时间线  
`widget`: 小部件 (可能会更改)  
