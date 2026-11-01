# 上游贡献记录

本人在 [ddcat-ai/open-ai-canvas](https://github.com/ddcat-ai/open-ai-canvas)（AI 影视创作开源工作台）的贡献记录，截至 2026-11-01。

## 总览

- 提交 PR **15** 个（账号 `itsWyatt-K` 14 个 + 账号 `WMRBYY` 1 个）
- **12** 个的代码已进入上游 `main` 分支，占 80%
- 上游 `main` 中现有 **20** 个提交（author: itsWyatt-K，2026-09-21 ~ 09-23），合计 **+6780 / −1820 行**，涉及 **29** 个文件

其中 12 个已落地的 PR 分两种形态：

| 落地形态 | 数量 | 说明 |
|---|---|---|
| GitHub 标记 Merged | 4 | 走平台合并按钮，PR 显示紫色 Merged 徽章 |
| 维护者 squash / cherry-pick 落库后关闭原 PR | 8 | 代码已在 `main`，但 PR 状态显示 closed，不带 Merged 徽章 |

> 第二种不是"未合并"。上游维护者的习惯是把补丁在本地 squash 或 cherry-pick 后推入 `main`，再手动关闭原 PR。判定依据见下方逐条佐证。

## 一、经 GitHub 正式合并（4 个）

| PR | 内容 | 合并日期 | 上游提交 |
|---|---|---|---|
| [#568](https://github.com/ddcat-ai/open-ai-canvas/pull/568) | 新增 72 个社区创作方法论技能（judian-skills） | 2026-09-21 | `73ef84ffc` |
| [#575](https://github.com/ddcat-ai/open-ai-canvas/pull/575) | 种子技能统一为 34 个场景域包（judian-skills 完整两层资产） | 2026-09-22 | `0021f64d5` `3fb703dd2` |
| [#577](https://github.com/ddcat-ai/open-ai-canvas/pull/577) | 技能 description 进入 Agent 系统提示 manifest | 2026-09-22 | `5fe27ae64` |
| [#580](https://github.com/ddcat-ai/open-ai-canvas/pull/580) | 新增 skill_search 工具，Agent 侧技能检索 | 2026-09-22 | `18b082a2d` `e28c28f97` `04bbbf642` `590f6b420` |

## 二、已进入上游 main（维护者落库后关闭原 PR，8 个）

| PR | 内容 | 上游落库提交 | 落地佐证 |
|---|---|---|---|
| [#590](https://github.com/ddcat-ai/open-ai-canvas/pull/590) | 技能使用统计端点，把启用/检索/读取归因到具体技能 | `33baecde2` | 提交信息带 `(#590)`；3-way merge 对当前 main 净改动 0 |
| [#603](https://github.com/ddcat-ai/open-ai-canvas/pull/603) | 场景预设只读端点 `GET /api/skills/presets` | `ec81a1b92` | 提交信息带 `(#603)`；端点现存于 `backend/internal/handler/skills.go` |
| [#604](https://github.com/ddcat-ai/open-ai-canvas/pull/604) | 种子条目同步合规改造后的 judian-skills（22 个 instruction 更新） | `c4879421c` | 改动量 +22/−22 与 PR 完全一致；上游种子「蒸馏」措辞残留实测为 0 |
| [#606](https://github.com/ddcat-ai/open-ai-canvas/pull/606) | 门房配方表改用商店真名并标注上架状态 | `7ebdd0626` | 改动量 +1/−1 与 PR 一致；维护者原话：「主线已包含…因此关闭。感谢贡献」 |
| [#607](https://github.com/ddcat-ai/open-ai-canvas/pull/607) | ask_user 必须给可点选项，禁止把候选写进正文 | `7c01d29a0` | 提交信息带 `(#607)` |
| [#608](https://github.com/ddcat-ai/open-ai-canvas/pull/608) | 会话级场景胶囊，一键挂载技能组合 | `67cbda6cd` | 提交信息带 `(#608)` |
| [#593](https://github.com/ddcat-ai/open-ai-canvas/pull/593) | recall_lessons 分词器放行中文单字（CJK token 被静默吞掉） | `23b4b2add` | `git patch-id` 与上游提交精确匹配 |
| [#594](https://github.com/ddcat-ai/open-ai-canvas/pull/594) | skill_search 分词器放行中文单字（CJK token 被静默吞掉） | `bca47a27b` | `git patch-id` 与上游提交精确匹配 |

## 三、未采纳（2 个）

| PR | 内容 | 状态 | 原因 |
|---|---|---|---|
| [#437](https://github.com/ddcat-ai/open-ai-canvas/pull/437) | 影策 fork 回流：接回 v1.2.7 + D-057 Agent Server Executor 双通道（60 提交 / 308 文件 / +20757） | Closed 2026-09-18 | 范围过大，维护者未回应 |
| [#611](https://github.com/ddcat-ai/open-ai-canvas/pull/611) | 种子聚焦为双产线 13 工位（68→47）+ Agent 双产线引导策略 v9 | Closed 2026-10-14 | 本人主动关闭：分支基线早于项目改名，与当前 main 已演变为大规模回退，不具备可合并性 |

## 四、待审（1 个）

| PR | 内容 | 状态 |
|---|---|---|
| [#939](https://github.com/ddcat-ai/open-ai-canvas/pull/939) | 电商 Agent 与后台电商知识库前后端（9 提交 / 288 文件） | Open，2026-11-01 提交 |

## 怎么核实

- PR 列表（主账号）：[pulls?q=author:itsWyatt-K](https://github.com/ddcat-ai/open-ai-canvas/pulls?q=author%3AitsWyatt-K)
- PR 列表（第二账号）：[pulls?q=author:WMRBYY](https://github.com/ddcat-ai/open-ai-canvas/pulls?q=author%3AWMRBYY)
- 提交列表：[main 分支 author:itsWyatt-K](https://github.com/ddcat-ai/open-ai-canvas/commits/main?author=itsWyatt-K)

逐条核验方法：

```bash
# 1. 看某个 PR 的补丁是否已在上游（"-" 开头表示内容已被吸收）
git cherry upstream/main <分支名>

# 2. 看上游是否留有带 PR 编号的 squash 提交
git log upstream/main --grep="(#608)"

# 3. 统计本人在上游的全部提交
git log upstream/main --author="itsWyatt-K" --oneline | wc -l
```

> 这份记录独立于任何个人仓库的可见性。即使本地的开发仓库不公开，上面的 PR 与提交依然可以在上游查到。
