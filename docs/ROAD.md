# Toterra Roadmap / Toterra 路线图

**Status / 状态:** Active / 生效中
**Date / 日期:** 2026-09-08
**Version discipline / 编号纪律:** Development uses the pre-release p-track only — `p.<release>.<module>.<sub-item>` (max three levels). The release track `r.x.y.z` is cut from a specific p version at stabilization time and introduces no new features. / 开发计划一律只用 p 轨 `p.<发布档>.<模块>.<子项>`（最多三级）；`r.x.y.z` 为正式发行轨，只做优化与稳定、不引新功能。

## Positioning / 定位

* Toterra 为系列主内容模组（万象之土 / Land of All Things）：万物拟真生存、每个领域深度扩展、生物与地形无穷变种、玩家自由成长——全能者可达成但极难。 / Toterra is the series main content mod: hyper-realistic all-domains survival, deep expansion of every domain, endless exploration variety, free growth — mastering all is possible but extremely demanding.
* 世界改造归 Toterra：消费 Subterra 框架（`subterra-api`）重组九维世界生成、矿石按维度分布、`RegionAnnouncement` 区域命名解锁等。 / World reshaping is Toterra's job: it consumes the Subterra framework (subterra-api) to recombine the nine-dimension worldgen, ore-by-dimension distribution, RegionAnnouncement region-naming unlocks, etc.
* 世界观分层：物理层（主世界地形 / 气候 / 成矿 / 生态 / 交通物理）按 B 档拟真重写；叙事与超自然层保留 MC 世界观，真实地球物理 × 奇异异界对比为设计意图。 / Worldview layering: the physical layer is rewritten full-realism (B tier); the narrative and supernatural layer keeps the MC lore — realistic earth physics against eerie otherworlds is the design intent.

## Design Principles / 设计原则

* **无「系统」气味（2026-09-08 定，全局铁律）**：玩家侧不得出现游戏化系统——禁 HUD 面板 / 进度条 / 数值计数 / 任务日志 / 等级图标 / 系统提示弹窗。一切以**世界语言**表达：声望 = 世界对你的看法（NPC 态度、可交易与否、遭遇敌意），不为数值面板；领域成长 = 你真正会做的（配方 / 工具 / 行为），无进度条；线索与任务 = 实物（碑文、石卷、书信、遗物），贤者不给「任务」只交谈与交付物件；成贤 = 世界以贤者之礼对待你，而非解锁一个「模式」。设计文档中的术语（声望 / 领域 / 任务链等）仅为内部组织语言，玩家侧一律转译为世界实物，永不裸露。 / No "system" smell (global, decided 2026-09-08): nothing player-facing may look like a gamified system — no HUD panels, progress bars, numeric counters, quest logs, level icons, or system popups. Everything is expressed in the world's own language: reputation is how the world treats you; growth is what you can actually do; quests are physical artifacts; a sage converses and hands you objects, never a quest line; becoming a sage is the world treating you as one. In-doc terms (reputation / realm / quest chain) are internal vocabulary only — never surfaced to the player.

## Plan / 规划

六条设计线于 2026-09-08 定稿（世界线 / 交通体系线 / 生物线 / 世界观线 / 领域线 / 科技线），全部为 p 轨条目；实施顺序与子项细化随开发推进确认，未收敛的设计点明示「待细化」，不虚构占位。 / The six design lines were finalized on 2026-09-08 (world / transport / fauna / cosmology / realm / tech); all are p-track items; order and sub-items are refined as development proceeds; unconverged designs stay marked "to be refined" and nothing is invented.

* **藏录 / Ledger（通用内容登记册，Subterra 实现；2026-09-08 定）**：「贤者册」抽象**重命名通用化**，作 Subterra 框架能力落地——可注册 新领域 / 结晶世界观 / 镜像层 / 遗物条目 等世界内容，td 驱动 + API 双接口；**Toterra 消费 Sub 实现**，「贤者册」仅为其在主世界观语境的 diegetic 面貌；世界观注册契约语义仍由 Toterra 定义（前定），持久化与登记复用 Subterra Ledger。 / The "sage registry" abstraction is generalized and renamed the Ledger, implemented in Subterra (a generic content registry: new realms / crystallized worldviews / mirror layers / artifact entries; td + API); Toterra consumes it; the sage registry is only its diegetic face in the Main worldview; worldview-contract semantics stay in Toterra.

### Worldview Retention / 世界观保留清单（2026-09-08 定）

* 四块保留沿用（用户拍板）；清单外内容随拟真重写或待定。 / Four pillars retained (user decision); unlisted content is rewritten or pending.

| Pillar / 块 | Retained / 保留内容 | Link to realism / 与拟真层衔接 |
| --- | --- | --- |
| Nether & End / 下界与末地 | 异界维度存在与身份 | 与拟真主世界对比；不参与主世界物理拟真 |
| Magic & Arcana / 魔法·奥术 | 附魔、炼药、末影珍珠的奥术语义 | 传送压制≠移除，传送为奥术领域进阶解锁（见交通线） |
| Villager civilization / 村民文明 | 村庄贸易、掠夺者灾厄 | 社会学保留，行为层可按拟真微调 |
| Ancient ruins / 上古遗迹 | 要塞、远古城市、堡垒的上古叙事 | 文明遗迹压在真实地层之上 |

### Cosmology Line / 世界观线（三世界观宇宙学，2026-09-08 定）

* 三世界观，各三线（正 / 中 / 反）+ 特殊存在；相互独立又彼此影响，贤者知晓真相；混合制声望；影响载体 = 事件联动 + 势力·维度扩张 + 探索任务链。 / Three worldviews, each with three alignment lines plus special beings; independent yet inter-influencing; sages know the truth; hybrid reputation; event links + faction-by-dimension expansion + quest chains.

| Worldview / 世界观 | Stage / 场域 | Justice / 正线 | Neutral / 中线 | Anti / 反线 | Special / 特殊存在 |
| --- | --- | --- | --- | --- | --- |
| Main-realistic / 主·现实 | 主世界（拟真层） | 村民 | 女巫 | 灾厄 | 铁傀儡守护叙事 |
| Legend / 传奇 | 下界 / 不死传说 | 猪灵 | 骷髅 | 凋零系 | — |
| End / 末影 | 末地 / 虚空渗透 | 末影人 | 潜影贝 | 末影螨 | 末影龙 |

* 玩家关系（混合制）：声望可并存同刷，深度内容（名册 / 传承 / 特有装备）单选一个主立场——契合领域专精。 / Hybrid: reputations coexist for farming, but deep content (codex / heritage / exclusive gear) requires one primary alignment.
* 贤者（后二者合体，非旅行者）：贤者藏于稀有隐藏据点；另有遗迹 / 圣所碑文承载贤者知识（接上古遗迹保留块）。寻得后解锁世界观 lore 与专属任务链。 / Sages live in hidden strongholds and their knowledge survives in ruin inscriptions (tie-in with ancient ruins); finding them unlocks lore and quest chains.
* 势力扩张按维度不按地貌：世界观势力在各自维度扩张（猪灵商会打通下界↔主世界贸易前哨、潜影贝巢城于末地聚合、灾厄军团于主世界集结），一图变动泄压到另一图。 / Faction expansion is dimension-bound, not terrain-bound; one domino tips the others.
* 开放扩展（2026-09-08 定）：世界观注册契约**内置于 Toterra**（非 Subterra）；第三方经数据包（纯 td 声明）或模组（td + 代码钩子）添加新世界观；跨世界观 `links` 事件链接**全开放声明式**，任何注册世界观可参与联动与泄压；第三方依赖 = Subterra + Toterra。 / Open extension: the worldview registration contract is built into Toterra; third parties add worldviews via datapacks (pure td) or mods (td + code hooks); cross-worldview `links` are fully open and declarative; prerequisites = Subterra + Toterra.
* 支线机制（2026-09-08 定）：世界观内除主三线（`kind=main`）可声明支线（`kind=side`）。**平衡态铁律**——无玩家时世界不自动演进（支线不扩张 / 不冲突 / 不刷事件，零后台开销）；**晋升 = 玩家驱动**（声望 / 专属任务链 / 击败现任主线领袖），达阈值支线升主线、原主线退为支线（可再顶回）；晋升可触发跨世界观 `links`；**冲突处理 = 玩家手动择一晋升**，他线保持平衡态。机制三世界观通用，首批支线在主世界观（僵尸「皮死者之潮」/ 吸血鬼「夜行血亲」/ 精灵「自然秘术遗民」）。 / Side-line mechanism: worldviews declare `kind=side` lines beyond the main three; equilibrium rule (no autonomous evolution without the player; zero background cost); promotion is player-driven (reputation / quest chain / defeating the current main-line leader), demoting the old main line (re-promotable); promotion fires cross-worldview links; on tie the player picks one promotion; generic across worldviews, first batch in Main (zombie / vampire / elf).
* 势力同盟（2026-09-08 定）：任意势力（主 / 支线，可跨世界观）可声明缔结同盟；同盟改变势力扩张与事件联动走向（结盟互助、共享声望事件），经 `links`/新 `allies` 表声明。 / Faction alliances: any lines (main or side, possibly cross-worldview) may declare alliances; alliances reshape expansion and event dynamics, declared via `links`/`allies`.
* 种子化平衡态（2026-09-08 定）：无玩家的初始平衡态由**世界种子**确定性派生——不同种子下各线初始倾向、支线接近晋升的程度、势力亲疏各不相同；同种子完全一致。 / Seed-determined equilibrium: the no-player baseline is deterministically derived from the world seed; each world's cosmological opening differs, identical for the same seed.

#### Player entry & self-building / 玩家开局与自建（2026-09-08 定）

* 开局：出生主世界观、不属于任何势力、无初始声望——即系统内的「空白起点」。 / Start: spawned in the Main worldview, faction-free, zero reputation — the blank start of the system.
* 发现双通道：**线索**（贤者碑文 / 遗迹 / 隐藏据点，知识层，缓慢）+ **机遇**（支线遭遇 / 势力事件 / 同盟动向，事件层，突发）；两通道交汇处即玩家抉择点。 / Discovery via two channels: clues (knowledge layer) and opportunities (event layer), converging at the choice points.
* 自建三角（三者皆有，2026-09-08 定）：
  * **自建势力**（阵营层）：玩家派系注册入宇宙学，可结盟 / 参与势力扩张 / 积累声望，成为主世界观主线晋升候选（与 NPC 主线·支线竞争）。 / Own faction: registers into the cosmology; may ally, expand, gain reputation, and compete for the Main main-line throne.
  * **自建聚落**（场所层）：村落建设（占地 / 人口 / 防御 / 贸易航线），接村民文明与交通线，是自建势力的物理基座。 / Own settlement: colony building tied to villager civilization and transport; the physical base of the own faction.
  * **自建世界观**（叙事层）：「贤者立卷」——贤者记录玩家与势力所为成文，传奇度达标后结晶为**可注册的新世界观主体**（游戏内叙事路径；开发者路径仍为注册契约），供其他存档 / 多人世界探索。 / Own worldview: sage chronicles of player deeds crystallize into a new registered worldview once legendary (in-game narrative path; the dev path stays the contract), explorable in other saves/servers.

#### World truth & sage chronicle / 世界真相与贤者立卷（2026-09-08 定）

* 核心命题（宇宙学内核）：**世界观 = 结晶化的叙事层**。主·现实 = 持续推进的「现在层」（B 档物理拟真为其语法）；传奇 / 末影 = 两次被封存的历史层（传奇 = 被遗忘的愤怒，末影 = 边界与外）；上古遗迹 = 诸层分裂前的同源纪元残留；魔法奥术 = 层间渗漏的「溶剂」（故传送归奥术领域解锁）；贤者立卷 = 宇宙学运行本身——玩家结晶新世界观即系统执行现场。 / Core thesis: worldviews are crystallized narrative layers. Main = the ongoing now-layer; Legend / End = sealed historical layers; ruins = pre-schism origin-epoch remnants; arcana = solvent leaking between layers (hence teleport unlocks via the arcana realm); the sage chronicle is the cosmology executing — a player-crystallized worldview is the system in action.
* 贤者三卷（每卷对应一层真相）：**骄阳卷**（现在层起源）· **白骨卷**（传奇层失落）· **星钥卷**（末影层边界）；三卷各挂主管世界观事件作解锁阈值——白骨 ⇒ 传奇线事件、星钥 ⇒ 屠龙后解锁、骄阳 ⇒ 主世界文明推进。 / Three sage tomes: Sunrise (now) / Bone (legend) / Star-key (end); each unlock gated by its worldview's events.
* 立卷机制：记录源 = 行为事件流（声望 / 枢纽 boss / 支线晋升 / 聚落成就）；传奇度谱系 = 平凡 → 事迹 → 传奇 → **神话级阈值**；封卷即生成新世界观 td 注册（三线结构由玩家混合制主立场推断，自建势力成其创始正线）；**无玩家不推进**（与种子化平衡态同源）。 / Chronicle mechanics: event stream → legendary tiers → mythic threshold seals a new worldview registration; no-player-no-progress.
* 终局（**真相开放**，非单一大结局）：真相是客观事实（结晶—层叠—补写）；玩家立场选择只决定自身势力 / 线的走向，世界继续运转。 / Open truth: objective mechanism, no single ending; player stance shapes only their own lines.
* 封卷实感（**可进入的镜像层**）：封存的层作镜像场景供其他存档 / 多人进入，体验固化的传奇时刻——无尽探索推向「探索他人封存的传奇层」。 / Sealed layers become enterable mirror scenes — exploration of others' crystallized legends.

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.1.8 | Cosmology mechanics / 世界观机制：注册契约（td 声明 / 模组钩子，links 全开放）+ 三线声望（混合制）+ 势力同盟（`allies`，跨世界观可结盟）+ 种子化平衡态 + 支线机制（`kind=side`，平衡态 / 玩家驱动晋升 / 冲突择一）+ 玩家自建三角（势力 / 聚落 / 贤者立卷世界观）+ 贤者结构（隐藏据点 + 遗迹碑文）+ 新内容填充（末影鲸 / 末影圣所 / 潜影巢城 / 虚空裂隙 / 骷髅王座 / 猪灵商会驻点 / 凋零祭坛 / 村庄行会 / 灾厄军团行军 / 女巫密会 / 僵尸 / 吸血鬼 / 精灵） | planned / 已立项 |
| p.1.9 | Inter-worldview dynamics / 跨世界观影响：事件联动（枢纽 boss 重排）+ 势力·维度扩张 + 真相任务链（贤者三卷：骄阳 / 白骨 / 星钥）+ 贤者立卷（传奇度谱系 → 封卷结晶新世界观 → 镜像层可入） | planned / 已立项 |

### World Line / 世界线 — B 档 TFC 式彻底拟真

* 经拍板：世界默认档为 B（完全替换），仿 TerraFirmaCraft 真实地理。TFC 为 EUPL-1.2（强 copyleft），定为机制级 clean-room 参考——玩法设计不受版权保护，实现与资产全部自研。 / User decision: default world tier is B (full replacement), modeled on TerraFirmaCraft's realistic geography. TFC is EUPL-1.2 (strong copyleft) — mechanism-level clean-room reference only; implementations and assets are all self-made.

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.1.0 | Content-line skeleton / 内容线骨架：消费 Subterra worldgen API（SurfaceRules 装配点 / 预设备选）+ 结构护栏 + 矿物按维度分布前置注册 | designed / 已定 |
| p.1.1 | Litho strata / 岩性地层：litho 维度换 StrataAlgo（区域分层 + 岩石类型组态，td 定义），首个「维度独立换算法」验证 | planned / 已立项 |
| p.1.1 | Ore by parent rock / 矿石按母岩：mineral × {岩石类} 前置规则 + 矿脉走向，接结构护栏防重叠 | planned / 已立项 |
| p.1.1 | Climate-driven vegetation / 气候驱动植被：climate → vegetation 接缝（温度 / 降雨 / 蒸散 → 植被带） | planned / 已立项 |
| p.1.1 | World preset × realm link / 世界预设 × 领域联动：不同预设资源分布不同（供 Realm Line 消费） | planned / 已立项 |

### Transport Line / 交通体系线

* 思想：修路 = 探索循环的推进器（修路 → 移动强化 → 探索更远 → 区域命名 → 地图 → 新路）。 / Roads are an exploration-accelerator loop.
* 三语族分工：硬路稳 / 冰场快 / 轨道重；重量与承重是交通语义的核心。 / Three families: stable hard roads, fast rinks, heavy rails; weight and load capacity are core.
* 传送全面压制（压制≠移除，2026-09-08 口径修正）：平民环境收弱鞘翅 / 末影珍珠 / 冰船，陆地交通成为第一价值；传送能力保留为奥术领域进阶解锁（见世界观保留）。 / Teleport suppression (suppress ≠ remove): civilians lose elytra / ender-pearl / ice-boat shortcuts so land transport matters; teleporting returns as a later arcana-realm unlock (see worldview retention).

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.1.2 | Motion facets / 状态面扩展：blocks.td 由三面（speed / friction / sticky）扩至十一面（+8：jump / fall_safety / turn / slip / inertia / states 触发表 / break_w 承重 / break_t 碎裂），向后兼容 + 探针 | planned / 已立项 |
| p.1.3 | Hard roads / 硬路语族：土径 → 砂砾 → 石板 → 夯道分档（系数表 td），路网识别（连续方块识别 + 路网等级） | planned / 已立项 |
| p.1.4 | Ice dual model / 冰双模型：裸冰（变慢·变滑·惯性难停·承重碎裂·特殊状态 stumble/slide）vs 滑冰场（冰下保温层方块改写运动面 → 高速可控），不同冰种系数 / 承重 / 滞时不同 | planned / 已立项 |
| p.1.5 | Rails / 轨道语族：矿车重制（木 / 石砟 / 铁轨 + 坡度限制 + 下坡蓄力 + 货运车斗），重货干线定位 | planned / 已立项 |
| p.1.6 | Realm link / 专精联动：筑路 / 冰运 / 铁路三方向深度解锁（供 Realm Line 消费） | planned / 已立项 |

### Fauna Line / 生物线 — 现实生物学，性能优先

* 三大支柱：生理（体重 / 体质 traits + home terrain mastery）、生态（食物链 + 季节行为 + 社群 / 领地）、行为（驯化三维度 + 智力分级）。 / Three pillars: physiology, ecology, behavior.
* 性能纪律（拍板优先项）：AI 分级预算桶（反射 / 回避 / 计划）；分区空间索引杜绝每 tick 全局扫描 O(n²)；亚种 traits 由区域种子哈希确定性派生（零运行时遗传算法）；spawn 密度锚定复用 Subterra 激活范围优化；季节用全局调度器而非逐实体时钟。 / Performance is a hard prerequisite (see rows).

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.1.7 | Physiology / 生理层：体重（消费重量体系）+ traits（运动 facets：体重 / 体质包 / home terrain mastery，确定性派生）+ **生理分类继承体系**（2026-09-08 定）：分类即模板 / Fauna classes are templates，详下 | planned / 已立项 |
| p.1.7 | Ecology / 生态层：食物链 + 捕食密度平衡 + 季节行为（迁徙 / 换毛 / 冬眠 / 繁殖季），fauna 维度算法第一实装 | planned / 已立项 |
| p.1.7 | Behavior / 行为层：驯化三维度（幼年印记 / 食物贿赂 / 信任积累）+ 智力分级（预算分级） | planned / 已立项 |
| p.1.7 | Variance / 变种：区域种子确定性亚种（毛色 / 体型 / 习性）+ 罕见物种与迁徙走廊作探索目标 | planned / 已立项 |

#### Physiology detail / 生理分类继承体系（2026-09-08 定）

* 不同类生物按其生理特征划分分类轴，每类给一份「运动基包」（十一面 facets 默认值 + 方块系数模板），物种在此之上仅做覆盖——两级继承（分类模板 → 物种覆盖）。 / Animals are grouped by physiology into classes; each class defines a motion base pack (eleven-facet defaults + block-factor template); species only override on top — two-level inheritance (class template → species override).
* 分类轴：足型/步态（有蹄 / 爪掌 / 趾行 / 蹼足 / 节肢多足 / 鳞足爬行 / 无足滑动 / 羽足）· 体型质量档（轻 / 中 / 重 / 巨型，决定体重基数 → break_w 与驮载）· 被覆物（毛皮 / 角质 / 鳞 / 甲壳，修正摩擦与粘滞）· 运动介质（陆行 / 攀爬 / 水栖 / 滑翔 / 飞行）。 / Axes: foot/stride, mass tier, integument, locomotion medium.
* 配置量级 O(分类×方块)+O(物种覆盖)，取代 O(物种×方块)；方块系数表即 blocks.td per-mob 的抽象层（fauna_class 模板 + mobs overrides）。 / Config cost drops from O(species×block) to O(class×block)+O(overrides); the factor table is the per-mob abstraction of blocks.td.
* 咬合：破冰阈值走 break_w（重型/有蹄易裂，轻/蹼稳）、滑倒概率走 slip（与冰双模型闭环）；亚种 traits 仅在类窗口内浮动（生理边界决定变种天花板）；加载期预计算 `分类×方块材质→系数` 常表，零运行时推导。 / Interlocks: ice break via break_w, stumble via slip; variant traits float only within class bounds; load-time precomputed constant table for O(1) lookup.

### Realm Line / 领域专精（灵魂玩法，p.2 轨起）

* 总原则（2026-09-08 定，**否决点数稀缺制**）：**自由优先**——MC 的灵魂是自由，不给玩家设固定框架与领域点硬上限。玩家可精通**全领域**，只是**极难达成**；「只能精通少数」是涌现结果而非规则。 / Overriding principle: freedom first — no realm-point caps or fixed fences; mastering all realms is possible but very demanding; "few realms in practice" emerges from depth, not rules.
* 领域成长 = 开放深层成长树：每领域一条连续成长线（入学 → 深层，无硬顶），逐级投入递增（行为事件流 / 资源 / 仪式），曲线**前快后慢**；成长可累积不可洗点（记忆属于现实，洗不掉）。 / Open deep growth trees per realm, un-capped, escalating costs, front-loaded then steep; growth is cumulative and never resettable.
* 正交解耦：**领域成长（技能）** × **世界观主立场（意识形态）** 互不锁死；领域决定你会干什么，立场决定你站在哪。 / Realm growth orthogonal to worldview alignment.
* **贤者之路（全能者的顶点）**：跨领域成长累积达「神话」阈值后，玩家可选**成贤**——成为宇宙学的观察者 / 记录者（读全部碑文、立卷之权、可自拟世界观规则），亦可继续作凡人玩家；贤者不是 NPC 专属，是玩家的终极人生选项，与「贤者立卷」机制闭环。 / Sage path: at mythic breadth the player may become a sage — the cosmology's observer / recorder; sages are not NPC-exclusive; the player's ultimate life choice, closing the loop with the sage-chronicle mechanic.
* 存档与性能：领域成长档案 = 行为事件流累积（td/zd），零全局模拟、零热路径开销。 / Save-side deterministic ledger; no global simulation or hot-path cost.

#### Realm catalog / 领域清单（第一批 12，2026-09-08 定）

* 内置第一批 12 领域，覆盖全部内容线；领域可经注册契约（td 声明）扩展，第三方可增补。 / First batch of 12 realms covering all content lines; realms are extendable via the contract.

| Realm / 领域 | Line / 对应线 | Note / 说明 |
| --- | --- | --- |
| 地质 Geology | 世界线 | 矿脉 / 地层 / 勘探（B 档拟真成矿） |
| 农垦 Farming | 生存基盘 | 耕作与作物（B 档） |
| 博物 Naturalism | 生物线 | 识别 / 驯养三维度 / 生态知识 |
| 冶金 Metallurgy | 科技线 | 提炼与合金（接母岩成矿） |
| 工匠 Mechanism | 科技线 | 机巧 / 装配 / 逆向试作 |
| 草药 Herbalism | 世界观·女巫 | 药学制剂（中立线知识） |
| 奥术 Arcana | 世界观·魔法 | 层间溶剂 / 附魔炼药 / 传送解锁 |
| 考古 Antiquary | 世界观·遗迹 | 碑文 / 遗物解读（逆向辨识层） |
| 天文 Astronomy | 探索 | 观星 / 时令 / 航海辨向 |
| 商道 Trade | 世界观·村民 | 交易 / 会商（村民·猪灵·自建聚落） |
| 战技 Warfare | 世界观·灾厄 | 武备与征战防卫 |
| 交通 Wayfare | 交通线 | 三语族统一领域（硬路 / 冰道 / 轨道三支） |

#### Realm invention / 研究新领域（2026-09-08 定）

* 玩家可研究并**创立新领域**——第一批 12 不是封闭清单（玩家成为领域作者，与自建世界观同一作者位）。 / Players can research and establish brand-new realms; the first 12 are not a closed list.
* 成型 = **纯涌现自持名**：长期打磨一套不属于任何现有领域的技艺（驯龙 / 自创法门），重复实践使其自然凝成雏形并**自持其名**；无贤者仪式、无捏造菜单（diegetic）。 / Emergence + self-naming: prolonged novel practice crystallizes a new realm with its own name; no ritual, no menu.
* 去向 = **可共享注册**：新领域写入通用「藏录 / Ledger」（Subterra 实现），跨存档 / 多人可引用、可被探索。 / Shareable: new realms register into the Ledger (Subterra), cross-save and multiplayer.
* 代价：创立需领域成长累积 + 相关领域交叉（科研重投入），成长曲线同法则。 / Cost: deep investment and cross-realm intersections; same growth law.

#### Gate wiring / 挂点接线表（p.2.1，2026-09-08 一稿）

* 挂点 = 领域成长树上挂的「世界产物」；门槛档位 = 领域内投入分档（浅尝 / 熟练 / 精通；特殊档：领域交叉、跨领域神话级）。档位为内部语，玩家侧只透过「会不会 / 能不能做」自然生效（无系统气味）。世界生成（地层 / 气候 / 矿脉）为世界侧执行，不设玩家门（预设 × 专精联动见世界线）。 / Wires = world artifacts gated on a realm's growth; tiers are internal vocabulary — players only feel them as "can I do this". Worldgen itself is world-side and ungated (~preset×realm link in the World Line).

| 挂点 Content | 领域 Gate | 档位 Tier |
| --- | --- | --- |
| 矿物辨认 / 找矿、矿脉走向 | 地质 Geology | 熟练 |
| 母岩直觉（按岩层预判成矿） | 地质 Geology | 精通 |
| 提炼 / 合金工艺 | 冶金 Metallurgy | 熟练 / 精通 |
| 硬路高档（石板 → 夯道）+ 路网识别 | 交通 · 硬路支 | 熟练 |
| 滑冰场保温层（冰道可控快线） | 交通 · 冰道支 | 熟练 |
| 重载轨道 / 货运车斗 | 交通 · 轨道支 | 精通 |
| 矿车斜坡 / 下坡蓄力 | 交通 · 轨道支 | 熟练 |
| 物种识别 / 生态知识 | 博物 Naturalism | 熟练 |
| 驯化三维度（印记 / 贿赂 / 信任） | 博物 Naturalism | 精通 |
| 附魔 / 炼药 | 奥术 Arcana | 熟练 |
| 传送（层间溶剂本体） | 奥术 Arcana | 精通 |
| 遗物辨识 / 碑文解读 | 考古 Antiquary | 熟练 |
| 铭文 → 超越钩子（贤者识货） | 考古 Antiquary | 精通 |
| 制药（含与女巫中立知识） | 草药 Herbalism | 熟练 |
| 时令 / 航海辨向 | 天文 Astronomy | 熟练 |
| 观星预言 / 跨季知识 | 天文 Astronomy | 精通 |
| 村民 / 猪灵交易会商 | 商道 Trade | 熟练 |
| 商会扩张 / 跨世界观贸易 | 商道 Trade | 精通 |
| 聚落防御 / 征伐 | 战技 Warfare | 熟练 |
| 灾厄对抗进阶 | 战技 Warfare | 精通 |
| 自建势力（阵营层） | 任意领域 Any | 熟练 |
| 自建聚落（场所层） | 任意领域 Any | 浅尝 |
| 复刻遗物（构造信息） | 工匠 Mechanism | 浅尝 |
| 改良遗物（材料研究） | 工匠 Mechanism | 熟练 |
| 超越 / 原理级创新 | 工匠 Mechanism | 精通 |
| 研究新领域 | 领域交叉 Cross | 涌现（无硬门） |
| 成贤 / 立卷 / 镜像层 | 跨领域 Mythic | 神话级 |

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.2.0 | Realm growth trees / 领域成长树：realm id + 层级投入曲线 + 配方（td schema），事件流 → 成长 | planned / 已立项 |
| p.2.1 | Gate wiring / 跨领域挂点接线：世界 / 交通 / 生物 / 世界观各内容的领域门槛（挂点表一稿已定，详上） | designed / 已定（一稿） |
| p.2.2 | Sage path / 贤者之路：成贤阈值（神话级）+ 贤者能力（读碑 / 立卷 / 拟规则） | planned / 已立项 |

### Tech Line / 隐型技术线（2026-09-08 定）

* **定义**：科技不预设技术树——玩家初始**零技术知识**，仅凭直觉（燧石割裂 / 生火 / 简单工具），科技史 = 发现史。 / No preset tech tree: the player starts with zero technical knowledge, relying on intuition; technology is a history of discovery.
* **获得通道（diegetic）**：① 意外发现前人成果（遗迹残件 / 图纸拓片 / 工具样例 → 逆向拆解）；② 接触文明（村民手艺人、贤者、猪灵商会的经验传授）；③ 实践验证（学会 ≠ 领悟，需在动手使用中掌握）。 / Acquisition: discovering predecessors' works in ruins, learning from civilizations, mastering through practice.
* **推动发展**：在学得的基础上**创新推进**（设计新物件 / 新机械），新人造物反哺世界（更优工具、可造更强基建）——技术是可扩展的，玩家可把科技推过前人。 / After learning, the player innovates and pushes technology beyond the ancestors; new artifacts feed back into the world.
* **横向底座定位**：技术 = 通用学识层，发明深度由相关领域限定（如铁轨 = 筑造技术 × 铁路领域），与 Realm p.2.1 挂点接线合并核对。 / Tech is a horizontal base; invention depth is gated by realms (joined with the p.2.1 gate wiring).
* **与前人成果 / 世界观衔接**：遗迹遗物 = 同源纪元技术（接上古遗迹保留块）；贤者 = 知识层；跨世界观技术流成立（传奇猪灵冶炼、复现主世界技艺）。 / Ruins carry origin-epoch tech; sages are the knowledge layer; cross-worldview tech exchange exists.
* **无系统气味**：无科技树 UI / 无科技点数 / 无研发队列；进步只透过「你能做出 / 能互动的事」呈现。 / No tech-tree UI, no tech points, no research queues; progress shows only through what you can make and do.

#### Tech detail / 遗迹逆向拆解机制（2026-09-08 定）

* 五步闭环（全程 diegetic，无进度条，「能否做成」即进度）：**① 检视**（观物得零件视认 / 材料提示 / 磨损铭文）→ **② 拆解**（拆卸台方块内动手，出零件样件；失败 = 部件断裂）→ **③ 试作**（按揣摩组态反向组装 / 触发，成功 = 反向原型 = 「会了」）→ **④ 复现**（自家工坊稳定复刻，掌握程度唯一读数）→ **⑤ 超越**（换材 / 改良 / 原理级创新，接 p.2.4）。 / Five-step loop (all diegetic, no progress bar): inspect -> disassemble (on a disassembly bench) -> reverse-prototype -> replicate (stable output is the only mastery gauge) -> transcend (improve / innovate, feeds p.2.4).
* 领悟四层：**辨认**（检视 / 贤者识货）→ **复刻**（拆 + 试作）→ **改良**（复刻 + 相关领域）→ **超越**（改良 + 领域精通级）。 / Comprehension tiers: identify, replicate, improve, transcend.
* 信息与缺损：遗物信息 = 构造 / 材料 / 铭文；拆坏且未修复 → **该件**信息永久缺损，**同类遗物可补全相同知识块**（驱动为补全而探索）。 / Broken artifacts lose info per-piece; same-kind artifacts complete the same knowledge blocks (exploration hook).
* 知识永久性（2026-09-08 定）：领悟的知识**永久保留、永不遗忘**（与 Realm 不可洗点一致）；失败只损材料 / 工具 / 该件信息，不损已学。 / Learned knowledge is permanent (consistent with realms); failure costs materials/tools, never learned knowledge.
* 事件流咬合：检视 / 拆解 / 试作全过程计为行为事件（喂贤者传奇度 + 领域成长）；遗物清单 td 声明、按遗迹类型 × 种子确定性生成，第三方可扩展。 / Whole loop feeds the event stream; artifact catalog is td-declared, seed-deterministic, extendable.
* 工具与工作台：拆卸台（新方块，世界内工作台式交互，非系统面板）+ 锉 / 凿 / 小锤（可耗损工具）。 / Tools: a disassembly bench block plus wearing file/chisel/hammer.
* **遗物四类（td dtype）**：器械（构造侧重 → 机械零件）/ 器皿（材料侧重 → 冶炼铸艺）/ 图籍（铭文侧重 → 直接知识 / 贤者线索）/ 标本（材料细分 → 配方参考）；识别 = 「看着像器物」，**无高亮**。 / Four artifact kinds steering info emphasis; spotted by look, never highlighted.
* **拆卸台交互**：三槽 = 检视（免耗）· 拆解（锉凿锤，选部位 + 力道）· 试作（台面格拼组）；力道三档：轻柔（慢·高成）· 常规 · 粗暴（快·高断裂风险），纯物理隐喻无百分比；产出 = 零件（实体物品，可交易 / 可损坏）+ 残渣 + 铭文撕片。 / Three actions, three force tiers (no percentages); output parts, residue, inscription scraps.
* **信息三维**：构造 → 复刻可；材料 → 改良可；铭文 → 辨认与超越（铭文挂世界观钩子，可指向某线 / 贤者线索）；通道 = 检视（劣）→ 拆解（+）→ 试作（++）→ 贤者识货（铭文+，绝不代拆）。 / Three info dimensions; sages identify but never take the tools from your hands.
* **试作与「会了」**：零件按揣摩组态摆放（无提示），正确 = 反向原型；错误 = 散架（零件可回收 · 耗时）或组态卡死（需重拆）；原型 + 工坊稳定复现 2–3 次 = 技艺永久保存。 / Reverse prototype; mastery = stable replication twice or thrice.
* **复现稳定性**：新学低产出率，随复现次数趋稳（读数 = 做出几件，非进度条）；材料纯度 / 工具品质介入（冶金 · 工匠领域）。 / Output stabilizes with practice; mastery read as pieces made, never a bar.
* **失败范围（2026-09-08 定）**：拆坏**仅伤部位**——零件变废料、该件该部位信息缺损（同类补全为唯一挽回）；整件永不报废。 / Breakage damages parts only; the artifact itself never destroyed.
* **拆链阶梯（2026-09-08 定，T0–T4）**：技术分阶 = 逆向工具升级链——「第一件逆向 = 拆卸工具自己」：T0 直觉（石凿 / 手锉）→ T1 简易器（拆卸台）→ T2 机械（锉磨 / 车削）→ T3 精密（光学 / 精工）→ T4 符械（奥术交叉）。 / Tool-chain ladder T0–T4; the first reverse-engineered thing is the disassembly tool itself.
* **生成规则**：遗物按遗迹类型 × 种子确定性生成（td 清单，可扩展）；rarity = 常见残件 / 少见完整器械 / 稀有图籍·铭文完整件。 / Seed-deterministic generation; three rarity tiers.

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.2.3 | Intuition & discovery / 直觉与发现：零知识开局（凭直觉原始制作）、遗迹技术遗物（逆向）、文明接触学习（手艺人 / 贤者 / 商会） | planned / 已立项 |
| p.2.4 | Push & tiers / 推进与分阶：学得基础上创新（新设计 / 新机械），分阶仅以「能做之事」呈现，跨世界观技术交流 | planned / 已立项 |

## Discipline / 纪律

* 小任务逐个提交：每完成一个小任务即报告并提交一次，得确认后再做下一个。 / Small tasks are submitted one at a time; each is reported and committed before the next starts.
* 所有子任务完成后统一 review + 清理 + 推送。 / After all sub-tasks complete: one review, cleanup, and push.
* 验收确定性优先（服务端开服、客户端进世界、断言全 PASS）。 / Acceptance is determinism-first (server boots / client enters world / assertions PASS).

## Progress Log / 进度记录

* 2026-09-08 — 内容线初稿落盘：世界线（B 档 TFC 式彻底拟真）、交通体系线（十一面状态包 / 三语族 / 冰双模型 / 传送全面压制）、生物线（现实生物学三大支柱，性能优先）；TFC（EUPL-1.2）定为机制级 clean-room 参考。 / First content-line draft: world line (B, TFC-style full realism), transport line (eleven-facet state pack / three families / ice dual model / full teleport suppression), fauna line (real-biology pillars, performance-first); TFC (EUPL-1.2) adopted as mechanism-level clean-room reference.
* 2026-09-08 — 世界观保留定案：物理层拟真重写、叙事/超自然层保留（下界与末地 / 魔法奥术 / 村民文明 / 上古遗迹四块）；传送压制口径修正为「压制≠移除」。 / Worldview retention decided: physical layer rewritten, narrative/supernatural layer retained (Nether & End / magic / villagers / ancient ruins); teleport-suppression wording fixed to "suppress ≠ remove".
* 2026-09-08 — 世界观线定案（p.1.8–1.9）：三世界观 × 三线（主·现实 / 传奇 / 末影，正·中·反 + 特殊存在）；混合制声望（深度内容单选主立场）；贤者 = 隐藏据点 + 遗迹碑文；影响载体 = 事件联动 + 势力·维度扩张 + 真相任务链；新内容提案 10 项入 p.1.8。 / Cosmology line decided: three worldviews × three lines; hybrid reputation; sages via hidden strongholds + ruin inscriptions; influence via event links + dimension-bound faction expansion + truth quest chains; ten new-content proposals into p.1.8.
* 2026-09-08 — 世界观开放扩展定案：注册契约内置于 Toterra（数据包纯 td / 模组 td+钩子），links 跨世界观链接全开放声明式。 / Worldview open-extension decided: registration contract lives in Toterra (datapack pure-td / mod td+hooks); cross-worldview links are fully open and declarative.
* 2026-09-08 — 支线机制定案：`kind=side` 三世界观通用；平衡态铁律（无玩家不演进，零后台开销）；晋升 = 玩家驱动、冲突择一；首批支线在主世界观（僵尸 / 吸血鬼 / 精灵）。 / Side-line mechanism decided: generic `kind=side`; equilibrium rule; player-driven promotion with manual pick on tie; first batch in Main (zombie / vampire / elf).
* 2026-09-08 — 势力同盟与种子化平衡态定案：任意主 / 支势力（含跨世界观）可经 `allies` 缔结同盟并影响扩张与事件；无玩家的初始平衡态由世界种子确定性派生（同种子一致）。 / Faction alliances and seed-determined equilibrium decided: `allies` across lines/worldviews; no-player baseline derived deterministically from the world seed.
* 2026-09-08 — 玩家开局与自建定案：开局主世界观·无势力·空白起点；线索 / 机遇双通道发现；自建三角 = 自建势力（入宇宙学，可争主线）/ 自建聚落（场所基座）/ 自建世界观（贤者立卷，游戏内结晶新世界观）。 / Player entry and self-building decided: faction-free start in Main; clue/opportunity discovery; own faction / settlement / worldview (sage-chronicle crystallization).
* 2026-09-08 — Realm Line 总框架定案（**否决点数稀缺制**）：自由优先、无领域点硬上限；全能可达但极难（前快后慢成长曲线、成长不可洗点）；领域成长 × 世界观立场正交；顶点「贤者之路」——玩家可成贤（读碑 / 立卷 / 拟规则，非 NPC 专属）。 / Realm Line framework decided (point-cap rejected): freedom-first, no caps; mastering all possible but very hard; growth cumulative; orthogonal to alignment; apex = sage path (players may become sages).
* 2026-09-08 — 设计原则「无系统气味」定案（全局铁律）：玩家侧禁游戏化系统（HUD 面板 / 进度条 / 数值 / 日志 / 提示），一切以世界语言表达；文档术语仅作内部组织语，玩家侧一律转译为世界实物。 / "No-system" principle decided (global): no gamified systems player-facing; everything diegetic; in-doc terms are internal vocabulary only.
* 2026-09-08 — 隐型技术线定案（p.2.3–2.4）：零技术知识直觉开局；获得 = 遗迹遗物逆向 / 文明学习 / 实践领悟；学得后创新推进；技术为横向底座按领域限深度；无科技树 UI 与研发队列。 / Tech line decided: intuition-first zero-knowledge start; acquisition via ruins reverse-engineering, civilization learning, practice; innovation after learning; horizontal base gated by realms; no tech-tree UI.
* 2026-09-08 — 逆向拆解机制细化：五步闭环（检视→拆解→试作→复现→超越）、领悟四层（辨认→复刻→改良→超越）；拆坏信息缺损由同类遗物补全；知识永久保留；拆卸台方块 + 耗损工具；全流程进事件流。 / Reverse-engineering mechanic detailed: five-step loop, four comprehension tiers, same-kind artifact completion, permanent knowledge, disassembly bench.
* 2026-09-08 — 逆向拆解深挖：遗物四类（器械/器皿/图籍/标本，td dtype）、拆卸台三槽 + 力道三档（无百分比）、信息三维（构造→复刻 / 材料→改良 / 铭文→辨认超越·挂世界观钩）、试作与「会了」判定；失败仅伤部位；拆链阶梯 T0–T4（第一件逆向 = 拆卸工具）；遗物按遗迹 × 种子确定性生成。 / Reverse-engineering deepened: four artifact kinds, three actions + three force tiers, three info dimensions, prototype/mastery rules, part-only breakage, T0–T4 tool-chain ladder, seed-deterministic generation.
* 2026-09-08 — 领域清单第一批 12 定：地质 / 农垦 / 博物 / 冶金 / 工匠 / 草药 / 奥术 / 考古 / 天文 / 商道 / 战技 / 交通（td 可扩展）。 / First-batch realm catalog (12) decided; extendable via contract.
* 2026-09-08 — 研究新领域定案：第一批 12 非封闭清单；纯涌现自持名（实践凝成新领域，无贤者仪式）；可共享注册（写入通用「藏录」跨存档 / 多人引用）；玩家成领域作者。 / Realm invention decided: emergence + self-naming; shareable via the Ledger; players become realm authors.
* 2026-09-08 — 「贤者册」通用化定案：重命名为「藏录 / Ledger」，Subterra 实现（新领域 / 结晶世界观 / 镜像层 / 遗物条目通用登记，td + API 双接口）；Toterra 消费 sub，贤者册仅为其 diegetic 面貌；世界观契约语义仍在 Toterra。 / Sage-registry generalized as the Ledger, implemented in Subterra; Toterra consumes it; contract semantics stay in Toterra.
* 2026-09-08 — 挂点接线表一稿（p.2.1）落定：27 项内容挂点 × 12 领域三档门槛（含领域交叉 / 跨领域神话级两特殊档）；世界生成为世界侧执行不设玩家门；门槛档位为内部语，玩家侧无 UI。 / Gate-wiring first draft landed: 27 wires across the 12 realms; worldgen ungated; tiers are internal vocabulary only.