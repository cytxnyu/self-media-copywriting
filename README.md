# 自媒体文案skill

根据你已有的素材，直接回答三个问题：**为了流量，前 3 秒说什么；为了获客，讲完怎么让合适的人来找；数据差，先改哪里。**

技能标识：`self-media-copywriting`。界面显示名：**自媒体文案skill**。

## 可以直接这样用

```text
用 $self-media-copywriting。这是我的素材/口播稿：……
这条主要想获取流量。帮我选一个前三秒开头，并写出后面怎么接。
```

```text
用 $self-media-copywriting。这是现有正文：……
我提供的服务是……，适合……，已有的咨询入口是……
帮我写结尾，让真正有这个需求的人来找我，也给第一次回复的话术。
```

```text
用 $self-media-copywriting。这是作品和数据：……
平台/实际入口：……；发布后多久：……；以前同类作品：……
先判断最值得改的一处，给具体改稿和验证方法。缺数据就说明边界。
```

也可以直接说：“把这堆素材写成一条完整口播”“已经拍完，不能补录，怎么修开头”。不用提前填满所有信息；技能会从现有材料提取，只补问影响当前任务的关键缺口。

## 会拿到什么

| 任务 | 交付 |
|---|---|
| 三秒开头 | 推荐首句、后续承接、画面建议及不同机制的备选 |
| 咨询结尾 | 具体对象、真实利益、一个行动、首次咨询承接 |
| 数据复盘 | 正确口径的观察、待验证解释、优先修改、验证指标 |
| 完整文案 | 一个明确角度、可直接口播的整稿、素材/证据需求 |

它会区分开头的“留住人”和结尾的“促成行动”，也会区分播放量、资料领取、有效咨询与成交。没有案例时可以用真实过程展示能力；没有产品时可以先验证需求。

## 安装

将本仓库放进支持 `SKILL.md` 的工具的技能目录，并保留 `references/` 与 `agents/`。

Codex 默认目录安装示例（若配置了 `CODEX_HOME`，使用其下的 `skills`）：

PowerShell：

```powershell
$skillRoot = if ($env:CODEX_HOME) { Join-Path $env:CODEX_HOME 'skills' } else { Join-Path $HOME '.codex/skills' }
git clone https://github.com/cytxnyu/self-media-copywriting.git (Join-Path $skillRoot 'self-media-copywriting')
```

macOS / Linux：

```bash
git clone https://github.com/cytxnyu/self-media-copywriting.git "${CODEX_HOME:-$HOME/.codex}/skills/self-media-copywriting"
```

目标目录已存在时先检查其中内容，避免覆盖自己的修改。安装后在能发现该技能的聊天中调用 `$self-media-copywriting`；已有聊天未显示时，新开聊天或重新加载技能。此技能不依赖 API 密钥、私有资料、其他自定义技能或专用脚本。

## 文件导航

- [SKILL.md](SKILL.md)：入口、目标判断、素材证据与输出约定。
- [知识精华与来源取舍](references/principles.md)：从课程笔记归纳出的决策方法。
- [开头与正文承接](references/opening.md)：前三秒和后续内容如何配合。
- [咨询引导](references/conversion.md)：真实交付如何连接客户行动。
- [数据诊断](references/diagnosis.md)：分母、基线、假设和修改优先级。
- [行为验收用例](evals/cases.md)：可重复运行的场景与观察标准。
- [本次验证记录](evals/results.md)：本版本实际验证范围与限制。

## 资料范围

依据用户提供的《自媒体变现实操笔记》、2026 年 10 月 19–20 日的 35 张课件截图，以及一段约 2.18 秒的同页录屏进行独立提炼。笔记标注课程来源为辣姣《自媒体变现路径》。截图有重复页面；录屏没有新增完整教程。

课程展示的两份进阶资料只有封面，未提供正文，因此本技能未声称吸收其完整内容。公开仓库只包含重新组织的方法、原创示例和技能文件，原始课件、聊天画面及个人信息保留在本地。

课程中的收益案例、平台排序、CES 权重和“两小时窗口”没有在此获得独立验证，不作为效果承诺或平台算法事实。具体平台规则需要使用时查验官方现行说明。对课程观点的取舍及本次新增的操作规范见[知识精华](references/principles.md#来源与取舍)。
