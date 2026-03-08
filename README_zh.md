<h1 align="center">Thinking Models</h1>

<p align="center">
  <strong>让 AI 的分析从「正确但平庸」变成「真正有洞察」</strong>
</p>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-MIT-blue.svg?style=for-the-badge" alt="MIT License"></a>
  <a href="https://github.com/Mocooa/thinking-models/stargazers"><img src="https://img.shields.io/github/stars/Mocooa/thinking-models?style=for-the-badge" alt="GitHub Stars"></a>
</p>

<p align="center">
  <a href="#快速安装">快速安装</a> · <a href="#看看区别">效果对比</a> · <a href="README.md">English</a>
</p>

---

## 为什么需要这个 Skill？

你让 Claude 帮你分析一个决策、一个战略、一个业务问题——它给你一个条理清晰、四平八稳的回答。这种回答你在公众号文章和咨询 PPT 里已经见过一百遍了。

不是说它*错*了。只是……**没什么用**。它没有告诉你任何你还不知道的事情。

问题出在哪：

- 🤔 "我该不该辞职创业？" → 给你利弊分析，**但从来不质疑「辞职 vs. 留下」这个二选一本身对不对**
- 📉 "我们流失率 15%，怎么降？" → 列 8 条标准打法，**但不问你到底有没有 product-market fit**
- 🎯 "帮我分析一下竞争格局" → 漂亮的 SWOT 表格，**但没有意外的角度，没有「你有没有想过这个」**
- 🔄 不同模型得出相同结论？很好。不同模型**互相矛盾**？→ **Claude 挑一个说，把矛盾忽略了**——可往往矛盾本身才是最有价值的洞察

Claude 已经*知道*所有思维模型——第一性原理、MECE、逆向思维、Pre-mortem、JTBD，你能想到的它都知道。但知道模型和**系统化地在正确的时机选对模型、组合使用**，完全是两回事。

**这个 Skill 就是让它真正用好这些模型的路由逻辑。**

---

## 快速安装

```bash
npx skills add Mocooa/thinking-models
```

支持 Claude Code、Cursor、Windsurf 和 [15+ 个其他 Agent](https://skills.sh)。

<details>
<summary>手动安装（点击展开）</summary>

```bash
mkdir -p ~/.claude/skills/thinking-models

# 中文版
curl -o ~/.claude/skills/thinking-models/SKILL.md \
  https://raw.githubusercontent.com/Mocooa/thinking-models/main/SKILL_zh.md

# English
curl -o ~/.claude/skills/thinking-models/SKILL.md \
  https://raw.githubusercontent.com/Mocooa/thinking-models/main/SKILL.md
```

选一个语言就行，Skill 会自动触发。
</details>

---

## 看看区别

**提问**: *"我在考虑从大厂离职创业，做 AI 教育方向，有一些积蓄但没有创业经验，帮我分析一下"*

<table>
<tr><th width="50%">没装 Skill</th><th width="50%">装了 Skill</th></tr>
<tr><td>

直接给建议：

> *"AI 教育确实是热门方向，有几个利好：市场需求真实存在、行业处于早期、大厂背景有背书价值…… 几个务实的建议：先别裸辞，在职期间先做 MVP 验证……"*

没毛病。也没什么用——和随便搜一篇创业文章说的一样。

</td><td>

先挑你的问题：

> *"你的问题里藏着三个假设：1) '创业'是唯一路径——其实从顾问到内容创作者，有很多低风险的中间形态；2) '有积蓄'不等于有创业资本；3) 'AI 教育'不是一个赛道，是一个赛道集群"*
>
> *"你把问题框成了'走 vs. 留'的二选一。但这其实是一个连续谱。"*

然后把 AI 教育拆成 5 个截然不同的细分市场，用生态位理论分析你该站哪个位置，Pre-mortem 预演怎么会死，跨心理学/系统论/生物学三个镜头交叉验证，最后抛出：

> *"把自己想象成一支股票——你不是在'辞职创业'，你是在做一次个人 IPO。"*

</td></tr>
</table>

### 跑分（3 组测试，17 项检查）

| 检查项 | 有 Skill | 没有 |
|---|---|---|
| **总通过率** | **100%** (17/17) | 29% (5/17) |
| 质疑假设 | ✅ 每次都做 | ❌ 从来没有 |
| 跨学科交叉验证 | ✅ 每次都做 | ❌ 从来没有 |
| 不寻常角度 | ✅ 每次都做 | ❌ 从来没有 |
| 领域镜头标注 | ✅ 每次都做 | ❌ 从来没有 |
| 结构化分析 | ✅ | ✅ |
| 多种方案 | ✅ | ✅ |

最后两行：Claude 不装 Skill 也能做好。前四行：**不装 Skill 就从来不做**。

多花约 2 倍 token 和 4 倍时间。需要真正有洞察的分析时，值得。

---

## 它做了什么

Claude 已经知道所有模型知识了。这个 Skill 只是**路由逻辑**——决定*什么时候*用*哪些*模型、*怎么*组合。

| 步骤 | 做什么 |
|------|-------|
| 0 | **质疑问题**——隐含假设、你问的是症状还是根因、有没有被框架锁住 |
| 1 | 匹配 11 种问题原型 → 选模型组合 |
| 2 | 拆解复合问题 |
| 3 | 三维诊断：任务类型 × 领域镜头 × 复杂度 |
| 4 | 跑分析，每个洞察标注来源镜头 |
| 5 | 生成 1-2 个不寻常角度（学科迁移、时间翻转、反事实） |
| 6 | 交叉验证：哪些镜头得出同一结论？哪些互相矛盾？缺了什么？ |
| 7 | 根据复杂度调整输出形式 |

### 里面有什么

| | |
|---|---|
| 🧠 **25+ 实用模型** | CoT、ToT、SCAMPER、第一性原理、MECE、5 Whys、逆向思维、Pre-mortem、JTBD、情景规划、贝叶斯思维…… |
| 🔭 **80+ 理论镜头** | 覆盖心理学、经济学、生物学/战略、系统论、数学/概率、增长 |
| 🗂️ **11 个元框架** | CGEC、六顶思考帽、Cynefin、OODA、Double Diamond 等 |

> Skill 不*教* Claude 这些模型——它已经知道了。Skill 告诉它**什么时候该用哪个、怎么组合才不会浮于表面**。

---

## 给人看的文档

`docs/` 目录里有参考资料，想自己了解这些模型的可以翻翻：

- [practical-models.md](docs/practical-models.md) — 25+ 模型，含使用场景和 Prompt 模板
- [mental-models-library.md](docs/mental-models-library.md) — 89 个模型，9 大学科
- [meta-frameworks.md](docs/meta-frameworks.md) — 11 个组合框架

这些是给你在 GitHub 上看的——Skill 不会加载它们。

---

## 贡献

发现问题？[提 Issue](https://github.com/Mocooa/thinking-models/issues)。想改进路由逻辑或加新的匹配模式？欢迎 PR。

## License

[MIT](LICENSE)
