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
| [`lingxi-vespers-ios`](https://github.com/501EUniversity/lingxi-vespers-ios) | Product · MG-02 native | 灵犀 · 晚香 SwiftUI native iOS 重写 · **build 12**(2026-05-13 晚)cumulative 89+ 项 P0:17 bug + 4 tab/Welcome/feedback + WCAG AA + microcopy + 24 i18n + 9 (build 11) i18n catch-all + 14 (build 12) contract/silent/server-auth/auth-takeover/XSS/build-gate · codex 5 轮 review loop 抓 5 大层 P0 · 立 8 新 red lines + Dynamic Type wave follow-up · SoT 8 类应扩 11 类(加 auth boundary / URL injection / build gate) |
| [`fit-pocket`](https://github.com/501EUniversity/fit-pocket) | Product · MG-03 web | 健身小本 — pocket-sized 训练计划 + 复盘 · backend Next.js + Apple Sign in/refresh routes(2026-05-13 加 · inherit lingxi r5 takeover 防御)|
| [`fit-pocket-ios`](https://github.com/501EUniversity/fit-pocket-ios) | Product · MG-03 native | 健身小本 SwiftUI native iOS · **build 2-r3**(2026-05-13 晚)Archive-ready · 4 tab + Apple Sign in + Welcome + Feedback + Profile · pocketSeal 暖橙占位 · **第 2 案例验 SoT 11 类工具化**:lint 11 类 0 P0 + codex 3 轮收敛(对比 lingxi build 12 用 5 轮)|
| [`xhs-need-radar`](https://github.com/501EUniversity/xhs-need-radar) | Pipeline | 小红书需求雷达 · 双周扫痛点 → Opus 4.7 生成 Top 3 MVP → 部署 · **v3.3**(2026-05-17 晚 · radar 接 cowork plugin · 8-skill cross-plugin chain `ba7c853`→`7e6d5b0` 5 commits · 真 e2e PASS · 10:17 / 18 artifact 真落地 · spec 质量 ≥ Cowork 501E_竞品深度调研.docx 同档 · 立 user-global red line "用 cowork plugin 不重造 PM 团队的轮子")· **v3.1+v3.2**(2026-05-17 一晚 9 个 systemic bug · S7 60min timeout+recovery / verifier G+H rubric / upstreamLibScout / Next.js scaffold / progressWatchdog SDK / staticAudit S7.5 / spec.deferred_to_v05)· 触发案例 `safari-atlas` 半人工 ship · v3.1+v3.2 改进**没在新 app 真实战验**(下次新 spec 跑 S1-S11 验贯通) |
| [`xhs-generated-apps`](https://github.com/501EUniversity/xhs-generated-apps) | Apps monorepo | pipeline 产 + 手工迁入 + design handoff · **8 app**(2026-05-17 加 safari-atlas "行远·Yonder" 旅游 itinerary AI · 真接 Claude Sonnet 38s) |
| [`501e-engineering-skills`](https://github.com/501EUniversity/501e-engineering-skills) | Plugin · ⭐ 16 skill | 工程纪律 + 商业化 baseline · battle-tested · 含 `commercial-app-ui-baseline` 全套 SwiftUI+backend 模板 |
| [`reddit-radar`](https://github.com/501EUniversity/reddit-radar) | Pipeline · WIP | Reddit 获客侦察 · 服务 Reddit + AEO/SEO/GEO 主战线 |

## 商业化双轨

- **小头** · consumer app 订阅 / 一次性付费(灵犀 + 后续 graduate)
- **大头** · 把累积的推广流程 + playbook + 工具链做成 SaaS,卖给其它 Founders

对外叙事:**绝不**卖"我们能造 X 个 app",**只**卖"我们能让你的 app 从 0 到 100 用户的可复制流程"。

---

## 📌 当前主方向(2026-05-15 更新)

接 Cowork 出的商业分析 + 竞品深度调研 · 3 条战略决定:

1. **Phase 3 SaaS 是 north-star · 2 app 是 case + 弹药**:灵犀 + Fit Pocket 不是业务本身 · 是 Phase 3 SaaS($299/月给 solo founder · 第 13 月+ 起跑)推介的方法论证明。对外叙事调整为"用 Lovable/Replit/Cursor 的服务" · 不是又一个 agentic builder。
2. **🔴 5-LOI gate · 第 9 月前必过**:Phase 3 SaaS 在建之前 · 5 个 design-partner 面访 + 收 $299/月付费 LOI · 3+ 进 / <3 改价/改受众/改 model · 不许"先建后改"。
3. **90 天聚焦灵犀**(0-30 天)· Fit Pocket Archive 但暂停 GTM 推动 · 防稀释 Phase 1 证明 + 算法降权两个账号。

威胁面已经清楚:
- 工具竞品累计 $50亿+ 融资(Lovable / Cursor / Replit / Bolt / v0) · 工具对工具 = 自杀
- **Anthropic 自家 "Claude for Small Business"** 已发(Cowork 内 15 agentic workflow · 含 Pro/Max plan) · $299/月被免费 toggle 挤压 · 必须以 done-for-you 服务侧竞争
- Mintlify($10M ARR / $250-300/月 / 中端 B2B 技术 founder)是最接近 analog · 反向工程他们 GTM

完整决策 log + 历史:[Notion · 501E 战略决策 Log](https://www.notion.so/501E-Log-34a38b3189e181edbfbefc4d0ff8835d) · [`atelier/docs/decision-log.md`](https://github.com/501EUniversity/atelier/blob/main/docs/decision-log.md)

---

## QA 系统(2026-04-24 上线 · 2026-04-29 闭环升级 · 2026-04-29 晚 双红线纠正)

共享引擎 + per-app 契约驱动 · **8 audit + multi-persona LLM judge(per_route preflight + persona.setup_query)+ ai-output-quality + reviewer + auto-fixer + health-check 6 项 + verify-deploy** 全自动闭环。

- **commercialize 全自动 supervisor 闭环**(2026-04-30 升级):Step E.5 RLS 必启 · **Step F-AUTO 调 supervisor 11-stage**(替代旧 F.5/F.7/F.8 三个 hard gate)· 失败时 supervisor 自己 spawn fixer 改源码 + push + verify-deploy · loop 5 轮 · 真 stuck(同 finding ≥ 3 次)才 escalate-to-product.md + wechat 推 Eric · **0 人工介入** · 跟 6h cron 同一引擎
- **health-check 6 项**:railway-deploy(deployment list 必 SUCCESS) · supabase-rls(public schema 必全启) · liveness · critical-routes · build-artifact · db-connectivity
- **verify-deploy 工程保险**:`atelier/agents/qa-real-device/verify-deploy.mjs` · push 后必跑 · railway deployment list 最新条 SUCCESS + curl base_url 200/302 · 否则 exit 2 — 防"git push ≠ deploy success"红线
- **Auto-fixer 退出条件**:同 finding 修过 ≥ 3 次 → 升级到产品层(`escalate-to-product.md` + 自动微信推 Eric)· 计数源 Notion findings DB hash · git log fallback
- **--until-clean**:auto-fix.mjs 真多轮 audit→fix→re-audit 循环 · 5 轮硬上限防 LLM 抽风
- **6h cron**:⏸ 暂停(2026-04-30 · 没真用户不烧 LLM)· 重启 `node atelier/scripts/install-macbook-cron.mjs`
- **跨 app contract pattern library**(2026-04-30 立):`atelier/contracts/501e-common.contract.json` 抽公共红线(PWA / i18n / a11y / 量表方向 / LLM 输出约束 / forbid AI tone)· per-app contract 继承 common · 改 common 一改全 commercial app 生效 · 第一次跑就抓出 fit-pocket P0 i18n messages 缺失
- **supervisor escalate 治本三选一**(2026-04-30 立):同 finding 修 ≥3 次升级 · architect agent 必须 explicit 选 A 改 schema / B 改交互 / C feature flag / D 归档 · 不许"换大模型再试"假治本 · stage 10b 逐条验 verify_criteria · stage 11 reflect 检测产品 bug 标 acceptable_p1 红线
- **Supabase service_role 月度轮换提醒**(2026-04-30 立):launchd 每月 1 号 9am 自动跑 · 25 天后推 wechat 提醒 · 防 leak 全暴露
- **per-app QA-WORKFLOW.md**(2026-05-01 · OpenAI Symphony 启发):每个 commercial app 根目录有 `QA-WORKFLOW.md`(YAML front matter + Markdown body)· extends `atelier/contracts/501e-common.qa-workflow.md` · supervisor + commercialize 都读 · 替代 hardcoded 常量(向后兼容 fallback)· 跟 contract 双轨(contract=什么违规 · workflow=怎么跑)
- ~~per-fixer git worktree 隔离~~(2026-05-01 实施 · 同日**回滚**)· git worktree 不带 .gitignored 的 node_modules · fixer prompt 强制 `npm run build` · 整链断 · 教训:工程级隔离改动必须真跑 supervisor 一轮验 · `git revert 587340d` → `a51dc2c`
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

---

## 📋 Commercialize Workflow · 全景图(2026-05-12 build 6 后)

从 idea 到上架 + 5 类判断累积 · 一条线 7 阶段:

```
阶段 0  需求雷达 → 阶段 1  MVP 自动生成 → 阶段 2  验证 → 阶段 3  COMMERCIALIZE (A-I 9 步 · 5 hard gate)
                                                                  ↓
阶段 4  Native client iOS(可选)→ 阶段 5  TestFlight 真用户期 0(in-app 反馈闭环 ★build 6)
                                                                  ↓
                              阶段 6  上架 + 6 维度大改 → 阶段 7  5 类判断累积 · 飞轮
```

5 个 hard gate(任一不过 ABORT 上线):
- **E.5** Supabase RLS 全启 · fit-pocket 真踩
- **F.4** ★build 6 · Native client UI baseline(tab≤4 / WelcomeView cover / SectionHero / Feedback wired)· lingxi build 5 真用户后立
- **F.5** Contract reviewer LLM 反审 8 维度
- **F.7** multi-persona LLM judge P0=0
- **F.8** Health check 6 项 PASS

详细全景图 + 人话解释 + 5 类判断:[Notion · 501E Commercialize Workflow](https://www.notion.so/501E-Commercialize-Workflow-2026-05-12-build-6-35e38b3189e181c9b1aadf7b5054d9a3)。

## 📦 Engineering Skills Plugin · 16 skill

抽自 60+ memory · battle-tested 跨 commercial app pipeline · [`501e-engineering-skills`](https://github.com/501EUniversity/501e-engineering-skills) PRIVATE alpha。

最新加(2026-05-12):**`commercial-app-ui-baseline`** — 每个 commercial app 必备的 3 件 baseline(底部 tab ≤ 4 + 共享 SectionHero + in-app feedback 闭环)· 含 9 个 copy-paste 模板(SwiftUI + backend Prisma/route + 本地 poll script)· 下次 app 直接抄。

详见 plugin README + `feedback_commercial_app_lessons_lingxi_17.md`(6 layer / 19 类 rules · 每条链回 lingxi 真出处)。

## 📱 Native Client Pipeline · lingxi-vespers-ios build 6 cumulative

- **build 1-5** · 17 bug 全 fix(Apple Sign in 字段 mismatch / onboarding 不 trigger / i18n raw key / mood 乱码 / 注销重登又弹 / history 永远空 / migration drift / race / 跨租户 · 全在真机+codex 8 轮 review loop 抓的)
- **build 6**(2026-05-12)· 加 Eric 真用户反馈 3 件:① 首页改首次弹窗(home tab → fullScreenCover) ② 4 tab(原 5)③ SectionHero 顶部一致 ④ in-app feedback 闭环
- **codex review loop** · 每 build 跑 N 轮 · 到 P0==0 才放行 Archive(build 5 跑 8 轮 · build 6 跑 1 轮)
- **真机 bug log** · `feedback_realdevice_bug_log_lingxi.md` 持续 append · 是 LLM judge / sim / static review 都看不到的护城河 layer

---

---

## 🛡 Audit Workflow 升级(2026-05-13)· 加 WCAG + Microcopy 双 audit + Claude Design 接入

`atelier` 加 2 个新 audit agent · 跟原有 LLM judge persona / contract reviewer 平行:

| Agent | 抓什么 | 跟现有 audit 关系 |
|---|---|---|
| [`qa-design-a11y`](https://github.com/501EUniversity/atelier/tree/main/agents/qa-design-a11y) | WCAG 2.1 AA 13 准则 · 对比度真 score / 触控真尺寸 / Dynamic Type / VoiceOver narrative / focus 顺序 | 跟 axe-core 互补:axe 抓 30% 技术层 · 这个 agent 抓另 70% 结构层 |
| [`qa-ux-copy`](https://github.com/501EUniversity/atelier/tree/main/agents/qa-ux-copy) | 5 原则(Clear/Concise/Consistent/Useful/Human)× 6 pattern · button label / error / empty state / CTA / onboarding | 跟 forbid_phrases(grep 黑名单)互补 · 黑名单挡暴露字样 · 这里正向审 copy 质量 |

两个 agent 都 wire 进 `qa-supervisor stage 2 audit` · `commercialize Step F-AUTO` 调 supervisor 自然带上 · 不用手动跑。`commercialize master_checklist` 加 **F.3.5 / F.3.7** gate · 任一 P0 = ABORT。

### 真验 · lingxi build 6 实跑 25 finding

build 6 codex P0==0 通过后 · 用 atelier 这 2 audit 真扫一遍 · 抓出 **3 P0 + 13 P1 + 9 P2 = 25 项**:
- **UX-Copy P0**:`common.unauth.applesignin` 文案暴露后端架构术语("apple-signin 端点接通后重试" → 用户语言)
- **UX-Copy P0**:`ProfileView` signedOutHero 5 处 hardcode 中文(没 i18n · 英文用户看到中文)
- **A11y P0**:`lingxiSeal #c4463a` on `lingxiPhoneBg #151627` 真对比度 3.6:1 < AA 4.5 · 影响所有 ≤11pt eyebrow / pressmark / tab selected label

build 7 一次清干净:`lingxiSealBright #e36b5b`(~5.5:1)替换所有小字 caps · 25 finding 全修。codex round 1 抓出我漏的 13 处残留 · sed 批量扫一遍。

→ **3 层平行**:codex 代码层 review + LLM judge persona 体验扫 + atelier audit 设计师级别 a11y/microcopy。互不可替代。

## 🎨 Claude Design 接入流程(2026-05-13)· lingxi-vespers app icon TF2

用户 → [`claude.ai/design`](https://claude.ai/design) → 5 方向 × 3 mockup + 6 TF deep dive(15 + 6 草稿)→ 选 **TF2 月夜册页 Moon Scroll**(原 TF2 是 yods/双柱 Kabbalah 符号 · Eric 嫌"宗教感太强" · Design 改成中式月夜挂轴 + 右下落款印『灵』字)→ Claude Code 接 handoff bundle(gzip tarball · 含 README + chat transcript + JSX 源 + HTML 渲染)→ 翻 JSX → SVG → `rsvg-convert -b #151627` → 1024×1024 RGB no alpha PNG → 替换 `AppIcon.appiconset/AppIcon.png` + 矢量源同存 `AppIcon.source.svg`(改色/size 直接复刷)。

→ 设计 / 工程 双向闭环:Claude Design 出方案 · Claude Code 真落地。

## 📱 Native Client Pipeline · lingxi-vespers-ios build 12 cumulative(2026-05-13 晚 替换 build 7 段)

- **build 1-5** · 17 bug 全 fix(Apple Sign in / onboarding / history / migration / 跨租户 / race · 真机+codex 8 轮 loop 抓)
- **build 6** · 4 tab + Welcome cover + SectionHero + in-app feedback 闭环(Eric 真用户反馈 3 件)
- **build 7** · WCAG AA + microcopy 双 audit 25 finding 全清 + Claude Design TF2 月夜册页 app icon
- **build 8-10** · lint Python escape silent fail retro 抓 47 i18n hardcoded + multi-round codex 抓残留 P0(ternary / lastError / multi-line) · 立 `feedback_audit_infra_self_verify` 红线
- **build 11**(commit cbc6ca4)· lint r6→r7 catch-all + multi-line array allow-list · 9 项 i18n caller(typeOptions zh tuple → en-slug canonical + legacy zh map 兼容)
- **build 12**(commit e9a5f70 + backend 3 + atelier 2)· 14 项真 P0:DELETE journal contract + profileCompletedAt rollback + 3 个 silent catch + auth refresh route + delete dead ensure + **Apple Sign in auth takeover 真修** + safeReturnTo XSS 4 处 + 3 react-hooks lint gate + atelier infra(supervisor guard / audit unavailable inject / multi-platform merge / top-N cap 去 / grep silent 真分)
- **codex review loop** · build 5 跑 8 轮 / build 6 跑 1 轮 / build 7 跑 2 轮 / build 11 跑 3 轮 / **build 12 跑 5 轮**(r1-r5 抓不同层 P0 · 5 大层覆盖)· 到 P0==0 才放 Archive
- **真机 bug log** · `feedback_realdevice_bug_log_lingxi.md` Gap 18-23 累积 · 护城河 layer
- **follow-up wave** · `project_dynamic_type_wave.md` · 82 sites `.font(.system(size:))` 无 relativeTo · 触发 fit-pocket 真起来抽 typography helper(7-12h · 字体策略 A 语义字体 vs B 自定义 Instrument Serif)

---

---

## 🛡 Findings Taxonomy · 8 大类护城河 · 应扩 11 类(2026-05-13 晚 codex r5 暴露)

Build 5 → build 12 累计 89+ 项 P0(17 build 5 bug + 25 audit finding + 9 build 11 i18n + 14 build 12 + codex 5 轮 r1-r5 ≈ 30+ + 5 atelier infra)按 pattern 分类成 **8 大类(待扩 11 类)** · 每类 build 阶段防御 + 测试阶段检测 + 真出处 · 任何新 commercial app commercialize 前 cross-check。

**已扩 3 类**(2026-05-13 晚 codex r5 暴露 → atelier `lint-findings-taxonomy.mjs` 8→11 类工具化):

- 类 9 · **Auth boundary takeover**(JWT verification gap / body-controlled user lookup / session hijack)· 真出处 lingxi apple-signin body.email lookup 漏洞 · lint pattern:`/api/auth/*` + `body.email/userId` + user lookup + 无 sanitize · allow-list E2E gated routes · **retro 验** pre-r5-fix 真抓 1 P0 ✅
- 类 10 · **URL injection / XSS / open redirect**(query 参数直接进 router.replace 或 window.location)· 真出处 lingxi OnboardingForm / signin returnTo · lint 单文件 50% · prop 链流转 audit agent 兜底(follow-up)
- 类 11 · **Build gate failure**(lint error / TS error / 失败 CI 当 ship 拦)· 真出处 react-hooks/set-state-in-effect 3 errors · lint 直接跑 `npm run lint` + `npx tsc --noEmit` exit code · **retro 验** pre-r5-fix 真抓 ✅

**真出处**:`atelier@088be77` 工具化 commit · retro test on `lingxi-vespers@7b023f5~1` 抓 2 P0(类 9 + 类 11)· 证明 lint 11 类工具化方向对 · 部分类(类 10 prop 链)需 audit agent 兜底。

| 类 | 频次 | build 阶段防御 | 测试阶段检测 |
|---|---|---|---|
| 1 · WCAG 文字对比度 | 30+(60%)| Brand/Colors.swift policy + lint-findings-taxonomy.mjs grep | F.3.5 qa-design-a11y · LLM 真算 luminance |
| 2 · UX microcopy | 15+ | microcopy_style_guide + forbid_phrases 扩展 | F.3.7 qa-ux-copy · 5 原则 × 6 pattern |
| 3 · Client↔Backend contract | 8 | preflight 字段 grep cross-check · body.userId = 红线 | F.5 qa-contract-reviewer · 8 维度反审 |
| 4 · Server-authoritative state | 4 | DB atomic INSERT ON CONFLICT · pending sync 三件套 | supervisor stage 4/5 + race test prod DB N=20 |
| 5 · Migration / schema | 3 | 真连 prod DB Node+pg 扫 | F.8 health-check + shadow schema test |
| 6 · iOS native client | 7 | Brand modifier relativeTo · nav title inline | F.4 native UI baseline + preflight 8 项 |
| 7 · Tab / page 架构 | 3 | tab ≤ 4 + SectionHero 复用 + Feedback wired | F.4 gate + commercial-app-ui-baseline plugin skill |
| 8 · Workflow process 偷懒 | meta | Karpathy 4 + 工程纪律 | codex multi-round + supervisor stage 11 reflect |

5 处工程化落实:
- **Memory** · [`feedback_findings_taxonomy_master.md`](https://github.com/501EUniversity)(local memory)· 8 大类 master index
- **Atelier** · [`scripts/lint-findings-taxonomy.mjs`](https://github.com/501EUniversity/atelier/tree/main/scripts/lint-findings-taxonomy.mjs) 快 grep + pre-commit hook · 跟 LLM audit 互补
- **iOS** · `Brand/Colors.swift` 加 WCAG AA policy 注释 · 写代码就看见 lingxiSeal vs Bright vs Deep 用哪
- **Supervisor** · `agents/qa-supervisor/prompts/reflector.md` A.5 · 自动标 finding `taxonomy_class` · 同类 ≥ 3 次升级工程保险
- **Commercialize** · master_checklist Step 0.5 · 强制 lint 跑过 0 P0 才进 Step A

Class 1 (WCAG) 占 60% · 自动化 ROI 最高。lint + audit 之后下个 app 几小时 ship 干净 · 不用 7 轮 codex 来回拉锯。

详细:[Notion · Findings Taxonomy 8 大类护城河](https://www.notion.so/Findings-Taxonomy-8-Classes-Moat-2026-05-13-35e38b3189e181b59b6bfb29c6df6531)

---

---

## ⚡ Build-Time Prevention · 4 Layers(2026-05-13 · Eric "build 阶段就避免" 工程化)

Lingxi build 7→8 真发现:即使 codex 7 轮 + qa-design-a11y + qa-ux-copy audit + 手修 · 仍有 **15 项 hardcoded 中文 i18n violation** 漏过 · 直到 atelier `lint-findings-taxonomy.mjs`(Python CJK 检测修好后)真 grep 才抓出。

→ Eric 指令:**以后任何 app 必须在 build 阶段就避免 · 不靠后置 audit 抓**。装 4 层 hook · 越早拦越好。

| Layer | 工具 | 拦截时机 |
|---|---|---|
| 1 · Pre-commit hook | `atelier/scripts/install-pre-commit-lint.mjs` 装 `.git/hooks/pre-commit` | 本地 `git commit` 前 · 秒级 |
| 2 · CI / PR check | `atelier/templates/lint-findings-taxonomy.yml` | GitHub PR / push · 秒级 |
| 3 · Commercialize Step 0.5 | `atelier/bin/commercialize.mjs` 真 spawn lint | commercialize 进 Step A 之前 |
| 4 · Fixer agent prompt | `atelier/agents/qa-supervisor/prompts/fixer-app-src.md` i18n strict 红线 | qa-supervisor stage 5 写源码时 |

→ 以后写 `Text("中文")` · 在 4 个 layer 任意一个被拦 · 不可能 ship 到 build 8 这种状况。

详细:[Notion · Build 8 + Build-Time Prevention 4 Layers](https://www.notion.so/Build-8-Build-Time-Prevention-4-Layers-2026-05-13-35e38b3189e18166a008cf95d906b2e3)

---

*Solo-ops · Built in Sonnet 4.6 + Opus 4.7 · Shanghai.*
