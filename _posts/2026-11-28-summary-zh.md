---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 129 条内容中筛选出 22 条重要资讯。

---

**科技新闻**
1. [谷歌 DeepCrossAttention：同等质量下宣称最高快 3 倍](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSec 披露 Linux nfsd 预认证堆溢出漏洞（CVSS 9.8）](#item-tech-news-2) ⭐️ 8.0/10
3. [报告称购物网站盗刷脚本用 WebRTC 外传支付数据](#item-tech-news-3) ⭐️ 7.0/10
4. [多州总检察长起诉 SpaceX，要求阻止 Grok 生成儿童性虐待及非自愿私密图像](#item-tech-news-4) ⭐️ 7.0/10
5. [计算机验证证明的可靠性之争](#item-tech-news-5) ⭐️ 7.0/10
6. [SemiAnalysis 深挖 Trainium3：DGE 微架构与推理性价比](#item-tech-news-6) ⭐️ 7.0/10
7. [美政府被指施压 Intel 出让 10%股份](#item-tech-news-7) ⭐️ 7.0/10
8. [《我的世界》基岩版资源包漏洞影响 26.52–26.63，26.65 已修复](#item-tech-news-8) ⭐️ 7.0/10
9. [微软推进 Windows 内置驱动替代第三方驱动](#item-tech-news-9) ⭐️ 7.0/10

**科技博客**
1. [听书台：在真实使用中迭代需求](#item-tech-blog-1) ⭐️ 5.0/10
2. [2020–2026：机械硬盘每 TB 价格从约 110 元涨到近 200 元](#item-tech-blog-2) ⭐️ 5.0/10
3. [Optimizely 脚本被篡改，旧版 iOS 仅打开网页即可能被入侵](#item-tech-blog-3) ⭐️ 4.0/10
4. [NodeWarden 九个月更新：离线、云备份与多用户](#item-tech-blog-4) ⭐️ 4.0/10

**财经新闻**
1. [国常会部署加力发挥“国家队”稳市作用](#item-finance-news-1) ⭐️ 8.0/10
2. [标普 500 指数进入回调，熊市并不必然意味着经济衰退](#item-finance-news-2) ⭐️ 7.0/10
3. [BBC：伊朗战争推高气价，数百万家庭 1 月能源账单将涨 26%](#item-finance-news-3) ⭐️ 7.0/10
4. [人行报告：灵活运用货币政策工具并研究非银流动性支持](#item-finance-news-4) ⭐️ 7.0/10
5. [美团第 3 季扭亏为盈 净利润 20.7 亿元人民币](#item-finance-news-5) ⭐️ 7.0/10
6. [港股升 467 点 恒指涨 2.1% 科指急升近 6.5%](#item-finance-news-6) ⭐️ 7.0/10
7. [国务院常务会议研究深化资本市场投融资改革](#item-finance-news-7) ⭐️ 7.0/10
8. [国务院常务会议释放稳市场信号，A 股午后大涨，创业板指升 11.61%](#item-finance-news-8) ⭐️ 7.0/10
9. [央行发布大额存单新规 个人起购门槛降至 10 万元](#item-finance-news-9) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [谷歌 DeepCrossAttention：同等质量下宣称最高快 3 倍](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 8.0/10

谷歌研究博客介绍了 DeepCrossAttention，一种针对 Transformer 残差连接的注意力改进方法，宣称能在模型质量相当的情况下实现最高 3 倍的速度提升。该说法面向依赖 Transformer 的训练和推理场景，但所给材料没有提供基准设置、实现细节或独立复现结果。因此，目前可以确认的是谷歌研究博客中的性能主张，而非已发布产品或第三方实测结论。

hackernews · ComputedCamp995 · 11月27日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50672565)

**「背景」** Transformer 通常通过残差连接将每个子层的输出与输入相加，使信号能够跨层传递；Google 的 DeepCrossAttention 则改用可学习、依赖输入的权重和跨层注意力，动态组合前面各层的信息，以缓解传统残差连接中的信息稀释。Google 在 2025 年 2 月的 arXiv 论文中介绍了这一架构，此次 Google Research 博客再次对其进行了说明。

**「对开发者的影响」** 对于需要训练深层 Transformer 的团队，DCA 意味着要改动模型代码中的残差相加逻辑，把它换成可学习的逐 token 路由和跨层注意力，因此无法只靠调参获得这项收益。Google 声称训练速度最高可提升 3 倍，但该数字来自厂商博客、在 ICML 2025 上报告的成果，目前尚无独立复现，采用前应先在自身负载上做基准对照。

**「社区讨论」** 在 Hacker News 讨论中，有评论者批评谷歌研究博客中的折线图不合适，认为不同方法之间没有时间或连续关系，应改用柱状图；也有人追问该技术能否与 MTP、DFlash 等已有加速方法叠加，把吞吐量从过去两年 reportedly 的 10 倍进一步提升到 30 倍。另有评论者将其与 DenseNet 类比，并对 Gemini 的便宜和快速作出未经证实的猜测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections - Google Research</a></li>
<li><a href="https://arxiv.org/abs/2502.06785">[2502.06785] DeepCrossAttention: Supercharging Transformer ...</a></li>
<li><a href="https://explainx.ai/blog/google-deepcrossattention-transformer-residual-connections-2026">DeepCrossAttention (DCA): Google Fix for Deep Transformers ...</a></li>
<li><a href="https://aiweekly.co/alerts/googles-deepcrossattention-trains-transformers-up-to-3x-faster">Google&#x27;s DeepCrossAttention trains transformers up to 3x ...</a></li>

</ul>
</details>

**标签**: `#transformer efficiency`, `#attention mechanisms`, `#Google Research`, `#model optimization`, `#AI infrastructure`

---

<a id="item-tech-news-2"></a>
### [OpenSec 披露 Linux nfsd 预认证堆溢出漏洞（CVSS 9.8）](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

据 OpenSec 披露，Linux 内核 NFS 服务器 nfsd 存在预认证堆溢出漏洞 CVE-2026-99362（CVSS 9.8），攻击者无需登录，仅通过发往 tcp/2049 的连接即可越界写入内核堆并获取 root shell。该漏洞自 Linux 3.16 起存在，影响启用 NFSv4.1 或 4.2 的文件服务器、NAS 和集群存储节点。修复版本为 6.12.117、6.18.61、7.3.2 和 7.4-rc1，需升级内核并重启；无法立即升级时可限制 tcp/2049 访问。CVE 于 2026 年 11 月 20 日公开，当前来源未给出利用代码或独立复现结果。

telegram · zaihuapd · 11月27日 12:57

**「技术背景」** NFSv4.1 引入会话（session）与槽位应答缓存机制，服务器会为每个会话槽位缓存应答，以便客户端重传时复用。据 Red Hat 的漏洞记录，客户端可通过协商极小的缓存应答大小，再发送携带 SEQUENCE 操作的复合请求，使服务器把完整应答复制进过小的缓冲区，从而造成越界写（CVE-2026-99362）。因此该缺陷位于 nfsd 的 NFSv4.1/4.2 会话应答缓存路径上，只要主机 TCP 2049 端口可达，客户端即可在通过任何身份验证之前触发。

**「影响与处置」** 对暴露 tcp/2049 且启用 NFSv4.1/4.2 的文件服务器、NAS 和集群存储节点，管理员需升级到 6.12.117、6.18.61、7.3.2 或 7.4-rc1 并重启内核；无法立即完成时，应先用防火墙限制 tcp/2049 访问作为临时缓解，而不能替代补丁。Red Hat 对该漏洞评分为 9.4（内核 CNA 为 9.8），并指出远程客户端可通过协商最小缓存回复大小并发送含 SEQUENCE 操作的复合请求触发越界写。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://rokkhe.hashnode.dev/nfs2root-cve-2026-99362-linux-nfsd">NFS2ROOT (CVE-2026-99362): what it is, who is exposed, and ...</a></li>
<li><a href="https://computingforgeeks.com/nfs2root-cve-2026-99362/">NFS2ROOT (CVE-2026-99362): Check, Patch, Mitigate ...</a></li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://computingforgeeks.com/nfs2root-cve-2026-99362/">NFS2ROOT (CVE-2026-99362): Check, Patch, Mitigate ...</a></li>

</ul>
</details>

**标签**: `#Linux kernel`, `#NFS`, `#security vulnerability`, `#CVE-2026-99362`, `#privilege escalation`

---

<a id="item-tech-news-3"></a>
### [报告称购物网站盗刷脚本用 WebRTC 外传支付数据](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

InfoHawk 于 2026 年 11 月 27 日（黑色星期五当天）发布的报告称，热门购物网站上发现信用卡盗刷脚本，这些脚本利用 WebRTC 将窃取的支付数据外传，以规避常见的流量监控。报告将其描述为 Magecart 类攻击的一次手法演变，但现有材料未提供受影响网站名称、脚本样本、感染规模或被绕过监控的具体类型，因此这些细节仍属未经独立核实的厂商说法。

hackernews · scanr · 11月27日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50668145)

**「背景：Magecart 与 WebRTC 绕过」** Magecart 类攻击通常指向电商网站注入数字信用卡窃取脚本，在用户结账时读取支付数据。据一份 LinkedIn 帖子描述，采用 WebRTC 的窃取脚本可通过 DataChannel 传输数据，从而绕开 HTTP\(S\) 和 CSP 的控制，接收恶意载荷并外传卡号。

**「影响」** 对电商和支付安全团队而言，直接后果是结账页面的第三方脚本治理与监控范围需要覆盖 WebRTC 等非 HTTP 通道；若只监控常规网络请求，可能会漏掉此类外传行为。由于报告未说明具体检测方式，实际需要调整哪些监控规则仍需结合自身流量审计确认。

**「社区讨论」** 评论者 afavour 认为问题不在 WebRTC 的技术特性本身，而在于它较少被监控，同样的外传用普通 HTTP 请求也能完成，只要页面嵌入第三方脚本就始终存在风险；jszymborski 则以这类事件为由，认为拦截广告和第三方脚本是合理的自保手段。另有评论者（snickerer、s\_u\_d\_o）主张浏览器不应执行来自陌生方的代码、广告也应被沙箱化，但这些属设计层面的观点，而非已验证的修复方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/write2nishan_webrtc-skimmer-bypasses-csp-to-steal-payment-activity-7443480737682526208-kq-S">WebRTC Skimmer Bypasses CSP to Steal Payment Data | LinkedIn</a></li>
<li><a href="https://www.akamai.com/glossary/what-is-magecart">What Is Magecart ? | Akamai</a></li>
<li><a href="https://www.retailtouchpoints.com/executive-viewpoints/magecart-meet-the-cybercriminals-silently-stealing-payment-data-from-websites/99630/">Magecart : Meet the Cybercriminals Silently... - Retail TouchPoints</a></li>

</ul>
</details>

**标签**: `#web security`, `#credit card skimming`, `#WebRTC`, `#third-party scripts`, `#e-commerce`

---

<a id="item-tech-news-4"></a>
### [多州总检察长起诉 SpaceX，要求阻止 Grok 生成儿童性虐待及非自愿私密图像](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

多个州的总检察长对 SpaceX 及其关联的 xAI/Grok 提起诉讼，要求法院阻止 Grok 生成儿童性虐待材料和非自愿私密图像，并指控该平台推广此类内容。起诉目前只是州检察长办公室的指控，尚非法院认定的事实；公开材料也未说明 Grok 的具体防护机制为何失效。对 Grok 的运营方和用户而言，这意味着相关图像生成能力可能面临禁令或更严格的过滤要求，但在裁决前仍属未决诉讼。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**「背景」** Grok 是 xAI 的生成式 AI 产品，争议集中在模型如何处理涉及真实人物或未成年人的图像请求，以及平台应承担何种审核责任。此次诉讼不是产品版本更新，而是把生成式 AI 的输出责任带入法院审查。

**「影响」** 若法院支持禁令请求，Grok 可能被要求阻止或过滤相关请求和输出，运营方还需面对诉讼带来的合规与内容审核调整；这些后果取决于案件进展，目前尚未发生。

**「社区讨论」** 评论者质疑 Grok 此前是否已全面禁止这类内容，还是用户必须绕过限制才能生成，并追问制作图像的个人是否应被追责。另有评论者声称美国最高法院已裁定，为个人消费而用 AI 制作儿童性虐待材料受言论保护、但不得涉及真实儿童；这是评论中的法律主张，并非本文核实的事实。

**标签**: `#AI safety`, `#content moderation`, `#generative AI`, `#legal/regulation`, `#xAI/Grok`

---

<a id="item-tech-news-5"></a>
### [计算机验证证明的可靠性之争](https://cr.yp.to/proofs/falseccp.html) ⭐️ 7.0/10

一篇题为《False computer-checked proofs》的文章主张，形式验证的使用者和开发者不应把“计算机检查通过”当作命题为真的充分条件，并呼吁为证明助手和检查器提供更高保障。文章没有发布新工具、版本或基准结果，而是围绕 Lean、Metamath 等系统的健全性缺陷，讨论计算机验证证明在什么条件下才值得信任。

hackernews · \_tk\_ · 11月27日 15:26 · [社区讨论](https://news.ycombinator.com/item?id=50667989)

**「背景」** 形式化证明的信任通常集中在一个尽量小的内核上：只要内核接受每一步，整个定理就被视为已检查。2026 年 10 月披露的 CVE-2026-72844 表明 Lean 4 内核存在可靠性漏洞，可在不使用公理、sorry、unsafeCast 或篡改 .olean 文件的情况下构造通过检查的 False 证明；相关事后分析还指出，独立 Rust 检查器 nanoda 因另一个投影节点验证 bug 未能拦住该无效证明。

**「冗余检查成为实际约束」** 对于把形式化验证用于高风险场景的团队，实际约束是：只要单个证明检查器（kernel）存在一个 soundness bug，整条验证链就可能失效，因此需要冗余检查。评论者指出，Metamath 的 set.mm 与 iset.mm 要求证明通过 5 个由不同作者用不同语言实现的独立验证器才能入库；还有评论者举例称，有研究者分别利用 Lean 和当时仅发布一周的 nanoda 各自的不同 bug，构造出能同时通过两者的“证明”。因此，在选型或验收时，应确认是否存在独立的交叉检查路径，而不是只依赖单一证明助手。

**「社区讨论」** 评论者主要质疑文章对风险规模的呈现：twotwotwo 表示健全性 bug 确实存在，但要让错误证明误导数学家，需要多套检查器同时被攻破，且输入在非正式审阅中不显可疑；他还举例称，有 DeepMind 研究者利用 Lean 与当时刚发布一周的 nanoda 各自的不同 bug，让同一“证明”通过。dwheeler 补充，Metamath 的 set.mm 和 iset.mm 要求 5 个不同语言实现的独立验证器全部通过，因此用单个 C 验证器的历史 bug 概括整个系统会误导；gr\_norm 认为这些健全性 bug 少到“能放进一条推文”，对 99.9% 的软件已足够可靠；andai 则提醒，形式化证明可能只是证明了系统对需求的错误理解，不过他假设数学证明因问题已由人符号化而较不易受此影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aitoolly.com/ai-news/article/2026-08-02-lean-kernel-soundness-bug-14576-postmortem-of-the-ai-assisted-collatz-conjecture-disproof-and-fix">Lean Kernel Bug #14576: Postmortem and Technical Analysis | AIToolly</a></li>
<li><a href="https://www.openwall.com/lists/oss-security/2026/10/26/2">oss-security - CVE-2026-72844: Lean 4 kernel soundness bug ...</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#proof assistants`, `#soundness`, `#Lean`, `#Metamath`

---

<a id="item-tech-news-6"></a>
### [SemiAnalysis 深挖 Trainium3：DGE 微架构与推理性价比](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

SemiAnalysis 发布对 AWS Trainium3 的架构与推理性能深度评测，指出其微架构从底层就以 tile（瓦片）为一等原语设计，而非像 Nvidia GPU 那样在通用图形/线程架构上逐代加装 Tensor Core、TMA、Tensor Memory 等 AI 专用单元。该文称，Trainium 的 Descriptor Generation Engines（DGE，对应 Nvidia TMA 与 AMD MI455X TDM）在其微基准中能在较小消息尺寸下达到峰值 HBM 带宽利用率（MBU），作者称这在 Nvidia GPU 上无法实现。评测还称，在承载真实编码智能体会话回放的 AgentX 端到端负载上，Trainium3 搭配 PDS 与 vLLM 的每美元吞吐（性能/总拥有成本）在整个“TCO 对 p90 交互性”曲线上优于除 Vera Rubin 以外的所有加速器。上述数字来自 SemiAnalysis 自建的 InferenceX/UBenchX 基准，文章摘录未给出绝对性能数值，且部分架构细节由 AWS Annapurna Labs 团队协助验证，属评测机构结论而非独立第三方复现。

rss · Semianalysis · 11月27日 15:54

**「背景」** InferenceX（2025 年 10 月以 InferenceMAX 名义推出）是一个持续测量跨 AI 加速器与推理服务软件性能的开源基准；把 Trainium3 纳入同一套吞吐-延迟曲线，才使与 Nvidia GB300 的每美元推理成本比较具备统一口径。架构上，Nvidia 的数据中心 GPU 是从图形处理器出发，逐代加入 Volta 的 Tensor Core、Hopper 的 TMA 和 Blackwell 的 Tensor Memory，而 Trainium 以 tile 为一等原语从零面向 ML 设计，这也是 SemiAnalysis 讨论其 DGE 等微架构差异的起点。

**「影响」** 对正在评估推理硬件的团队而言，这一评测把比较维度从单卡算力转向“特定延迟目标下的每美元 token 成本”，并说明 Trainium3 的优势依赖 PDS 加 vLLM 的软件栈以及小消息下的高 HBM 带宽利用率——这意味着选型时必须锁定相同的 p90 交互性目标与软件版本才能与 GB300 等平台公平对比，同时 Vera Rubin 在该曲线上仍被列为领先者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/inferencex">InferenceX | AI Wiki</a></li>

</ul>
</details>

**标签**: `#AWS Trainium`, `#AI accelerators`, `#inference`, `#microarchitecture`, `#Nvidia`

---

<a id="item-tech-news-7"></a>
### [美政府被指施压 Intel 出让 10%股份](https://arstechnica.com/tech-policy/2026/11/intel-faced-a-choice-give-trump-10-or-face-the-consequences/) ⭐️ 7.0/10

据 Ars Technica 报道，一份联邦诉讼中引用的内部电话记录显示，2025 年 8 月，美国商务部律师 David Shapiro 要求 Intel 首席财务官向美国政府出让 10%股份，并称这不是谈判、总统计划在当周五宣布协议。记录还称，Intel 董事会可以选择拒绝，但 Shapiro 表示拒绝会带来他无法预料的后果。上述内容来自为 Intel 董事准备的讲话摘要，报道未说明该要求最终是否被接受。

rss · Ars Technica · 11月27日 12:05

**「背景」** 据《纽约时报》2025 年 11 月的报道，特朗普政府正以数十亿美元规模入股英特尔等私营企业，由政府直接持有企业股权的做法不同寻常，且当时没有放缓迹象（tool-2-3）。英特尔是总部位于加州圣克拉拉的美国芯片设计与制造企业（tool-2-1），也是这类政府入股交易中被公开提及的典型案例（tool-2-3）。

**「影响」** 对 Intel 及其董事会而言，直接后果是必须在接受政府持股与承受未具体说明的后果之间权衡；若政府入股，Intel 的股权结构和董事会决策将直接受美国政府股东身份影响，若拒绝，记录中所谓“无法预料的后果”则意味着公司需把监管与政治风险纳入决策。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Intel">Intel - Wikipedia</a></li>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>

</ul>
</details>

**标签**: `#Intel`, `#semiconductor industry`, `#US tech policy`, `#government intervention`, `#corporate governance`

---

<a id="item-tech-news-8"></a>
### [《我的世界》基岩版资源包漏洞影响 26.52–26.63，26.65 已修复](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

附加组件开发者 8Crafter 于 11 月 15 日在 Reddit 公开称，《我的世界》基岩版 26.52 至 26.63 存在资源包漏洞：含 content.zipe 的资源包可改动 Ore UI 文件并运行隐藏脚本，更早版本也可能受影响；PC、手机和主机均受影响，Java 版不受影响。玩家加入服务器或 Realm 且开启资源包自动下载时，可能无需手动安装就收到问题文件；8Crafter 列举的利用方式包括删除全部存档、获取玩家 IP，以及在 Windows 上于特定条件下无提示打开任意 URI、启动资源包内的批处理文件下载恶意软件。Mojang 已在 26.65 版修复；AxmBro 发布的 Windows 只读检测工具可查找 content.zipe，但不能判定资源包是否恶意。

telegram · zaihuapd · 11月27日 18:04

**「背景」** 在基岩版中，资源包用于替换纹理、音效和界面素材；当玩家加入服务器或 Realm 并开启资源包自动下载时，客户端可能无需手动安装就能收到并加载这些包。Ore UI 是基岩版构建游戏界面的框架，因此对 Ore UI 文件的改动会作用于客户端界面层。

**「影响」** 仍在使用 26.52 至 26.63 的玩家应在加入服务器或 Realm 前升级到 26.65，或关闭资源包自动下载；服务器和 Realm 管理者则需检查资源包中是否含 content.zipe，不能仅凭检测工具的结果认定资源包安全。

**标签**: `#Minecraft Bedrock`, `#security vulnerability`, `#resource packs`, `#game security`, `#patch release`

---

<a id="item-tech-news-9"></a>
### [微软推进 Windows 内置驱动替代第三方驱动](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

微软在 Ignite 2026 大会上确认，正为整类硬件开发 Windows 内置驱动，以减少进入系统内核的第三方代码，部分第三方驱动未来可能被内置功能取代。打印机是首个重点：近期推出的 Windows Ready Print 模式用于取代旧式第三方打印驱动；微软产品经理 Mehmet Kucukgoz 称，SoundWire、SDCA 等音频类驱动将很快成为 Windows 内置组件，I3C 总线、USB 以太网和 MIPI 摄像头类驱动仍在开发中。微软还推出驱动质量倡议（DQI），旨在提升驱动的可靠性、质量和安全标准，并鼓励第三方开发者尽量使用内置驱动，OEM 的定制驱动也应遵循这一思路。

telegram · zaihuapd · 11月28日 02:09

**「背景」** Windows 的驱动通常分为随系统提供的内置驱动（in-box driver）和由硬件厂商、OEM 或芯片厂商单独提供的第三方驱动；后者往往以内核模式运行，会直接影响系统稳定性和安全边界。把整类设备驱动收归内置，意味着微软要维护面向该类硬件的通用驱动，而硬件厂商的驱动交付和定制方式也会随之改变。

**「影响」** 对打印设备厂商和驱动开发者而言，旧式第三方打印驱动将首先被 Windows Ready Print 取代；音频、I3C、USB 以太网和 MIPI 摄像头类内置驱动尚在开发，微软未披露具体版本或兼容性安排。OEM 与第三方驱动团队被要求按 DQI 提高可靠性、质量和安全标准，并优先采用内置驱动。

**标签**: `#Windows`, `#device drivers`, `#Microsoft`, `#kernel security`, `#hardware ecosystem`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [听书台：在真实使用中迭代需求](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=197002) ⭐️ 5.0/10

rss · Dapenti Xilei · 11月28日 03:19

**「背景」** 作者以自制的“听书台”为例，说明音频生成产品中的细节需求往往无法预先想全。这个工具已为“图卦”等内容生成 241 小时、4 万余条音频段落，最长的一本 700 页书约 19 小时、1GB。作者认为，“一句提示词”适合简单需求，复杂或起初并不清楚的需求只能在真实使用中发现。

**「方案」** 他列举了多个由具体使用倒逼出的功能：有听众觉得男女声播客里的男声过于低沉，界面上便出现“男声+0.5”选项，在最终合成时稍微提高男声音量；多音字容易读错，就临时用别字指定读音，生成后再改回；长段落让模型吃力，就自动拆分；场景或章节切换处加停顿，避免听众误以为出错；前言和注释则可忽略不读。系统还支持 A/B 角色、自动分段、收藏好段落以汇总“吐槽”、勾选导出部分音频，以及独立于生成过程的异步复检；需要重生成的片段可插队，完成后自动回到待复听队列。作者称这些只是主要部分，每个按钮都对应实际遇到的问题，而修改以不影响整体、兼容多数需求为原则。

**「启示」** 作者由此强调，即便简单应用也包含大量无法预先设想的细节，只有真实需求和持续迭代才能形成具体可用的东西；缺少具体实践，理念就得不到正确反馈，真实知识或共识也难以建立。他把这一逻辑从软件延伸到了社会。

**标签**: `#TTS`, `#需求迭代`, `#音频生产`, `#产品设计`, `#LLM 工作流`

---

<a id="item-tech-blog-2"></a>
### [2020–2026：机械硬盘每 TB 价格从约 110 元涨到近 200 元](https://www.appinn.com/hard-drive-price-2026/) ⭐️ 5.0/10

rss · Appinn · 11月27日 12:24

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/hard-drive-price-2026/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;小众软件作者青小蛙自 2020 年起持续推荐亚马逊海外购的大容量机械硬盘，这些历年促销文章无意间记录下了一组价格。2026 年黑五，他把旧文与当年报价放在一起比较，发现长期稳定的每 TB 价格已经明显跳涨。

**「方案」** 作者汇总了西部数据 Elements、My Book 等外置机械硬盘的含税到手价：2020 年至 2025 年，大容量机械硬盘的促销价基本维持在 110 元/TB 左右，2020 年 12 月 14TB 为 111.07 元/TB，2025 年 11 月 20TB 为 106.48 元/TB，2025 年 12 月他甚至感叹“有货就是王道”。而 2026 年黑五美亚报价按 1:7 折算、未含税费与跨境运费，每 TB 约为 192 至 292 元；同样是西数 20TB，价格从 2025 年的 2129.58 元升至约 3850 元，高出约 81%。国外博主 Alex Kretzschmar 的记录也显示同样趋势：Best Buy 同款西数 EasyStore 20TB 在 2024 年黑五卖 249.99 美元，2026 年卖 549.99 美元，两年涨了 300 美元、涨幅 120%，2026 年的每 TB 价格（27.50 美元）比 2018 年还高 53%；照此计算，2024 年花 1000 美元买 4 块 20TB 硬盘组建 NAS，今年仅硬盘就要约 2200 美元。作者也说明，样本来自非系统的促销文章历史，未进一步分析涨价成因。

**「启示」** 作者的核心结论是：大容量机械硬盘延续多年的约 110 元/TB 低价时代已在 2026 年黑五被打破，价格接近翻倍。对依赖机械硬盘扩容的 NAS 与自建存储用户来说，按旧价格估算的存储成本需要重新评估。

**标签**: `#机械硬盘价格`, `#存储成本`, `#黑五促销`, `#价格追踪`, `#NAS`

---

<a id="item-tech-blog-3"></a>
### [Optimizely 脚本被篡改，旧版 iOS 仅打开网页即可能被入侵](https://www.appinn.com/iphone-web-attacks-coruna-darksword/) ⭐️ 4.0/10

rss · Appinn · 11月28日 01:13

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/iphone-web-attacks-coruna-darksword/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;11 月 16 日，为网站提供页面版本测试服务的 Optimizely 脚本被攻击者植入恶意代码，访客照常打开网站就会把恶意代码一起带进来；同一时期，Coruna 与 DarkSword 两套网页攻击工具被指能让旧版 iOS 设备“只打开网页就中招”。

**「方案」** 作者引用 Report URI 的排查：在 1611 份脚本中有 188 份被篡改，涉及 178 家机构，包括 BBC、CNN、Zoom、GitLab、宜家和汇丰。这段代码能把用户复制的加密货币收款地址换成攻击者的地址，也有版本会收集网页表单中填写的银行卡资料，并在遇到运行旧系统的 iPhone 或 iPad 时尝试用 Coruna、DarkSword 入侵。Optimizely 称当天已清除受影响项目里的恶意代码，Report URI 当晚复查也未再发现异常脚本，截至 11 月 25 日 Optimizely 仍未收到设备感染报告。作者强调，这类攻击发生在浏览器处理网页内容的过程中，用户无需下载 App、填写密码或点击“允许”；Coruna 涉及 iOS 13 至 17.2.1，DarkSword 涉及 iOS 18.4 至 18.7，Google 自 2025 年 11 月起已在真实攻击中发现后者，苹果随后扩大 iOS 18.7.7 的适用范围以提供修复。作者给出的应对办法是把系统升到设备能装的最高版本：iPhone 11 及更新机型装 iOS 27.2.1，XS、XS Max、XR 装 18.7.12，8、8 Plus、X 装 16.7.16，6s、7 和第一代 SE 装 15.8.8；仍停留在 iOS 13 或 14 的设备需先升到至少 iOS 15。

**「启示」** 作者的结论是：第三方脚本带来的供应链风险和网页即触发（无需交互）的攻击方式，让“只是看看网页”本身成为可被利用的入口；对无法升级到新系统的旧设备，及时打补丁几乎是唯一现实可行的自保手段，作者也坦言除此之外并无更好办法。

**标签**: `#iOS安全`, `#供应链攻击`, `#浏览器漏洞`, `#恶意脚本`, `#安全更新`

---

<a id="item-tech-blog-4"></a>
### [NodeWarden 九个月更新：离线、云备份与多用户](https://www.appinn.com/nodewarden-update-1/) ⭐️ 4.0/10

rss · Appinn · 11月27日 09:13

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/nodewarden-update-1/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;NodeWarden 是一个能直接部署在 Cloudflare Workers 上的开源密码管理器，兼容 Bitwarden 官方客户端（浏览器扩展、手机与桌面端），只需把服务器地址改成自己的部署地址即可，无需自备服务器，在免费额度内就能运行。作者今年 2 月首次介绍它，9 个月过去功能增加了不少，于是再写一篇汇总式更新。

**「方案」** 作者列出的更新中，最实用的是网页密码库支持 PWA：安装到电脑或手机后，只要在线登录并缓存过密码库，断网也能解锁查看，兼容设备上还能用 Passkey 离线解锁。内置的云备份中心可定时增量备份到 WebDAV 和 S3 兼容存储，并预设了 Cloudflare R2、Backblaze B2、Tigris 等配置。多用户方面，部署后第一个注册者成为管理员，之后用邀请码拉人，每人有独立密码库，但暂不支持 Bitwarden 的组织与共享集合。新增的密码安全检测页可查弱密码、重复密码、已泄露密码和未开启双重验证的账户，并附密码生成器、重复条目清理；登录方式上支持 TOTP、YubiKey OTP、Passkey 以及用已登录设备授权新设备，还能管理或撤销设备信任——其中 TOTP 在原版 Bitwarden 属付费功能，这里可免费用。此外还有多设备实时增量同步与移动端推送、Send、扫码添加 TOTP、等效域名、更多条目类型、KeePass CSV 导入、隐藏网页入口等。升级只需在自建 fork 上 Sync fork、Update branch，等 Cloudflare 自动构建部署，数据库会自动完成结构升级，不用写 SQL 或重新导入数据；但 2 月部署的老版本要检查 Node.js 24.22.1 与 NODE\_VERSION、保留原 JWT\_SECRET、保留数据库与附件存储及 Durable Objects 绑定，并且务必先做完整备份。作者也提醒，NodeWarden 是与 Bitwarden 官方无关的独立第三方项目，折腾前可先用在线 DEMO 体验。

**「启示」** 对不想维护服务器又想自建密码库的人来说，NodeWarden 已从“能在免费额度上跑起来”发展到日常可用的程度，离线访问与自动云备份补上了自托管最要紧的两块短板；但它仍是第三方项目，安全与信任取舍需要使用者自己判断，作者的建议是先看 DEMO 再动手。

**标签**: `#Bitwarden 兼容`, `#Cloudflare Workers`, `#自建密码管理器`, `#开源项目更新`, `#PWA 离线`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [国常会部署加力发挥“国家队”稳市作用](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 8.0/10

国务院总理李强 11 月 27 日主持召开国务院常务会议，提出加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准基金”功能并提供充足流动性保障，同时完善保险、企业年金、社保基金等中长期资金入市支持引导政策。会议还要求依法强化资本市场全链条监管，坚决查处财务造假、违规减持等行为。

telegram · zaihuapd · 11月27日 05:35

**「背景」** “国家队”在此指以中央汇金公司为代表的国有稳市资金；“类‘平准基金’”指这类资金在市场波动时提供流动性、稳定市场预期的安排。此次国务院常务会议将其纳入资本市场稳市机制部署。

**「影响」** 对股票投资者以及保险、企业年金、社保等中长期资金而言，专家认为，优化中央汇金类“平准基金”功能并提供流动性保障，有助于阻断非理性下跌的负反馈循环；但中长期资金仍受考核机制制约，入市支持政策如何落地尚待具体安排。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cls.cn/detail/2546318">cls.cn/detail/2546318</a></li>
<li><a href="https://www.cls.cn/detail/2546577">新华社： 国 常 会 关于 资 本 市 场 部署释放五大鲜明信号</a></li>
<li><a href="https://finance.eastmoney.com/a/202611273941634358.html">如何理解 国 常 会 对 资 本 市 场 的最新定调？ 专家解读来了 _ 东方财富网</a></li>

</ul>
</details>

**标签**: `#资本市场政策`, `#国家队稳市`, `#中央汇金`, `#中长期资金入市`, `#监管执法`

---

<a id="item-finance-news-2"></a>
### [标普 500 指数进入回调，熊市并不必然意味着经济衰退](https://www.cnbc.com/2026/11/27/the-sp-500-is-in-a-correction-bear-markets-and-recessions-dont-always-follow.html) ⭐️ 7.0/10

标普 500 指数在 11 月 20 日收于 6,910.39 点，较 10 月 6 日收盘纪录高点 7,818.93 点下跌 11.6%，进入技术性回调，为 2025 年 4 月以来首次。

rss · CNBC Finance · 11月27日 13:21

**「背景」** 技术性回调通常指较近期高点下跌至少 10%，熊市则指下跌 20%或以上；CNBC 分析称，自 1962 年以来的 13 轮标普 500 熊市中，有 8 轮与美国国家经济研究局（NBER）认定的经济衰退重叠。德意志银行策略师 Henry Allen 表示，本轮下跌尚未伴随衰退、经济数据恶化或美联储加息周期这三个历史上常见的熊市触发因素。

**标签**: `#S&amp;P 500`, `#market correction`, `#recession risk`, `#Federal Reserve`, `#AI spending`

---

<a id="item-finance-news-3"></a>
### [BBC：伊朗战争推高气价，数百万家庭 1 月能源账单将涨 26%](https://www.bbc.co.uk/news/videos/cwjd7y4jk581o?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

BBC Business 报道称，受伊朗战争引发的天然气价格飙升影响，数百万家庭的能源账单将在 1 月上涨 26%。该报道未提供具体的账单金额基准、涨价的确切生效日期，也未说明数据来源。

rss · BBC Business · 11月27日 16:05

**「背景」** 英国对家庭能源账单设有价格上限，即定期设定的供应商可向典型家庭收取的年度费用上限；BBC 将此次 26%的上涨归因于伊朗战事引发的天然气价格飙升，并称按新的典型家庭用量口径，2027 年 1 月起该上限为 2166 英镑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.co.uk/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>
<li><a href="https://www.bbc.com/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>

</ul>
</details>

**标签**: `#energy bills`, `#gas prices`, `#household costs`, `#geopolitical risk`

---

<a id="item-finance-news-4"></a>
### [人行报告：灵活运用货币政策工具并研究非银流动性支持](https://news.rthk.hk/rthk/ch/component/k2/1879533-20261127.htm) ⭐️ 7.0/10

中国人民银行在金融稳定报告中表示，将灵活高效运用多种货币政策工具、保持流动性充裕，并研究建立在特定情景下向非银机构提供流动性的机制性安排。同日国务院常务会议强调资本市场事关经济发展大局，证监会表示将研究推出增量政策，并鼓励上市公司加大分红回购。

rss · RTHK Finance · 11月27日 15:05

**「背景」** 人行定期发表金融稳定报告，而国务院常务会议由总理主持；这次人行、国务院和中证监同日就资本市场表态，构成跨部门协同稳定市场预期的政策背景。

**标签**: `#中国货币政策`, `#资本市场稳定`, `#人行`, `#中证监`, `#流动性支持`

---

<a id="item-finance-news-5"></a>
### [美团第 3 季扭亏为盈 净利润 20.7 亿元人民币](https://news.rthk.hk/rthk/ch/component/k2/1879512-20261127.htm) ⭐️ 7.0/10

美团公布，2026 年第 3 季按年扭亏为盈，录得净利润 20.7 亿元人民币，去年同期亏损 186.3 亿元，但按季比较则下跌约 4%。期内收入约 1156 亿元人民币，按年增长近 22%，按季升逾 10%。

rss · RTHK Finance · 11月27日 09:28

**「背景」** 去年同期的 186.3 亿元亏损，是外卖平台补贴大战所致，也是美团近三年来首次季度亏损（据经济日报报导）；美团表示，上季行业补贴更趋理性，这一低基数是理解本季由亏转盈的前提。

**「影响」** 美团称外卖行业平均客单价按年显著回升、低价订单占比持续下降，这意味着消费者能买到的低价外卖减少、每单平均支出上升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://money.udn.com/money/story/5603/9170382">外 卖 大战拖累 美 团 第 3 季 亏762亿 | 大陆政经 | 两岸 | 经济日报</a></li>

</ul>
</details>

**标签**: `#美团`, `#季度业绩`, `#扭亏为盈`, `#外卖行业`, `#中国平台经济`

---

<a id="item-finance-news-6"></a>
### [港股升 467 点 恒指涨 2.1% 科指急升近 6.5%](https://news.rthk.hk/rthk/ch/component/k2/1879507-20261127.htm) ⭐️ 7.0/10

港股在期指结算日造好，国务院常务会议提出加力发挥“国家队”稳市作用，恒生指数收报 22694 点，升 467 点，涨幅 2.1%。科技指数收报 3637 点，急升近 6.5%，创逾 1 年半以来最大单日涨幅。

rss · RTHK Finance · 11月27日 08:34

**「背景」** 国务院总理李强 11 月 27 日主持召开国务院常务会议，研究持续深化资本市场投融资综合改革，提出加力发挥“国家队”稳市作用，并进一步优化中央汇金公司的类“平准基金”职能，即由中央汇金等国有机构入市买入股票以平抑市场波动。当日港股恰逢期指结算日。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.eastmoney.com/a/202611273941564045.html">国常会：加力发挥“国家队”稳市作用 进一步优化中央汇金公司的类“平准...</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-11-28/doc-inkafyfq5072095.shtml">首提“国家队”，国常会释放稳市信号，机构火速解读_新浪财经_新浪网</a></li>
<li><a href="https://www.thepaper.cn/newsDetail_forward_34573081">国常会：加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准...</a></li>

</ul>
</details>

**标签**: `#Hong Kong equities`, `#China policy`, `#tech rally`, `#semiconductors`, `#market stabilization`

---

<a id="item-finance-news-7"></a>
### [国务院常务会议研究深化资本市场投融资改革](https://news.rthk.hk/rthk/ch/component/k2/1879500-20261127.htm) ⭐️ 7.0/10

国务院常务会议今日研究持续深化资本市场投融资综合改革，监管部门表示将全力推动中长期资金入市政策取得更多成效，并严格规范控股股东、实控人减持、执行退市制度。报道未披露具体新措施、量化目标或实施时间表。

rss · RTHK Finance · 11月27日 07:53

**「背景」** 中长期资金入市指引导期限较长、追求稳定回报的资金进入股市，目的是形成“长钱长投”的市场机制。

**标签**: `#China capital markets`, `#regulatory policy`, `#long-term funds`, `#IPO regulation`, `#State Council`

---

<a id="item-finance-news-8"></a>
### [国务院常务会议释放稳市场信号，A 股午后大涨，创业板指升 11.61%](https://news.rthk.hk/rthk/ch/component/k2/1879499-20261127.htm) ⭐️ 7.0/10

国务院常务会议释放稳定市场信号后，内地股市午后抽升，上证综合指数收报 3606 点、升 3.73%，创业板指升 11.61%，科创 50 指数升 15.07%。

rss · RTHK Finance · 11月27日 07:39

**「背景」** 11 月 27 日召开的国务院常务会议研究持续深化资本市场投融资综合改革，新华社解读称会议释放了明确的稳市信号。此前沪指、深证成指和创业板指均已连跌两周，本周累计分别回升逾 2%、5.4%和 10.4%。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gov.cn/zhengce/202611/content_7087453.htm">国务院常务会议解读 | 国常会关于资本市场部署释放五大鲜明信号_政策...</a></li>
<li><a href="https://www.xinhuanet.com/20261127/ef625930eb634a159637130d54351b94/c.html">国务院常务会议解读丨国常会新部署释放明确稳市信号-新华网</a></li>

</ul>
</details>

**标签**: `#China stock market`, `#policy signal`, `#ChiNext`, `#STAR Market`, `#semiconductors`

---

<a id="item-finance-news-9"></a>
### [央行发布大额存单新规 个人起购门槛降至 10 万元](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

中国人民银行 11 月 27 日公布《大额存单管理办法》，将个人投资人认购起点从 20 万元下调至不低于 10 万元，机构投资人从 1000 万元下调至不低于 500 万元，新规自 2027 年 3 月 21 日起施行。同日公布的《人民币存贷款利率管理规定》也于同日施行，要求金融机构自主确定存贷款利率，不得通过高息揽储等不正当手段吸收存款。

telegram · zaihuapd · 11月27日 11:36

**「背景」** 现行门槛来自 2015 年《大额存单管理暂行办法》：个人 20 万元、机构 1000 万元；新办法将同时废止该暂行办法和 2016 年第 13 号公告。大额存单是银行向个人和机构发行的大额存款凭证，门槛即为单笔认购的最低金额。

**「影响」** 门槛减半直接扩大了潜在买家范围：此前存款在 10 万至 20 万元之间的个人达不到 20 万元起点、无法认购大额存单，2027 年 3 月 21 日新规生效后这类储户将进入可选范围；但同日发布的利率规定禁止银行以高息揽储等不正当手段吸收存款，实际能拿到多少利率仍由银行自主定价决定。

**标签**: `#PBOC regulation`, `#large-denomination CDs`, `#deposit rates`, `#banking sector`, `#China financial policy`

---