# Toterra Roadmap / Toterra 路线图

**Status / 状态:** Active / 生效中
**Date / 日期:** 2026-09-08
**Version discipline / 编号纪律:** Development uses the pre-release p-track only — `p.<release>.<module>.<sub-item>` (max three levels). The release track `r.x.y.z` is cut from a specific p version at stabilization time and introduces no new features. / 开发计划一律只用 p 轨 `p.<发布档>.<模块>.<子项>`（最多三级）；`r.x.y.z` 为正式发行轨，只做优化与稳定、不引新功能。

## Positioning / 定位

* Toterra 为系列主内容模组（万象之土 / Land of All Things）：万物拟真生存、每个领域深度扩展、生物与地形无穷变种、玩家只能精通少数领域。 / Toterra is the series main content mod: hyper-realistic all-domains survival, deep expansion of every domain, endless exploration variety, each player mastering few realms.
* 世界改造归 Toterra：消费 Subterra 框架（`subterra-api`）重组九维世界生成、矿石按维度分布、`RegionAnnouncement` 区域命名解锁等。 / World reshaping is Toterra's job: it consumes the Subterra framework (subterra-api) to recombine the nine-dimension worldgen, ore-by-dimension distribution, RegionAnnouncement region-naming unlocks, etc.
* 世界观分层：物理层（主世界地形 / 气候 / 成矿 / 生态 / 交通物理）按 B 档拟真重写；叙事与超自然层保留 MC 世界观，真实地球物理 × 奇异异界对比为设计意图。 / Worldview layering: the physical layer is rewritten full-realism (B tier); the narrative and supernatural layer keeps the MC lore — realistic earth physics against eerie otherworlds is the design intent.

## Plan / 规划

三线内容于 2026-09-08 定稿（世界线 / 交通体系线 / 生物线），全部为 p 轨条目；实施顺序与子项细化随开发推进确认，未收敛的设计点明示「待细化」，不虚构占位。 / The three content lines were finalized on 2026-09-08 (world / transport / fauna); all are p-track items; order and sub-items are refined as development proceeds; unconverged designs stay marked "to be refined" and nothing is invented.

### Worldview Retention / 世界观保留清单（2026-09-08 定）

* 四块保留沿用（用户拍板）；清单外内容随拟真重写或待定。 / Four pillars retained (user decision); unlisted content is rewritten or pending.

| Pillar / 块 | Retained / 保留内容 | Link to realism / 与拟真层衔接 |
| --- | --- | --- |
| Nether & End / 下界与末地 | 异界维度存在与身份 | 与拟真主世界对比；不参与主世界物理拟真 |
| Magic & Arcana / 魔法·奥术 | 附魔、炼药、末影珍珠的奥术语义 | 传送压制≠移除，传送为奥术领域进阶解锁（见交通线） |
| Villager civilization / 村民文明 | 村庄贸易、掠夺者灾厄 | 社会学保留，行为层可按拟真微调 |
| Ancient ruins / 上古遗迹 | 要塞、远古城市、堡垒的上古叙事 | 文明遗迹压在真实地层之上 |

### World Line / 世界线 — B 档 TFC 式彻底拟真

* 经拍板：世界默认档为 B（完全替换），仿 TerraFirmaCraft 真实地理。TFC 为 EUPL-1.2（强 copyleft），定为机制级 clean-room 参考——玩法设计不受版权保护，实现与资产全部自研。 / User decision: default world tier is B (full replacement), modeled on TerraFirmaCraft's realistic geography. TFC is EUPL-1.2 (strong copyleft) — mechanism-level clean-room reference only; implementations and assets are all self-made.

| p-track / p 轨 | Milestone / 里程碑 | Status / 状态 |
| --- | --- | --- |
| p.1.0 | Content-line skeleton / 内容线骨架：消费 Subterra worldgen API（SurfaceRules 装配点 / 预设备选）+ 结构护栏 + 矿物按维度分布前置注册 | designed / 已定 |
| p.1.1 | Litho strata / 岩性地层：litho 维度换 StrataAlgo（区域分层 + 岩石类型组态，td 定义），首个「维度独立换算法」验证 | planned / 已立项 |
| p.1.1 | Ore by parent rock / 矿石按母岩：mineral × {岩石类} 前置规则 + 矿脉走向，接结构护栏防重叠 | planned / 已立项 |
| p.1.1 | Climate-driven vegetation / 气候驱动植被：climate → vegetation 接缝（温度 / 降雨 / 蒸散 → 植被带） | planned / 已立项 |
| p.1.1 | World preset × realm link / 世界预设 × 专精联动：不同预设资源分布不同（供 p.1.9 专精系统消费） | planned / 已立项 |

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
| p.1.6 | Realm link / 专精联动：筑路 / 冰运 / 铁路三方向深度解锁（供 p.1.9 消费） | planned / 已立项 |

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

### Realm Line / 专精系统（灵魂玩法，待细化）

* 玩家只能精通少数领域；筑路 / 冰运 / 铁路 / 博物·驯养等领域的深度解锁联动世界、交通、生物三线；设计未定时不填充细节。 / Mastery of few realms; realm unlocks tie the three lines together; details pending.

## Discipline / 纪律

* 小任务逐个提交：每完成一个小任务即报告并提交一次，得确认后再做下一个。 / Small tasks are submitted one at a time; each is reported and committed before the next starts.
* 所有子任务完成后统一 review + 清理 + 推送。 / After all sub-tasks complete: one review, cleanup, and push.
* 验收确定性优先（服务端开服、客户端进世界、断言全 PASS）。 / Acceptance is determinism-first (server boots / client enters world / assertions PASS).

## Progress Log / 进度记录

* 2026-09-08 — 内容线初稿落盘：世界线（B 档 TFC 式彻底拟真）、交通体系线（十一面状态包 / 三语族 / 冰双模型 / 传送全面压制）、生物线（现实生物学三大支柱，性能优先）；TFC（EUPL-1.2）定为机制级 clean-room 参考。 / First content-line draft: world line (B, TFC-style full realism), transport line (eleven-facet state pack / three families / ice dual model / full teleport suppression), fauna line (real-biology pillars, performance-first); TFC (EUPL-1.2) adopted as mechanism-level clean-room reference.
* 2026-09-08 — 世界观保留定案：物理层拟真重写、叙事/超自然层保留（下界与末地 / 魔法奥术 / 村民文明 / 上古遗迹四块）；传送压制口径修正为「压制≠移除」。 / Worldview retention decided: physical layer rewritten, narrative/supernatural layer retained (Nether & End / magic / villagers / ancient ruins); teleport-suppression wording fixed to "suppress ≠ remove".