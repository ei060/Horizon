---
layout: default
title: "Horizon Summary: 2026-11-26 (ZH)"
date: 2026-11-26
lang: zh
---

> 从 168 条内容中筛选出 21 条重要资讯。

---

**科技新闻**
1. [1Password 确认安全事件，部分客户账户信息被窃](#item-tech-news-1) ⭐️ 8.0/10
2. [Anthropic 相关 GRH Lean 验证出现更短可读版本](#item-tech-news-2) ⭐️ 8.0/10
3. [FCC 有条件批准 SpaceX 部署百万颗轨道数据中心卫星](#item-tech-news-3) ⭐️ 8.0/10
4. [Ubuntu 安全补丁响应慢引发讨论，部分用户转向 Debian](#item-tech-news-4) ⭐️ 7.0/10
5. [Character.AI 私聊数据出售遭多州总检察长反对](#item-tech-news-5) ⭐️ 7.0/10
6. [Ladybird 发布首个可下载 Alpha，支持 macOS 与 Linux](#item-tech-news-6) ⭐️ 7.0/10
7. [Ars Live 讨论：数据中心遭军事与无人机打击恐难停止](#item-tech-news-7) ⭐️ 7.0/10
8. [伊朗 Shahid Kaveh 被指远程调高法国超市冷柜温度](#item-tech-news-8) ⭐️ 7.0/10
9. [Claude 等通用模型在蛋白质任务上挑战 AlphaFold](#item-tech-news-9) ⭐️ 7.0/10
10. [小鹏科技日：Robotaxi 年底无人示范运营，IRON 明年量产](#item-tech-news-10) ⭐️ 7.0/10
11. [腾讯开源 Hy4 flash 量化权重，64GB Mac mini 可跑最小版](#item-tech-news-11) ⭐️ 7.0/10
12. [Minecraft Java 版曝资源包字体 RCE 漏洞](#item-tech-news-12) ⭐️ 7.0/10
13. [三星与 SK 海力士据报采用长江存储 Xtacking 技术](#item-tech-news-13) ⭐️ 7.0/10

**科技博客**
1. [2026 QQ8：地球的临时迷你月亮](#item-tech-blog-1) ⭐️ 5.0/10
2. [五款开源输入法稳定性对比](#item-tech-blog-2) ⭐️ 5.0/10
3. [Ladybird Alpha：独立内核开源浏览器](#item-tech-blog-3) ⭐️ 4.0/10

**财经新闻**
1. [报道称美商务部施压英特尔交出 10%股份](#item-finance-news-1) ⭐️ 9.0/10
2. [美国提议对 14 个贸易伙伴加征第 301 条新关税](#item-finance-news-2) ⭐️ 8.0/10
3. [英国能源账单明年 1 月起上涨 26%](#item-finance-news-3) ⭐️ 7.0/10
4. [Shein 同意支付 1 亿美元和解美国消费者误导指控](#item-finance-news-4) ⭐️ 7.0/10
5. [韩国央行加息 0.25 厘至 3.25 厘 上调今明两年增长预测](#item-finance-news-5) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [1Password 确认安全事件，部分客户账户信息被窃](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password 确认发生安全事件：攻击者入侵一名员工的企业 GitHub 账户，借此访问源代码并向后台服务推送恶意代码，导致部分客户账户信息被下载，包括姓名、邮箱地址、账户标识以及账户创建和最近登录时间。公司称客户保险库及其内容未受影响，但未披露受影响用户数量；调查于 11 月 19 日开始，公司已停用涉事账户、轮换或撤销可能暴露的内部凭证，并加强邀请与恢复邮件验证码。1Password 表示用户无需更改账户，但应警惕钓鱼。

hackernews · lxhrstn · 11月25日 17:18 · [社区讨论](https://news.ycombinator.com/item?id=50644817)

**「背景」** 1Password 是广泛使用的密码管理器，客户凭据存放在加密保险库中，因此其后台服务的代码部署权限本身就是高价值攻击目标。按披露的时间线，公司于 11 月 19 日开始调查员工企业 GitHub 账户被入侵的迹象，攻击者正是借该账户接触源代码并向后台服务推送了恶意代码，随后造成信息被下载。

**「后续钓鱼风险」** 对受影响客户而言，泄露的姓名、邮箱、账户标识和登录时间可能被用于定制化钓鱼；已有用户报告收到包含部分个人细节、冒充共享保险库链接的邮件，因此应核对发件域名并避免点击可疑链接。1Password 表示用户无需更改账户或保险库，但已加强邀请和恢复邮件的验证码，收到此类邮件时需额外确认。

**「社区讨论」** Hacker News 讨论中，tptacek 认为员工笔记本电脑被攻陷、攻击者随后向 GitHub 推送代码并最终部署，是 SaaS 公司长期面临的标准入侵路径；ctidd 则质疑公告未说明是否缺少分支保护规则，以及恶意代码为何能被推送到后台服务。另有用户 qixxiq 报告收到包含部分个人细节、声称“共享 210 个项目”的高质量钓鱼邮件，ChrisHardie 则对在线保险库在代码被恶意推送后的安全性表示担忧。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1Password’s backend ...</a></li>
<li><a href="https://9to5mac.com/2026/11/25/1password-confirms-security-incident-heres-what-you-need-to-know/">1Password confirms security incident, here’s what you need to ...</a></li>

</ul>
</details>

**标签**: `#security incident`, `#1Password`, `#supply chain security`, `#phishing`, `#SaaS security`

---

<a id="item-tech-news-2"></a>
### [Anthropic 相关 GRH Lean 验证出现更短可读版本](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

GitHub 上发布了 lsernau/grh-lean，这是一个面向 GRH 相关工作的更短、更易读的 Lean 形式化版本，被描述为与 Anthropic 的 GRH Lean 验证相关。评论称代码量从约 1700 万行降到约 7.6 万行，并加入了对“known math”和“new math”的区分及大量人类可读文档；但另有评论提到约 30 万行的版本，且来源未提供仓库内容，这些数字和具体范围尚不能视为已核实。现有材料没有表明这构成新的数学突破，重点在形式化代码的规模与可读性。

hackernews · nb-t · 11月25日 21:48 · [社区讨论](https://news.ycombinator.com/item?id=50648050)

**「背景」** 2026 年 11 月 20 日，Levent Alpöge 宣布他与 Anthropic 的 Claude 合作得到黎曼猜想及 Dirichlet L 函数广义黎曼猜想的证明，并以 Lean 形式化代码发布，共 175,187 个文件、约 1700 万行。次日，Lean FRO 与 Mathlib 计划宣布已核验该证明。此次的 lsernau/grh-lean 是同一结果经压缩、面向阅读的 Lean 4 版本，构建于 Mathlib 之上，只使用 propext、Classical.choice 与 Quot.sound 三条公理。

**「影响」** 对需要审阅、教学或复用该形式化的 Lean 用户来说，更短的代码和更清晰的文档可直接降低阅读与核查成本；在行数和版本差异未澄清前，使用者应先核对仓库的实际提交、构建说明和对应定理范围，而不能仅凭评论中的 7.6 万行判断其完整性。

**「社区讨论」** 评论者称赞可读版本把“known math”与“new math”分开并配有文档，认为这有助于消化形式化内容；也有人追问这是否构成对陶哲轩一个月前关于巨型证明缺乏洞见这一观点的挑战，以及 LLM 能否通过“golf”证明并解释它们。还有评论者希望有数学家真正理解核心论证，写出正式数学论文并在会议上讲解，而不只停留在 Lean 代码。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge&#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.math.uwaterloo.ca/~mrubinst/alpoge_claude_grh/">Alpöge/Claude proof of the Generalized Riemann Hypothesis</a></li>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau/grh-lean: A short Lean 4 proof of the ...</a></li>

</ul>
</details>

**标签**: `#Lean`, `#formal verification`, `#AI-assisted mathematics`, `#Generalized Riemann Hypothesis`

---

<a id="item-tech-news-3"></a>
### [FCC 有条件批准 SpaceX 部署百万颗轨道数据中心卫星](https://arstechnica.com/space/2026/11/the-fcc-has-authorized-spacex-to-deploy-1-million-satellites/) ⭐️ 8.0/10

美国联邦通信委员会（FCC）于周三有条件批准 SpaceX 部署最多 100 万颗「Starmind」卫星，用作轨道数据中心。若全部部署，在轨卫星数量将增加约 50 倍。FCC 主席 Brendan Carr 称此举「为支撑美国领导力与增长所需的计算基础设施开辟了大胆的新前沿」。该决定属于有条件授权而非实际部署；FCC 同时驳回了反对者提出的部分关键担忧（包括对科学研究的潜在威胁），理由是这些事项不在其监管权限之内。

rss · Ars Technica · 11月25日 18:22

**「背景」** 轨道数据中心指的是把计算和数据处理载荷搭载在卫星上，在轨处理数据，而不是完全依赖地面机房；SpaceX 在申请中称，这类卫星可借助近乎持续的太阳能实现显著的成本与能效优势，并减少对地球环境的影响。该提案在获批前遭到 Amazon、Viasat 和美国天文学会反对。

**「部署时间表」** FCC 的授权附有明确部署节点：SpaceX 须在 2033 年 11 月 25 日前部署首批 Starmind 卫星。对打算采用轨道数据中心容量的开发者和组织来说，近期容量规划仍应基于地面设施，并将 Starmind 视为受监管时间表约束、尚未形成可用服务的长期选项。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/25/spacex-fcc-satellite-approval.html">SpaceX wins FCC approval for 1 million orbital data center satellites</a></li>
<li><a href="https://nypost.com/2026/11/25/business/fcc-approves-elon-musks-spacex-to-launch-1-million-satellites-for-data-centers-in-space/">FCC approves Elon Musk&#x27;s SpaceX to launch 1 million satellites for...</a></li>
<li><a href="https://spaceflightnow.com/2026/11/26/fcc-green-lights-spacexs-plan-to-launch-1-million-starmind-data-center-satellites/">FCC green lights SpaceX’s plan to launch 1 million ‘Starmind ...</a></li>

</ul>
</details>

**标签**: `#FCC`, `#SpaceX`, `#orbital data centers`, `#satellite constellations`, `#computing infrastructure`

---

<a id="item-tech-news-4"></a>
### [Ubuntu 安全补丁响应慢引发讨论，部分用户转向 Debian](https://www.openwall.com/lists/oss-security/2026/11/25/9) ⭐️ 7.0/10

2026 年 11 月 25 日，Hacker News 上围绕 oss-security 邮件列表一篇题为“Slow Ubuntu security response times”的帖子展开讨论，焦点是 Ubuntu 发布安全修复的速度。多名评论者表示已在生产环境中采取行动：一位用户称其所在公司将全部服务器镜像从 Ubuntu 换成 Debian，另一位称一周前首次因为这个原因，把“通用 Linux 虚拟机”的默认选择改为 Debian。讨论同时出现相反论据，认为各发行版都要在补丁速度与回归测试之间取舍。由于原始 oss-security 帖文内容未提供，具体涉及哪些漏洞、延迟多久、影响哪些 Ubuntu 版本均无法核实。

hackernews · gslin · 11月25日 20:38 · [社区讨论](https://news.ycombinator.com/item?id=50647181)

**「背景」** 这封邮件由 Hanno Böck 于 2026 年 11 月 25 日发到 oss-security 邮件列表，帖子主题就是 Ubuntu 对严重安全漏洞的响应偏慢；oss-security 是公开讨论发行版安全处理进度的邮件列表。Ubuntu 把安全更新放在单独的 security 仓库，一些管理员会配置 unattended-upgrades 只安装该仓库的补丁，而讨论中有用户指出修复有时先出现在 -updates、数小时后才进入 security 仓库，这使响应延迟直接影响自动打补丁的服务器。

**「对运维的影响」** 对仅启用 security 源做无人值守升级的管理员，评论者 alanfranz 报告了一个具体的操作隐患：近期的安全修复往往先出现在 -updates 源，数小时后才进入 security 源，因此沿用“只装安全更新”的旧配置可能在关键补丁上滞后。他本人的应对是改为安装全部更新，并接受因此破坏系统的风险；这是个人经验之谈，未经独立验证。

**「社区观点」** 争论集中在“快”与“稳”的取舍：有评论引用稳定内核维护者 2025 年的说法，认为必须跟进全部 stable/LTS 更新，手工挑选补丁无法覆盖已知和未知问题，反而可能更不安全；反对过快发布的一方则强调 Debian 等发行版 QA 资源有限，回归问题确实会发生，并举例 Debian bug 1154101。还有评论者对 Ubuntu 出现这种延迟表示不解，认为这与其“开箱即用、有社区支持”的定位不符。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.openwall.com/lists/oss-security/2026/11/25/9">oss-security - Slow Ubuntu security response times - openwall.com</a></li>
<li><a href="https://seclists.org/oss-sec/2026/q4/890">oss-sec: Slow Ubuntu security response times</a></li>

</ul>
</details>

**标签**: `#Ubuntu`, `#Linux security`, `#vulnerability response`, `#open source`, `#distribution maintenance`

---

<a id="item-tech-news-5"></a>
### [Character.AI 私聊数据出售遭多州总检察长反对](https://techcrunch.com/2026/11/25/state-ags-fight-character-ais-plan-to-auction-off-users-private-chats/) ⭐️ 7.0/10

美国多州总检察长正挑战 Character.AI 的拟议破产出售，争议在于交易包含超过 2100 万个美国账户的敏感个人数据，其中 210 万个账户的注册者为未成年人。总检察长们把这一数据范围列为反对理由，但目前没有公开具体的法律行动或裁决结果。该出售仍属拟议阶段，聊天数据最终如何处理、交易能否按现有方案推进，现有信息尚未说明。

rss · TechCrunch · 11月25日 17:35

**「背景」** 破产程序中的资产出售可以把公司持有的数据库和用户记录随业务一并转让给买方，法院在批准前会审查相关方提出的异议。州总检察长可以代表本州居民就此类交易提出异议，尤其是涉及消费者数据和未成年人时。对 Character.AI 而言，这意味着交易标的不仅是模型或品牌，还包括大量私人聊天数据的控制权。

**「影响」** 若交易按现有方案推进，受影响用户的私密聊天记录控制权可能随资产转移给买方，其中包括 210 万个未成年人账户；总检察长介入使数据处置成为交易能否推进的关键问题。

**标签**: `#AI privacy`, `#data governance`, `#Character.AI`, `#bankruptcy sale`, `#consumer protection`

---

<a id="item-tech-news-6"></a>
### [Ladybird 发布首个可下载 Alpha，支持 macOS 与 Linux](https://arstechnica.com/gadgets/2026/11/ladybirds-new-alpha-shows-theres-life-beyond-chromium/) ⭐️ 7.0/10

Ladybird 项目于 11 月 23 日发布首个可下载的 alpha 版本，提供 macOS 和 Linux 预编译包。此前用户必须自行从源码编译，现在则可安装并自动更新。该项目用四年时间从零编写渲染引擎和 LibJS JavaScript 引擎，而不是基于 Blink 或 Gecko 分叉；项目负责人 Andreas Kling 称浏览器外围“朴素但可用”。这仍是早期 alpha，功能完整度有限。

rss · Ars Technica · 11月25日 17:33

**「背景」** 浏览器引擎负责把 HTML、CSS 和 JavaScript 渲染为页面，而目前主流浏览器几乎都集中在少数几个引擎上：Chrome、Edge、Brave、Opera 使用 Google 的 Blink，Firefox 依赖 Gecko。Ladybird 经过约四年的开发，自行编写渲染引擎与 LibJS JavaScript 引擎，此前外界只能从源码自行编译，这次才首次提供可直接安装、可自动更新的预编译版本。

**「影响」** 希望评估非 Blink、非 Gecko 浏览器引擎的开发者现在可以直接安装试用并提交反馈；但作为早期 alpha，它更适合测试和实验，而不是作为日常主力浏览器。自动更新机制也降低了跟进新构建版本的成本。

**标签**: `#browser engines`, `#open source`, `#Ladybird`, `#software releases`, `#web platforms`

---

<a id="item-tech-news-7"></a>
### [Ars Live 讨论：数据中心遭军事与无人机打击恐难停止](https://arstechnica.com/gadgets/2026/11/ars-live-recap-dont-expect-military-attacks-on-data-centers-to-stop/) ⭐️ 7.0/10

在 2026 年的中东冲突中，亚马逊的数据中心首次遭到军事攻击，俄罗斯与乌克兰也互以无人机大规模袭击对方的数据中心；Ars Technica 就此举办直播讨论并发布回顾。英国皇家联合军种研究所（RUSI）的 Joseph Jarnecki 在会上指出，公共云已被军方用于运行战场管理系统、人事和资源管理等计算任务，这种军民两用使得民用数据中心在作战目标选择原则下可能被视为军事目标，从而招致攻击。他还强调，廉价的“自杀式”无人机能以极低成本给数据中心造成不成比例的经济损失，并引发大范围云服务中断。Ars Technica 此前报道称，伊朗对亚马逊数据中心的打击曾造成客户数据永久丢失。

rss · Ars Technica · 11月25日 16:47

**「背景」** 这轮讨论的核心前提是数据中心“军民两用”：公共云和私有数据中心既承载民用业务，也被军方用于战场管理、人事和资源管理等计算任务，因此可能被对手视为军事目标。RUSI 的分析指出，当数据中心同时托管民用与军用负载时，打击它可以产生战略效果；Ars 的直播讨论则进一步追问，面对无人机和导弹，加固数据中心、提升战时云韧性是否现实。

**「对云用户的影响」** 对依赖单一区域云资源的用户来说，物理攻击的后果不止于服务暂时中断：Ars 此前报道的客户数据永久丢失表明，灾备与跨区域冗余方案需要把“数据中心本身成为打击目标”纳入假设，而不能只考虑设备故障或网络攻击。Jarnecki 强调的成本不对称也意味着，运营商难以用传统防空手段在经济上覆盖廉价无人机带来的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.rusi.org/explore-our-research/publications/commentary/iranian-data-strikes-shake-global-digital-infrastructure">Iranian Data Strikes Shake Global Digital Infrastructure | Royal United ...</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/11/ars-live-can-the-cloud-survive-drone-strikes-on-data-centers/">Ars Live: What drone attacks on data centers mean for... - Ars Technica</a></li>

</ul>
</details>

**标签**: `#data center security`, `#cloud infrastructure`, `#drone attacks`, `#critical infrastructure`, `#military conflict`

---

<a id="item-tech-news-8"></a>
### [伊朗 Shahid Kaveh 被指远程调高法国超市冷柜温度](https://arstechnica.com/security/2026/11/a-familiar-iranian-hacking-group-has-found-a-new-way-to-cause-chaos/) ⭐️ 7.0/10

今年 10 月的一个夜晚，黑客远程调高法国数百家超市制冷系统的温度，造成数百万欧元的食品损失。法国情报机构在数字痕迹中发现波斯语线索，将事件指向伊朗伊斯兰革命卫队下属的精锐黑客单位 Shahid Kaveh；这一归因目前仍是“被指”，并非公开司法结论。该单位以在 1980 年代两伊战争中死亡的伊朗指挥官 Mahmoud Kaveh 命名，隶属革命卫队网络电子指挥部。

rss · Ars Technica · 11月25日 14:29

**「背景」** Shahid Kaveh 是伊朗伊斯兰革命卫队网络电子司令部（IRGC-CEC）下属的网络攻击单位之一，本次超市制冷系统事件并非它首次针对运营技术下手：据《金融时报》报道，该单位 2024 年还曾对美国工业控制设备发动过一波攻击。法国已于 11 月 9 日正式点名该单位为 10 月这起约 700 家超市受影响事件的幕后黑手。

**「影响」** 对使用联网温控系统的零售商来说，这起事件表明远程温度调节接口可被直接用来制造库存损失；运营方需要限制此类接口的访问权限，并对异常温度设定变更设置告警。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ft.com/content/5f3a85ad-e621-4189-bada-989f41702ed9?syn-25a6b1a6=1">The secretive Iranian cyber unit behind Europe’s freezer hacks</a></li>
<li><a href="https://www.fdd.org/analysis/france-is-latest-victim-of-iranian-cyber-sabotage-first-unleashed-on-israel/">France Is Latest Victim of Iranian Cyber Sabotage First Unleashed on...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#critical infrastructure`, `#IoT security`, `#state-sponsored hacking`, `#Iran`

---

<a id="item-tech-news-9"></a>
### [Claude 等通用模型在蛋白质任务上挑战 AlphaFold](https://www.solidot.org/story?sid=85992) ⭐️ 7.0/10

Phylo 研究员 Xinming Tu 本月初用 OpenAI、Anthropic 和 Google 的大模型测试它们预测鲜为人知细菌蛋白质序列的能力，称 Anthropic 最新版 Claude 不仅优于其他大模型，也超过针对蛋白质序列训练的专用工具；他与哈佛医学院的 Leo Chen 分享这一结果后，计算生物学界展开讨论。OpenAI 本周二宣布，其最新大模型设计出新蛋白质，实验室合成和测试时部分蛋白质的行为符合预期，这仍是厂商说法。部分科学家据此推测，Claude、ChatGPT 这类通用模型可能在蛋白质结构预测和设计上超越 AlphaFold 等专用工具；也有研究人员质疑，大模型展现的部分能力可能只是机械重复训练数据。上述结果目前仍属初步，缺少同行评议和独立复现。

rss · Solidot · 11月25日 15:26

**「背景」** AlphaFold 由 Google DeepMind 开发，其蛋白质结构数据库收录了超过 2 亿个预测结构；AlphaFold 3 还可通过服务器预测蛋白质与 DNA、RNA 等分子的相互作用。这类专用模型此前一直依靠针对蛋白质序列与结构数据训练，被当作蛋白质结构预测的参照工具。因此，让通用对话大模型直接完成同类任务，本身就是对既有分工的一次越界测试。

**「对蛋白设计团队的实际影响」** 按照 OpenAI 公布的数据，GPT-6.2 设计了 322 个蛋白 minibinder，实验室测试中只有 35 个出现结合，命中率约 11%，且整个流程仍要借助通用推理、代码工具以及专业结构工具配合完成。这意味着对生物技术团队而言，LLM 目前更像是候选生成器，湿实验筛选的规模和通量仍是瓶颈；在把通用模型用于实际项目前，还需要在未公开的靶点上，与 AlphaFold 这类专用工具做对照基准测试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://alphafold.ebi.ac.uk/">AlphaFold Protein Structure Database</a></li>
<li><a href="https://alphafoldserver.com/welcome">AlphaFold Server</a></li>
<li><a href="https://deepmind.google/science/alphafold/">AlphaFold — Google DeepMind</a></li>
<li><a href="https://www.unite.ai/openai-reports-gpt-6-designs-proteins-with-reasoning-and-code/">OpenAI Reports GPT-6 Designs Proteins With Reasoning and ...</a></li>
<li><a href="https://www.techrepublic.com/article/news-gpt-6-2-protein-design-lab-binding-results/">GPT-6.2 Protein Design: What the Lab Binding Data Show</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#protein structure prediction`, `#protein design`, `#large language models`, `#AlphaFold`

---

<a id="item-tech-news-10"></a>
### [小鹏科技日：Robotaxi 年底无人示范运营，IRON 明年量产](https://www.ifanr.com/1695212?utm_source=rss&amp;utm_medium=rss&amp;utm_campaign) ⭐️ 7.0/10

在 2026 年小鹏科技日上，小鹏称 IRON 人形机器人全程无人工遥控、独自完成中英文脱稿演讲；其 Robotaxi 已开启主驾无人载客体验，计划 2026 年年底在部分区域开启主驾无人示范运营，首款定制车型 YOYO-01 计划 2027 年发布。小鹏称第二代 VLA 自 2026 年 7 月起在德国、荷兰、法国完成本地泛化测试，11 月在巴黎门店向公众开放城区高阶智驾试乘，成为首家在欧洲开放该体验的中国车企，并目标 2027 年上半年开启全球首批交付。小鹏计划从 2027 年第二季度起对全球新购车用户开启图灵 AI 智驾订阅，服务开启前下订用户权益终身不变；双 Orin-X 车型将从 2026 年 12 月起分批收到第二代 VLA 蒸馏版推送。IRON 计划 2027 年 1 月进入硬件量产、第一季度在小鹏门店以导购身份实习、第二季度正式发布；小鹏还计划通过 OTA 将 5C 超充升至 6C，使 10%—80% 充电缩短至 10.7 分钟。

rss · iFanr · 11月26日 02:25

**「背景」** 小鹏把第二代 VLA 当作同一套智驾底座：今年 7 月起，搭载该方案的 NGP 已在德国、荷兰和法国完成本地泛化测试，之后才延伸到 L4 Robotaxi。另一个直接前情是去年科技日，IRON 因猫步过于拟人而遭遇“里面藏真人”的质疑，小鹏最终剪开机器人皮肤自证；今年 IRON 改为无遥控登台，不再需要靠剪开皮肤来证明。

**「车主权益与推送节奏」** 对小鹏现有车主和后续购车者而言，第二代 VLA 的落地按硬件平台分层：双 Orin-X 车型从 2026 年 12 月起分批收到蒸馏版，剩余双 Orin-X 车型要到 2027 年第一季度；图灵 AI 共驾则从 2026 年 12 月随 G9L、MONA L05 首批 OTA 推送。更直接的成本变化是，小鹏计划自 2027 年第二季度起向全球新购车用户开启图灵 AI 智驾订阅服务，只有服务开启前下订的用户保留终身智驾权益，后续购车者需把订阅支出计入用车成本。

**标签**: `#autonomous driving`, `#humanoid robots`, `#robotaxi`, `#VLA`, `#XPeng`

---

<a id="item-tech-news-11"></a>
### [腾讯开源 Hy4 flash 量化权重，64GB Mac mini 可跑最小版](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

腾讯混元通过 AngelSlim 开源了 224B 参数模型 Hy4 flash 的 GGUF 量化权重，面向希望在本地运行大模型的开发者。原始权重约 410.27GiB，最小的 IQ2-AH 版本为 125.73GiB，约为原版的 30%；文章称借助 Strata offload 框架，64 GB Mac mini 也能运行该版本。文章还给出以下数据：在 48 GB 显存设备上，10K 上下文下每秒生成 89 个 token；在 M5 Max 128 GB 上，Q3\_K 版本在 32K 上下文下每秒生成 47 个 token。在 DeepSWE v1.1 等评测中，Q3\_K 与原模型的得分差距不超过 0.4 分；这些性能与质量数据来自二手摘要，仍需独立验证。

telegram · zaihuapd · 11月25日 09:29

**「背景」** 关键前提是量化后的权重仍大于机器内存：最小的 IQ2-AH 版本为 125.73GiB，单靠 64 GB 内存放不下。Strata 是开源本地推理引擎，其做法是把同一份检查点拆分到 GPU 显存、主机内存和只读 NVMe 上，让超出内存容量的模型仍能加载运行。

**「实际影响」** 对想在本地运行 224B 模型的用户来说，可行的做法是根据可用内存选择量化档位：64 GB Mac mini 只能依靠 Strata offload 运行体积最小的 IQ2-AH（125.73GiB，约为原版权重的 30%），而已公布的 32K 上下文下每秒 47 token 的成绩来自 M5 Max 128 GB 上的 Q3\_K，不能直接套用到前者；来源中“与原模型差距不超过 0.4 分”的 DeepSWE v1.1 结论同样只针对 Q3\_K，IQ2-AH 的质量损失并未披露。此外，除 AngelSlim 版本外，Hugging Face 上已有第三方发布的 Hy4-flash GGUF 量化，并用 KL 散度与原模型对比，选型时需自行核对各版本的体积与精度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stratallm.org/">Strata LLM – Run 125B+ MoE Models on 12GB VRAM Consumer GPUs ...</a></li>
<li><a href="https://github.com/ro99/strata">GitHub - ro99/strata: C/C++ MoE inference engine for models ...</a></li>
<li><a href="https://huggingface.co/nace-ai/Hy4-flash-GGUF">nace-ai/Hy4-flash-GGUF · Hugging Face</a></li>
<li><a href="https://www.mindstudio.ai/blog/tencent-hy4-flash-local">Running Tencent&#x27;s Hy4-Flash Locally: Hardware, Quantization ...</a></li>

</ul>
</details>

**标签**: `#open-source AI`, `#model quantization`, `#local inference`, `#Tencent Hunyuan`, `#GGUF`

---

<a id="item-tech-news-12"></a>
### [Minecraft Java 版曝资源包字体 RCE 漏洞](https://github.com/bikini/minecraft2shell) ⭐️ 7.0/10

11 月 22 日公开的 minecraft2shell 披露，Minecraft Java 版服务器资源包中的特制 TrueType 字体可触发 FreeType 2.14.3 及更早版本的原生越界写，并在 Java 版 26.3 Windows 客户端执行任意代码；1.20.5 至 1.21.10 及 26.1 至 26.4 快照受影响，1.20.4 及更早版本和基岩版不受影响。Mojang 仍在使用 lwjgl-freetype 3.4.3，暂无官方补丁，也未见 CVE 确认。社区于 11 月 24 日发布 m2sfix 1.0.0，可通过 Java agent 或 mod 关闭 hinting 临时缓解；在修复前不要添加资源包，或将多人游戏服务器的资源包权限设为“禁用”。

telegram · zaihuapd · 11月25日 12:46

**「背景」** FreeType 是开源字体渲染库，Minecraft Java 版客户端通过 LWJGL 的 lwjgl-freetype 绑定调用它来解析和渲染字体，资源包中携带的 TrueType 字体也走同一条路径。因此这次的越界写发生在原生代码里，而非 Java 逻辑层：只要客户端加载并解析恶意字体文件就会触发，与玩家是否进入某个具体世界无关。

**「影响与应对」** 对使用 Java 版 1.20.5 至 1.21.10（含 26.1–26.4 快照）的 Windows 客户端玩家而言，只要连接一个下发含特制 TrueType 字体的资源包并发送普通动作栏文本的服务器，就可能触发 FreeType 2.14.3 的越界写而执行任意代码——公开 PoC 是针对 Mojang 签名、捆绑 FreeType 2.14.3 x64 的 Java 26.3 Windows 客户端构建验证的。在 Mojang 发布补丁前，投稿人建议不要添加任何资源包，把多人服务器的资源包权限设为“禁用”，或安装社区 m2sfix 1.0.0（以 Java agent 或 mod 关闭 hinting）作为临时缓解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/bikini/minecraft2shell">GitHub - bikini/ minecraft 2 shell : Minecraft to native RCE · GitHub</a></li>

</ul>
</details>

**标签**: `#Minecraft`, `#RCE`, `#security vulnerability`, `#FreeType`, `#open source`

---

<a id="item-tech-news-13"></a>
### [三星与 SK 海力士据报采用长江存储 Xtacking 技术](https://tech.ifeng.com/c/8yLRPKxQy4L) ⭐️ 7.0/10

据凤凰网报道，三星电子和 SK 海力士已通过交叉许可协议，同意在 3D NAND 闪存中采用长江存储 Xtacking 堆叠技术的部分内容；三星、SK 海力士和长江存储均拒绝置评，协议尚未获得确认。Xtacking 将存储单元与控制电路（CMOS）分别制作在两片晶圆上，再通过键合工艺合为一体，使两部分能够独立生产和优化。Omdia 高级分析师表示，这种安排可让厂商自行生产存储阵列，并把逻辑电路交给晶圆代工厂，从而采用更先进的制程。

telegram · zaihuapd · 11月25日 14:33

**「技术背景」** Xtacking 是长江存储提出的 3D NAND 键合路线：把存储阵列和 CMOS 逻辑电路分别制作在两片晶圆上，再键合到一起，使两部分可以独立选择制程。该技术早在 2018 年就由长江存储展示，并已在实际生产中得到验证；随着 NAND 堆叠层数升至数百层，传统单晶圆方案的限制更加突出。

**「影响」** 若协议落地，三星和 SK 海力士可在 3D NAND 制造中把存储阵列与 CMOS 逻辑电路分开生产、再行键合，并可能将逻辑部分交由晶圆代工厂的先进制程完成；但这目前仍只是据报道的安排，三家公司未予证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/samsung-and-sk-hynix-tap-ymtcs-xtacking-tech-in-cross-license">Samsung and SK Hynix cross-license YMTC&#x27;s Xtacking 3D NAND</a></li>
<li><a href="https://www.techpowerup.com/355199/samsung-and-sk-hynix-to-license-ymtcs-xtacking-technology">Samsung and SK hynix to License YMTC&#x27;s Xtacking ...</a></li>

</ul>
</details>

**标签**: `#3D NAND`, `#Xtacking`, `#semiconductor manufacturing`, `#Samsung/SK Hynix`, `#cross-licensing`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [2026 QQ8：地球的临时迷你月亮](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196974) ⭐️ 5.0/10

rss · Dapenti Xilei · 11月25日 23:52

**「背景」** 文章以 2026 QQ8 为例，介绍近地小行星如何被地球引力短暂捕获成“迷你月亮”，以及这类天体为何难以发现和确认。

**「方案」** 据作者转述，2026 QQ8 今年 4 月被地球引力捕获，直径约 2 米，即便进入大气层也只可能形成明亮流星，对地面没有实质威胁，预计 12 月初脱离。小行星中心主任佩恩称，迷你月亮并不罕见，平均任意时刻可能有一个，停留数周到数月；此前 2006 RH120 曾停留约一年，2020 CD3 约三年。它们小、远、视角移动快，现有巡天很难发现。2026 QQ8 由匈牙利 Konkoly 天文台的 Sárneczky 在 8 月例行搜寻中发现；因信号微弱，学界曾争论它是天然小行星还是人造太空垃圾，后通过追踪太阳辐射压对轨道的微小影响，并结合罗威尔发现望远镜和毛纳基山 2.2 米望远镜的数据，于 10 月下旬确认为天然天体。佩恩解释，近地天体若以不太大的速度接近，会随地球移动并逐渐受地球和月球引力扰动，开始绕地球打圈；其精确起源仍是进行中的课题。作者还称，目前已知近地天体约 4 万个，等维拉·鲁宾天文台 LSST 全面运行，佩恩预期已知天体将从约 150 万增至 500 万。

**「启示」** 文章的核心结论是：迷你月亮是地球附近持续发生的自然现象，2026 QQ8 的意义不在威胁，而在于展示引力捕获机制并预示巡天革命将带来更多发现。

**标签**: `#迷你月亮`, `#近地小行星`, `#轨道捕获`, `#天文观测`, `#薇拉·鲁宾天文台`

---

<a id="item-tech-blog-2"></a>
### [五款开源输入法稳定性对比](https://www.appinn.com/open-source-ime-boom-and-stability/) ⭐️ 5.0/10

rss · Appinn · 11月25日 09:40

**「背景」** 近期多款开源中文输入法集中出现，作者下载体验了其中五款，并以小狼毫（Weasel）的万象 base 方案（小鹤双拼）为统一参照，记录设置、稳定性、双拼与词库兼容性等第一手问题。作者的主观判断是，这些新项目热度虽高，成熟度却普遍不足以投入生产环境或支撑大规模宣发。

**「方案」** 作者的评分来自近两周高强度使用的主观清单，而非可复现的系统测试。小狼毫 v0.17.4.98 获 9 分，被视为当前最成熟的开源输入法：功能完整、成熟方案多、词库导入导出方便，几乎不崩溃（Firefox 崩溃也在 issue 区找到解法），主要缺点是配置过于复杂。青简 v0.3.3 得 7.5 分，主体可用且无明显崩溃、UI 或内存问题，但设置繁杂冲突，缺少部首查字，候选调权、双拼问字、全角符号和 Rime 多音词库导入等细节不完整。清风 v0.132.0 得 8 分，功能最多且都有 GUI，未发现明显恶性 bug，输入体验相对最佳，但设置项极多、搜索连自身提示都找不到，辅助码触发键保存失效、关闭学习仍自动调频，词库导入也有问题。水杉 v0.14.1 得 7 分，模型纠错选项最全但设置混乱，字体设置会崩溃，低配电脑上频繁丢字、丢输入和焦点，快捷键不可改，且不支持无读音词。FreeType v0.1.4 因宣传与实际不符仅得 4.5 分（抛开宣传为 6.5），存在设置不同步、候选拆词、按钮过小、反查缺失、混合词库导入出错等问题，但设置页的分区、精简和搜索被作者特别表扬。

**「启示」** 作者认为，这批开源输入法在功能数量上已经“爆发”，但稳定性、设置组织和双拼/词库等基础细节仍未过关；在它们补齐这些短板前，小狼毫仍是更可靠的选择，新项目不宜用过度宣传掩盖打磨不足。

**标签**: `#开源输入法`, `#Rime`, `#双拼`, `#稳定性评测`, `#Windows 输入法`

---

<a id="item-tech-blog-3"></a>
### [Ladybird Alpha：独立内核开源浏览器](https://www.appinn.com/ladybird-browser/) ⭐️ 4.0/10

rss · Appinn · 11月25日 06:26

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/ladybird-browser/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;现有浏览器大多共用 Chromium、WebKit 或 Gecko 内核，而 Ladybird 试图提供完全独立的选择：它源自 SerenityOS，2022 年成为独立跨平台项目，2024 年成立非营利组织，从零开发渲染、JavaScript 和 WebAssembly 引擎。

**「方案」** 2026 年 11 月 23 日，历经四年开发的 Ladybird 发布 Alpha，可直接在 macOS 和 Linux 安装，Windows 尚未支持。其目标包括完全独立内核、免费开源、尊重隐私、不接受默认搜索引擎交易、不靠用户数据变现；今年 2 月还宣布借助 AI 逐步将代码从 C++ 迁往 Rust。作者列出的已实现功能有书签、历史、隐私浏览、广告与内容拦截、多用户配置、会话恢复、PDF 和视频播放，Alpha 采用滚动更新，路线图是 2026 Alpha、2027 Beta、2028 正式版。作者上手称常见网页基本正常，但少见网站会出现 SSL 验证失败，开发者自己也承认部分网站打不开、偶尔崩溃、暂不保证安全并邀请安全研究。另一个明显取舍是它没有任何 AI 功能，暂不支持扩展和用户脚本，DevTools 通过本地端口调用 Firefox，作者还觉得内存占用似乎高于 Edge。

**「启示」** Ladybird Alpha 的意义不在于立即替代成熟浏览器，而在于证明一个不依赖现有内核、只专注浏览器的开源项目已经能跑起来；但兼容性、安全性和性能仍是它走向 2028 正式版前必须补齐的短板。

**标签**: `#Ladybird`, `#浏览器内核`, `#开源浏览器`, `#Alpha 发布`, `#上手体验`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [报道称美商务部施压英特尔交出 10%股份](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 9.0/10

据《连线》援引法庭文件报道，2025 年 8 月美国商务部律师在一通电话中警告英特尔首席财务官，董事会可以拒绝交出 10%股份，但将面临“无法预测的后果”。几天后英特尔董事会交出了这批股份，特朗普随后称美国政府“完全拥有并控制”英特尔 10%的股份且未支付对价，按报道这批股份现值约 110 亿美元。

telegram · zaihuapd · 11月25日 13:25

**「背景」** 据《纽约时报》报道，特朗普政府已在英特尔等多家私营企业取得持股，此次围绕英特尔 10%股份的安排属于政府直接入股企业这一罕见做法的延续。

**「影响」** 若该报道属实，英特尔现有股东将在政府未支付对价的情况下让出 10%股份对应的权益，而美国政府则罕见地成为一家主要芯片制造商的实际股东；此类直接持股在美国争议很大，2008-2009 年金融危机期间对通用汽车和 AIG 的临时持股是少数先例。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>
<li><a href="https://www.npr.org/2025/08/22/nx-s1-5509673/trump-says-us-government-will-take-stake-intel">Intel will give the U . S . government a 10 % stake , Trump says : NPR</a></li>
<li><a href="https://techcrunch.com/2025/08/22/u-s-government-plans-to-take-a-10-stake-in-intel/">US government plans to take a 10 % stake in Intel | TechCrunch</a></li>

</ul>
</details>

**标签**: `#美国商务部`, `#英特尔`, `#政府持股`, `#半导体产业`, `#产业政策`

---

<a id="item-finance-news-2"></a>
### [美国提议对 14 个贸易伙伴加征第 301 条新关税](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

美国政府周三提议依据 1974 年《贸易法》第 301 条，对中国、欧盟、日本、印度等 14 个贸易伙伴加征按国别设定的新关税，具体税率将于周三在《联邦公报》公布。方案称，对华将在 2018 年已加征的 25%之上再加 20%；若中国未遵守 2025 年 10 月在韩国釜山达成的贸易休战协议，对华新关税可能升至 40%。

telegram · zaihuapd · 11月25日 13:59

**「背景」** 美国 1974 年《贸易法》第 301 条授权美国贸易代表办公室调查他国贸易做法，并可据此加征关税；而拟对中国升至 40%附加税的前提，是 2025 年 10 月在韩国釜山达成的中美贸易休战协议。

**「影响」** 若措施实施，向美国出口相关商品的海外厂商和依赖这些进口商品的美国企业将承担按国别设定的额外关税成本；目前该方案仍属提议，税率和适用范围以《联邦公报》公布为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.congress.gov/crs_external_products/IF/PDF/IF11346/IF11346.31.pdf">Section 301 of the Trade Act of 1974 - Congress.gov</a></li>
<li><a href="https://www.aa.com.tr/en/americas/us-presses-china-to-immediately-honor-busan-trade-commitments/4114671">Anadolu Ajansı: US presses China to ‘immediately’ honor Busan trade ...</a></li>

</ul>
</details>

**标签**: `#US trade policy`, `#Section 301 tariffs`, `#China-US trade`, `#EU trade`, `#global supply chains`

---

<a id="item-finance-news-3"></a>
### [英国能源账单明年 1 月起上涨 26%](https://www.bbc.co.uk/news/articles/cm20qnq33e90o?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

英国能源监管机构 Ofgem 表示，明年 1 月起，用量典型的家庭年度能源账单将从 1,723 英镑升至 2,166 英镑，涨幅 26%，反映天然气批发成本飙升。该数字为三个月的价格上限，只有在全年维持这一水平时才成立。

rss · BBC Business · 11月25日 13:42

**「背景」** 英国能源监管机构 Ofgem 的居民能源价格上限以三个月为周期调整，此次 1 月至 3 月的上限根据过去三个月供应商支付的批发天然气价格上涨 33%设定。

**「影响范围」** 这次上调直接影响到未签订固定费率合约、受价格上限保护的英国家庭——他们从明年 1 月起将按新的上限支付燃气和电费。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>
<li><a href="https://www.independent.co.uk/news/uk/home-news/energy-price-cap-increase-cost-b3091156.html">Energy bills to soar to £ 2 , 166 a year as energy price cap rises again</a></li>
<li><a href="https://www.independent.co.uk/news/uk/home-news/energy-price-cap-increase-cost-b3091156.html">Energy bills to soar to £2,166 a year as energy price cap rises again</a></li>
<li><a href="https://www.bbc.co.uk/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>

</ul>
</details>

**标签**: `#energy prices`, `#household bills`, `#gas prices`, `#cost of living`, `#UK economy`

---

<a id="item-finance-news-4"></a>
### [Shein 同意支付 1 亿美元和解美国消费者误导指控](https://www.ft.com/content/0128d44e-8ca1-49b8-868b-b8fe0e4824c6?syn-25a6b1a6=1) ⭐️ 7.0/10

据英国《金融时报》报道，快时尚零售商 Shein 已同意支付 1 亿美元，以了结美国监管机构对其误导消费者的指控。监管方称，Shein 在棉质面料的产地来源上作出误导性陈述，并压制负面评价；报道未说明具体监管机构及和解协议的完整条款。

rss · FT Markets · 11月25日 11:18

**「背景」** 美国联邦贸易委员会（FTC）是美国的消费者保护机构，其指控 Shein 让消费者难以解决购买问题、未兑现配送承诺、压制负面评论，并在供应链和棉花产地方面作出误导性陈述；此次 1 亿美元被描述为消费者赔偿。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ftc.gov/news-events/news/press-releases/2026/11/shein-pay-100-million-over-allegations-deceptive-unfair-practices">SHEIN to Pay $100 Million Over Allegations of Deceptive and ...</a></li>
<li><a href="https://www.reuters.com/world/shein-pay-100-million-settle-us-claims-ftc-official-says-2026-11-24/">Shein to pay $100 million to settle US claims, FTC official says</a></li>
<li><a href="https://www.cbsnews.com/news/shein-100-million-ftc-deceptive-practices-settlement/">Shein to pay $100 million to settle federal claims that it ...</a></li>

</ul>
</details>

**标签**: `#Shein`, `#US consumer protection`, `#regulatory settlement`, `#fast fashion`, `#cotton sourcing claims`

---

<a id="item-finance-news-5"></a>
### [韩国央行加息 0.25 厘至 3.25 厘 上调今明两年增长预测](https://news.rthk.hk/rthk/ch/component/k2/1879324-20261126.htm) ⭐️ 7.0/10

韩国央行宣布加息 0.25 厘，指标利率升至 3.25 厘，创两年高位，符合市场预期；货币政策委员会以 5 票赞成、2 票反对通过。央行同时将今年经济增长预测上调至 3.9%、明年上调至 4.1%，并预计通胀将在相当长时间内维持在目标水平以上。

rss · RTHK Finance · 11月26日 02:11

**「背景」** 韩国央行实行通胀目标制，以中期消费物价通胀 2%为目标，并对通胀持续高于或低于目标同样重视。行长申铉松在 2026 年 10 月曾表示，核心通胀明年将高于 2%的目标，到 2028 年才会接近该水平。

**「影响」** 指标利率上升会传导至与政策利率挂钩的房贷和企业贷款，因此背负浮动利率房贷的韩国家庭及借贷企业，还款成本将相应增加。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bok.or.kr/eng/main/contents.do?menuNo=400015">| Inflation Targeting | Objectives &amp; Framework of Monetary ...</a></li>
<li><a href="https://www.bok.or.kr/eng/main/contents.do?menuNo=400530">General Principles of Monetary Policy Operation</a></li>
<li><a href="https://en.sedaily.com/economy/2026/10/22/bok-chief-says-inflation-to-reach-2-percent-target-in-2028">BOK Chief Says Core Inflation to Near 2% Target in 2028</a></li>

</ul>
</details>

**标签**: `#南韩央行`, `#利率`, `#通胀`, `#经济预测`, `#货币政策`

---