<div align="center">

### Zzup012 · YangoSec

本地优先的安全工具 · 漏洞挖掘 · 竞赛

<sub>Local-first security tooling · vulnerability research · CTF</sub>

[![ReachScope](https://img.shields.io/github/v/release/tubibibo/reachscope-workbench?label=reachscope&color=2e7d5b&logo=python&logoColor=white)](https://github.com/tubibibo/reachscope-workbench)
[![CI](https://github.com/tubibibo/reachscope-workbench/actions/workflows/ci.yml/badge.svg)](https://github.com/tubibibo/reachscope-workbench/actions/workflows/ci.yml)
[![LRC Toolkit](https://img.shields.io/github/v/release/tubibibo/lrc-toolkit?label=lrc-toolkit&color=3178c6&logo=typescript&logoColor=white)](https://github.com/tubibibo/lrc-toolkit)
[![CodeSheaf](https://img.shields.io/github/v/release/tubibibo/codesheaf?label=codesheaf&color=3178c6&logo=typescript&logoColor=white)](https://github.com/tubibibo/codesheaf)

</div>

---

## 在做的事

**[ReachScope Workbench](https://github.com/tubibibo/reachscope-workbench)** — 把一次发现从「采集 → 加固 → 复测 → 对比 → 关闭」串成闭环的本地工作台。Android / Web / 云配置 / 主机四个模块共用一套任务队列、证据结构与 SQLite 工作区；只监听回环，界面把「观察」「候选路径」「已确认漏洞」分开，不把启发式结果说成结论。

**[LRC Toolkit](https://github.com/tubibibo/lrc-toolkit)** / **[CodeSheaf](https://github.com/tubibibo/codesheaf)** — 两个 VS Code 扩展：一个做同步歌词的编辑与校验，一个把文件、选中范围和 import 依赖打成一包给模型。

## 漏洞挖掘

**CNVD 原创高危 × 2**（2026.05 / 2026.09）— 独立完成挖掘、验证与报送，2 个原创高危漏洞被国家信息安全漏洞共享平台收录，涉及某远程医疗综合服务平台与某网络存储设备。

**企业 SRC / 众测** — 在漏洞盒子、补天与厂商自建 SRC 提交 20+ 篇报告，覆盖出行、社交、医疗、游戏，已确认 11 个。其中：

- **严重** · 登录回调校验不严，可外带他人微信授权码并接管账号（某出行平台）
- **高危** · 按可枚举 `t_id` 批量读取他人真实手机号（某物流平台社区）
- **高危** · 服务端信任请求体里的 `user_id`，可批量读取任意用户通讯录（某物流平台 App）
- **高危** · SSO 回跳白名单含已失控域名，会话票据可被投递至第三方域（某短视频平台）
- **中危** · `gourl` 参数匿名可控的 DOM 型 XSS（某视频平台 passport）
- **中危** · 分号绕过 nginx 路径封锁，匿名调用 DWR 后端方法（某医疗平台）

## 竞赛

| 赛事 | 成绩 |
| --- | --- |
| 第 23 届全国大学生信息安全与对抗技术竞赛（ISCC 2026）· 全国总决赛 | 二等奖 |
| 河南省「御网杯」网络安全大赛（第十届）· 本科组 | 一等奖 |
| 睿抗机器人开发者大赛（RAICOM 2026）· 福建赛区 | 二等奖 |
| 软件系统安全赛 · 华东赛区 | 三等奖 |

## 开源

向 [frida](https://github.com/frida)（frida-gum / frida-core / frida-tools）和 [projectdiscovery/naabu](https://github.com/projectdiscovery/naabu) 提交的修复已合并，涉及 x86 重定位、模拟层加载回退、`frida-ps` 枚举中断等。另有 semgrep、impacket、APKiD 等项目的 6 个修复 PR 在审。

## 在意的事

证据要留得住，事后能指着说「这里」；没证实的就说没证实。下一步想在 ReachScope 上补一层红蓝验证：授权、非破坏，但能把影响真正证出来，证据跟结论一起走。做出来再写。

---

<sub>想聊直接开 issue。中文优先。</sub>
