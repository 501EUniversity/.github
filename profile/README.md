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
| [`lingxi-vespers`](https://github.com/501EUniversity/lingxi-vespers) | Product · MG-02 web | 灵犀 · 晚香 — 一本不做预言的玄学手札(塔罗 + 关系档案 + 日记)· Next.js + Capacitor 8 |
| [`lingxi-vespers-ios`](https://github.com/501EUniversity/lingxi-vespers-ios) | Product · MG-02 native | 灵犀 · 晚香 SwiftUI native iOS 重写 · 真 UITabBar / 翻牌 3D / RWS 78 牌 + lingxi 滤镜 / 共用 prod backend |
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

### 4-29 晚 6 轮 LLM judge 修复实战(P1 收敛 · 真闭环)

| | R1 | R2 | R3 | R5 | **TRUE FINAL** |
|---|---|---|---|---|---|
| **lingxi**(4 personas) | 6 | 4 | 2 | **0** ✅ | 0 ✅ 全 4 personas P1=0 |
| **fit-pocket**(6 personas) | 9 | 5 | 5 | 5 | **4**(5/6 personas P1=0 · 1 elder a11y escalate) |

总修了 **~50 项产品体验 bug**:塔罗抽卡 UI 放大 + 翻牌动画放慢 · /onboarding standalone confirmation · ProfileGate 三态 · RPE 1-5 反 → 1-10 行业标准 · fit-pocket Goal 枚举扩 recomp/cardio · e2e-onboard ?profile= 6 persona profile 注入 · /library badge × 肌群 layout 重设计 · abs goal 强制 2 核心专项注入(33%) · planGenerator push/pull 边界修 · 加传统杠铃硬拉 · elder 字号 4 轮迭代等。

**LLM stochastic 边界**:fit-pocket 剩 4 P1 全是 elder-low-vision 字号 a11y 同 category(修过 4 次仍抓 caps 印章 vs 字号 trade-off)· 按 escalate 纪律升级到产品层 · 4 选项(iOS Dynamic Type 治本 / elder mode toggle / 整体 caps 一刀切 / 短期 acceptable_noise)等 Eric 拍板。

### 双红线纠正(2026-04-29 晚 永久内化)

1. **`acceptable_p1_after_fixes` scope 严格** · 仅适用 LLM 自由文本生成 stochastic(塔罗解读 / insights)· **不适用** audit 抓的产品体验 bug(必须修源码) · `feedback_llm_stochastic_dont_overreach.md` 二次澄清
2. **git push ≠ Railway deploy success**(railway up 本地传模式)· `feedback_railway_up_not_git_autopull.md` 立 · 工程保险 `verify-deploy.mjs`(railway deployment list 必 SUCCESS) + `health-check.mjs` 加 `railway-deploy` + `supabase-rls` 双闸

详见 [`atelier/agents/qa-real-device/README.md`](https://github.com/501EUniversity/atelier/tree/main/agents/qa-real-device#readme) · 新 app 8 步上线 · [`atelier/README.md`](https://github.com/501EUniversity/atelier#readme)。

---

*Solo-ops · Built in Sonnet 4.6 + Opus 4.7 · Shanghai.*
