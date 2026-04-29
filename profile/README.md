# 501E · Validation + Distribution OS for solo founders

> From an idea to the first 100 users to a *replicable* growth motion — cumulative judgments, not one-off outputs.

**501E** 是两位 cofounder 在美国读大学时住过 3 年的房号。这个 org 用这个地址命名,提醒我们所有决定回到**一起发生的那个房间**。

---

## 我们不是什么

**❌ Not an app factory.** 我们不卖"用 AI 帮你做一个 app"。那东西谁都能做。

## 我们在累积的五类判断

1. **哪些需求值得做** — trend 扫描 + 真实用户痛点频次
2. **哪些产品体验会阻挡转化** — PostHog funnel + session replay 累积的卡点类型
3. **哪些分发动作是合规且可复制的** — GTM playbook(不是灰操作,是能教给别人的)
4. **哪些 skill / flow / 评估可以跨产品复用** — 这些 agent 和 checklist 的共用基座
5. **哪些经验最终可以沉淀成产品** — 选择性开放 = OpenClaw 

---

## 当前在跑的

| 仓库 | 类别 | 说明 |
|---|---|---|
| [`atelier`](https://github.com/501EUniversity/atelier) | ⭐ OS 主仓 | 商业化工作室 · 所有共享 agent / GTM / QA / data-analyst / 模板 |
| [`lingxi-vespers`](https://github.com/501EUniversity/lingxi-vespers) | Product · MG-02 | 灵犀 · 晚香 — 一本不做预言的玄学手札(塔罗 + 关系档案 + 日记) |
| [`fit-pocket`](https://github.com/501EUniversity/fit-pocket) | Product · MG-03 | 健身小本 — pocket-sized 训练计划 + 复盘 |
| [`xhs-need-radar`](https://github.com/501EUniversity/xhs-need-radar) | Pipeline | 小红书需求雷达 · 双周扫痛点 → Opus 4.7 生成 Top 3 MVP → 部署 |
| [`reddit-radar`](https://github.com/501EUniversity/reddit-radar) | Pipeline · WIP | Reddit 获客侦察 · 服务 Reddit + AEO/SEO/GEO 主战线 |

## 商业化双轨

- **小头** · consumer app 订阅 / 一次性付费(灵犀 + 后续 graduate)
- **大头** · 把累积的推广流程 + playbook + 工具链做成 SaaS,卖给其它 Founders

对外叙事:**绝不**卖"我们能造 X 个 app",**只**卖"我们能让你的 app 从 0 到 100 用户的可复制流程"。

---

## QA 系统(2026-04-24 上线 · 2026-04-29 闭环升级 · 2026-04-29 晚 双红线纠正)

共享引擎 + per-app 契约驱动 · **8 audit + multi-persona LLM judge(per_route preflight + persona.setup_query)+ ai-output-quality + reviewer + auto-fixer + health-check 6 项 + verify-deploy** 全自动闭环。

- **commercialize 四 hard gate**:Step E.5 RLS 必启 · F.5 contract reviewer 必过 · F.7 LLM judge 必 0 P0 · F.8 health-check 必 6/6 PASS
- **health-check 6 项**:railway-deploy(deployment list 必 SUCCESS) · supabase-rls(public schema 必全启) · liveness · critical-routes · build-artifact · db-connectivity
- **verify-deploy 工程保险**:`atelier/agents/qa-real-device/verify-deploy.mjs` · push 后必跑 · railway deployment list 最新条 SUCCESS + curl base_url 200/302 · 否则 exit 2 — 防"git push ≠ deploy success"红线
- **Auto-fixer 退出条件**:同 finding 修过 ≥ 3 次 → 升级到产品层(`escalate-to-product.md` + 自动微信推 Eric)· 计数源 Notion findings DB hash · git log fallback
- **--until-clean**:auto-fix.mjs 真多轮 audit→fix→re-audit 循环 · 5 轮硬上限防 LLM 抽风
- **6h cron**:macbook launchd(com.501e.atelier.qa-llm-judge)· lingxi + fit-pocket 持续监控
- **post-commit health hook**:每个 commercial app 装 git hook · 改源码后台跑 6 项 health · 不阻塞 commit
- **LLM stochastic 边界(scope 严格)**:`acceptable_p1_after_fixes` 字段**仅适用** LLM 自由文本生成(塔罗解读 / insights / 长文 over-promise·persona-drift·boilerplate)· **不适用** audit 抓的产品体验 bug(a11y / 量表反向 / badge 缺失等必须修源码)

### 4-29 晚 多轮 LLM judge 修复实战(P1 收敛曲线)

| | Round 1 | Round 2 | Round 4(round 3 修后) |
|---|---|---|---|
| **lingxi** | P1=6 | P1=4 | P1=2 |
| **fit-pocket** | P1=9 | P1=5 | P1=5(R3 引入 4 项 /library regression · R5 修) |

修了 ~40 项产品体验 bug:塔罗抽卡 UI 放大 · /onboarding standalone confirmation page · /tarot 三态拆分 · /history loading vs empty · RPE 量表 1-5 反 → 1-10 行业标准 · fit-pocket Goal 枚举扩 recomp/cardio · e2e-onboard ?profile= 6 persona · elder DONE 触控区 → 48px · L1·ROOKIE badge propagation 等。

详见 [`atelier/agents/qa-real-device/README.md`](https://github.com/501EUniversity/atelier/tree/main/agents/qa-real-device#readme) · 新 app 8 步上线 · [`atelier/README.md`](https://github.com/501EUniversity/atelier#readme)。

---

*Solo-ops · Built in Sonnet 4.6 + Opus 4.7 · Shanghai.*
