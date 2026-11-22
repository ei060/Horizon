---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 69 条内容中筛选出 9 条重要资讯。

---

**科技新闻**
1. [Lean 验证黎曼猜想的声明引发检查器可靠性争论](#item-tech-news-1) ⭐️ 8.0/10
2. [微软预览 USB4 RDMA 多 PC 合跑本地大模型](#item-tech-news-2) ⭐️ 8.0/10
3. [浙大在“天目 2 号”芯片上真机实现 QRAM 原型](#item-tech-news-3) ⭐️ 8.0/10
4. [GnuPG 公告列表披露 GPGME 漏洞，RCE 影响存争议](#item-tech-news-4) ⭐️ 7.0/10
5. [Dumpleton 发布 AI 辅助开发的 Rust ASGI/WSGI 服务器 Muru](#item-tech-news-5) ⭐️ 7.0/10
6. [OpenRouter 称 MiniMax 模型提示词可能被第三方读取](#item-tech-news-6) ⭐️ 7.0/10

**科技博客**
1. [写好代码的关键是避免灾难性错误](#item-tech-blog-1) ⭐️ 6.0/10
2. [Dettato：开源多乐器音频转 MIDI 工具](#item-tech-blog-2) ⭐️ 4.0/10
3. [群晖 DSM 两个严重漏洞及修复现状](#item-tech-blog-3) ⭐️ 4.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Lean 验证黎曼猜想的声明引发检查器可靠性争论](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 8.0/10

Lean 社区博客发布文章，声称用 Lean 对黎曼猜想完成了形式化验证；但现有材料未提供可供独立复核的证明脚本、Lean 版本或检查结果，因此这仍是待确认的声明，而非已确立的数学结论。讨论的焦点随之转向证明是否可能利用检查器缺陷，以及 AI 工具和人类专家在形式化过程中各自起了什么作用。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**「背景」** 黎曼猜想是 1859 年提出、关于 ζ 函数非平凡零点是否全部位于临界线上的未决问题；此次引发讨论的是 Levent Alpöge 在 2026 年 11 月 20 日宣布与 Claude 一同找到证明，并以 Lean 代码发布，相关报道同时强调该声明尚待专家核验。形式化验证的关键在于：导出的原始证明要由 Lean 官方内核以及 con-leche、con-ron 等多个独立检查器复核，Lean 社区博客称该证明已通过这些检查器；但检查器接受代码并不等同于数学界已确认证明内容。

**「影响」** 对形式化验证研究者和潜在引用者来说，关键动作是把该证明放到多个独立内核中重放并做人工审查；在证明细节公开前，不宜将其作为黎曼猜想的既定状态引用，也不宜据此判断 Lean 或 AI 辅助证明的可靠性。

**「社区讨论」** 评论者对检查器的独立性存在分歧：有人认为不同语言、不同内核且带自洽性证明的多个实现，使同时骗过所有检查器的概率极低；也有人举出此前 Collatz 假反例曾通过某个检查器，提醒不能把“独立检查器”当成绝对保证。另有评论强调人类合作者 Levent 的作用，并讨论 Claude 在形式化大量数学内容中的参与。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.clarin.com/us-news/who-is-levent-alpoge-the-anthropic-mathematician-who-claims-solved-the-riemann-hypothesis-with-claude_0_2WdGvYKBVM.html">Who is Levent Alpöge? The Anthropic mathematician who claims he...</a></li>
<li><a href="https://www.nacionale.com/en/articles/has-riemann-hypothesis-been-proved-levent-alpoge-claude-anthropic-claim-lean">Riemann hypothesis proof claimed with Claude , unverified</a></li>
<li><a href="https://www.youtube.com/watch?v=wM6-mBKzmVQ">250,000 pages? Three misunderstandings about the claimed Riemann ...</a></li>
<li><a href="https://leanprover-community.github.io/blog/posts/riemann-hypothesis/">Lean verification of the Riemann Hypothesis | Lean community blog</a></li>

</ul>
</details>

**标签**: `#formal verification`, `#Lean`, `#Riemann Hypothesis`, `#mathematics`, `#AI-assisted proof`

---

<a id="item-tech-news-2"></a>
### [微软预览 USB4 RDMA 多 PC 合跑本地大模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

微软发布 Windows 的 RDMA over USB4 开发者预览，让多台 PC 通过普通 USB4 连接共享内存与 GPU 算力，共同运行同一个本地 AI 大模型，无需专用网卡或交换机。演示使用三台搭载 AMD Ryzen AI Max+ 395 的 PC，以 4-bit 量化运行 Qwen3-235B-A22B，速度约 18.5 token/s。该功能将通过 Windows Insider 推送，目前仍是开发者预览，并依赖特定硬件与 USB4 连接。

telegram · zaihuapd · 11月21日 06:13

**「背景」** RDMA（远程直接内存访问）让一台计算机绕过对方 CPU 和常规网络协议栈，直接读写另一台设备的内存，从而降低多机协作时的通信开销。微软此次推出的正是面向 Windows 的 RDMA over USB4 开发者预览，按计划通过 Windows Insider 推送，而类似的多机互联此前通常需要专用网卡和交换机。

**「影响」** 对拥有多台 USB4 设备的本地 AI 用户，这一预览提供了不依赖专用网络设备即可汇总多台 PC 算力与内存的路径；但评估者需使用 Windows Insider 构建和兼容的 USB4 硬件，现阶段不宜将其视为生产环境能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1110636/">Microsoft представила решение на базе USB 4 и RDMA для... / Хабр</a></li>
<li><a href="https://www.goha.ru/microsoft-dobavila-v-windows-11-tehnologiyu-rdma-po-usb4-dlya-obedineniya-neskolkih-pk-v-edinyj-lokalnyj-ii-klaster-lWoPRN">Microsoft добавила в Windows 11 технологию RDMA по USB 4 для...</a></li>

</ul>
</details>

**标签**: `#RDMA`, `#USB4`, `#Windows`, `#local AI`, `#distributed inference`

---

<a id="item-tech-news-3"></a>
### [浙大在“天目 2 号”芯片上真机实现 QRAM 原型](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 8.0/10

浙江大学团队称，已在自主制备的超导量子芯片“天目 2 号”上首次于真机实现量子随机存储器（QRAM），成果发表于《自然·物理》。该原型能调取 4 位和 8 位数据，准确率分别为 80.9%和 60.4%；团队表示，其线路深度较未优化方案降低 30%以上，并首次验证该架构具备局部抗噪特性。团队下一步将推进 QRAM 的规模化研究。

telegram · zaihuapd · 11月21日 08:31

**「背景」** QRAM（量子随机存储器）是量子计算中长期停留在理论方案层面的部件，其设想是以量子叠加态寻址存储单元，使量子算法能高效读取大规模数据，此前尚无在真实硬件上运行的实例。《自然·物理》刊发的评论文章将该工作描述为基于超导量子处理器的 QRAM 原理性验证演示。此次实验所用的「天目 2 号」是由浙江大学超导量子计算团队与杭州逻辑比特科技联合研制的 100 比特超导量子芯片。

**「短期影响」** 对量子算法开发者而言，短期内这仍是架构验证，尚不能当作可用的高速量子内存：4 位和 8 位数据调取的准确率分别只有 80.9% 和 60.4%，依赖高保真 QRAM 的算法仍需等待规模扩大与准确率提升。更直接的工程参考是，该团队在超导芯片上验证了 bucket-brigade QRAM 架构及其局部抗噪特性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/en/item/Tianmu-2/4929794">Tianmu-2_Baiduwiki - 百度百科</a></li>
<li><a href="https://www.nature.com/articles/s41567-026-03273-9">Quantum random access memory put to the test | Nature Physics</a></li>
<li><a href="https://producteast.com/china-demonstrates-the-worlds-first-quantum-random-access-memory-advancing-practical-quantum-computing/">China Demonstrates the World &#x27;s First Quantum... - Product East</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#quantum memory`, `#research`

---

<a id="item-tech-news-4"></a>
### [GnuPG 公告列表披露 GPGME 漏洞，RCE 影响存争议](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 7.0/10

GnuPG 公告列表出现一项与 GPGME/GnuPG 相关的漏洞披露，讨论焦点是它是否真的构成远程代码执行（RCE）：有评论者认为这只是双重释放（double-free）缺陷，而非完整的 RCE 利用链。评论区称，使用 2.3.0 之前 GPGME 版本的软件无论动态链接、DLL 还是静态链接都可能受影响，并点名 Gpg4win、GnuPG Desktop、部分邮件客户端和 XMPP 客户端、Samba 与 Flatpak 等下游项目。另有评论称该问题五年前已被 Red Hat 修复但上游遗漏，且 GitLab 因签名提交路径的风险给出了 Omnibus 相关补丁；这些版本、修复与影响说法均来自社区讨论，仍需上游公告正文确认。

hackernews · gdgghhhhh · 11月21日 08:32 · [社区讨论](https://news.ycombinator.com/item?id=50587208)

**「背景：GPGME 是什么、影响面从何而来」** GPGME 是 GnuPG 提供给他方程序调用的库接口，邮件客户端、Gpg4win、Samba 等通过它调用加解密和签名功能；因此同一处库缺陷会随共享库、Windows DLL 或静态链接方式扩散到大量下游软件，而不是只停留在 GnuPG 命令行工具内。据 The Hacker News 报道，该漏洞编号为 CVE-2026-129975，影响 2.3.0 之前的 GPGME 版本，而 2.3.0 从未公开发布，修复因此需要下游项目自行回溯补丁。

**「影响与处置」** CVE-2026-129975 影响所有使用 2.3.0 之前版本 GPGME 的软件，无论该库以共享库、Windows DLL 还是静态链接方式集成；依赖它的邮件客户端、Samba 等下游程序需要升级到 2.3.0 或厂商补丁版本，静态链接的程序还需重新编译。

**「社区讨论」** 最实质的分歧是漏洞定性：一方认为报告把双重释放夸大为 RCE，另一方则强调 GPGME 2.3.0 之前版本的下游暴露面，尤其是 GitLab 的签名提交路径。还有评论者用“Red Hat 五年前已修复、上游遗漏”来质疑上游维护流程，并提及披露因 Ruby2Shell 漏洞提前到 2026-11-20。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html">GnuPG Warns Critical GPGME Flaw Could Expose App Data via...</a></li>
<li><a href="https://www.phoronix.com/news/GnuPG-GPGME-Critical">GnuPG&#x27;s GPGME Affected By Critical Security Bug In Turn... - Phoronix</a></li>
<li><a href="https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html">GnuPG Warns Critical GPGME Flaw Could Expose App Data via...</a></li>

</ul>
</details>

**标签**: `#security vulnerability`, `#GPGME`, `#GnuPG`, `#double-free`, `#coordinated disclosure`

---

<a id="item-tech-news-5"></a>
### [Dumpleton 发布 AI 辅助开发的 Rust ASGI/WSGI 服务器 Muru](https://simonwillison.net/2026/Nov/21/muru/) ⭐️ 7.0/10

Graham Dumpleton 公开了 Muru 项目：一个用 Rust 编写、面向 ASGI 与 WSGI Python 应用的服务器，目标是同时服务开发和生产环境。他是 mod\_wsgi 的创建者；Muru 以 AI 辅助方式开发，其公开开发记录从 11 月 4 日持续到 11 月 21 日，涵盖 worker 内部结构、一次导入多次 fork、开发环境 HTTPS、WSGI/ASGI 共存、无需服务网格的灰度发布、容器与 Kubernetes 集成、缩容到零以及带追踪的工具栏等设计。Dumpleton 称 AI 承担了大量表面工作，但判断哪些还不够好仍由他负责，20 年 mod\_wsgi 经验对此有帮助。现有材料未给出性能基准、版本号或生产采用数据，因此尚不能确认其生产就绪程度。

rss · Simon Willison · 11月21日 23:56

**「背景」** Graham Dumpleton 在 20 年前创建了 mod\_wsgi，这是一个用于在 Apache 下托管 Python WSGI 应用的模块，他也因此长期思考生产环境中运行 Python Web 应用的方式。Muru 延续了这一脉络，但同时面向传统的 WSGI 与较新的异步 ASGI 两类接口。

**「对现有 WSGI 部署的影响」** 对于仍在维护 WSGI 应用、又需要加入 WebSocket 的团队，Muru 支持在同一应用内混合运行 WSGI 与 ASGI，因此不必仅为这一需求就把应用改写成纯 ASGI。其 GitHub 项目描述还列出了零停机发布、流量管理和能感知 Python 进程的管理能力。不过，现有材料没有提供基准测试或生产采用数据；团队在评估时，应先在预发布环境中验证性能、兼容性和运维成熟度，再考虑迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/GrahamDumpleton/muru">GitHub - GrahamDumpleton/muru: Routing edge, control plane ...</a></li>
<li><a href="https://grahamdumpleton.me/posts/2026/11/muru-wsgi-and-asgi-together/">Muru: WSGI and ASGI together - Graham Dumpleton</a></li>

</ul>
</details>

**标签**: `#Python`, `#ASGI/WSGI`, `#Rust`, `#Web servers`, `#mod\_wsgi`

---

<a id="item-tech-news-6"></a>
### [OpenRouter 称 MiniMax 模型提示词可能被第三方读取](https://news.ycombinator.com/item?id=50585962) ⭐️ 7.0/10

OpenRouter 通过邮件通知用户，发往 MiniMax 模型的请求内容可能已被第三方读取；OpenRouter 已下架相关端点的“零数据保留”标签，并建议涉及敏感凭证的用户更换 API Key 和密码。安全研究者在 2026 年 7 月至 10 月向这些模型发送含测试 URL 的提示词，称第三方在 40 至 130 小时后访问了这些 URL。OpenRouter 将问题指向 MiniMax 及其转发方 AtlasCloud、Novita、StreamLake；其官网尚未发布相关说明，上述细节来自二手转述，尚待独立核实。

telegram · zaihuapd · 11月21日 06:53

**「背景」** OpenRouter 文档将“零数据保留（ZDR）”定义为：处理完成后不常规存储提示词或响应，页面所列的 CSAM 例外除外；其隐私设置可让用户只将请求路由到声明 ZDR 的端点。因此，移除相关端点的 ZDR 标签会直接影响依赖该设置限制数据留存与路由选择的用户。

**「影响」** 对曾通过受影响端点发送含密钥、密码或其他敏感信息提示词的用户，OpenRouter 的建议是轮换相关 API Key 和密码；在恢复可信的数据保留说明前，相关端点不再带有“零数据保留”标签，依赖该承诺处理敏感数据的工作流需要调整。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/docs/guides/features/zdr">Zero Data Retention - How OpenRouter gives you control over your...</a></li>

</ul>
</details>

**标签**: `#ai-security`, `#data-privacy`, `#openrouter`, `#minimax`, `#api-security`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [写好代码的关键是避免灾难性错误](https://seangoedecke.com/to-code-well-avoid-blunders/) ⭐️ 6.0/10

rss · Sean Goedecke · 11月22日 00:00

**「背景」** Sean Goedecke 认为，许多工程师把编程当成寻找绝妙洞察，但在大型商业代码库里，真正决定代码质量的是别犯灾难性错误。

**「方案」** 他用国际象棋和网球作类比：不送子、稳定回球就足以赢过大多数对手；编程没有篮球那种 99 比 1 的缓冲，一次失误就可能让优雅的代码库变得摇摇欲坠。作者列举的失误包括另起并行系统、为关键数据制造第二个真相源、把安全的同步操作改成脆弱的异步、增加隐蔽故障点、复杂化关键接口，归根结底是破坏一致性或引入不必要需求。轻微不一致也会破坏信任，后来者必须到处寻找意外；多余需求则因为后来者缺少上下文而难以删除，并会与每个新功能发生组合式交互，这正是大型代码库难维护的原因。因此他主张先找任务最自然地融入现有代码库的位置，再把需求裁到最小；若开始想用巧妙模式，应把它视为可能偏离重点的警告。作者限定讨论对象是大型商业代码库和大团队，但称这些建议同样适用于手写代码或驱动 AI 代理，并认为当前代理在一致性上接近人类，却明显更不擅长避免多余需求。

**「启示」** 换言之，优秀编程未必需要聪明，反而可能被聪明拖累；持续维护一致性、拒绝非必要需求，才是避免失误并保持代码库长期可维护的核心。

**标签**: `#software engineering`, `#code quality`, `#technical debt`, `#consistency`, `#requirements`

---

<a id="item-tech-blog-2"></a>
### [Dettato：开源多乐器音频转 MIDI 工具](https://www.appinn.com/dettato/) ⭐️ 4.0/10

rss · Appinn · 11月21日 06:25

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图产生偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/dettato/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;MP3/WAV 保存的是声音波形，MIDI 记录的是音高、时值和力度等演奏指令；Dettato 的目标是把前者自动转成多轨 MIDI，让普通电脑也能完成音乐转录。

**「方案」** 作者介绍，这个 KobiMusic 开源工具用一条 \`pip install\` 命令安装，运行 \`dettato song.mp3 -o out/\` 后会输出 \`song.mid\`（每个乐器一条音轨，另有鼓组轨）和记录轨道、音符数量的 \`song.json\`，首次运行会从 Hugging Face 下载模型。它由四个几十 MB 的模型串联：15.3M 参数模型标注 88 个音高位置的起止与音高（每个音高两个声部），4.9M 证据模型删错音、修正起止并补漏，2.9M 分组模型把音符分配到乐器轨并命名，5.0M 鼓模型识别 General MIDI 鼓键、鼓组和管弦打击乐。开发者称，笔记本 CPU 转录 15 秒音频约需 87 秒（含模型加载），RTX 5060 8GB 转录 4 分钟歌曲约需 15 秒、显存峰值低于 4GB；运行需 Python 3.10+ 和 PyTorch 2.2+，M 系列 Mac 可指定 CPU，但耗时取决于机器与录音长度。作者没有解释核心算法、精度或失败模式，文中“工作原理”仅有一张图，相关性能数据应视为开发者提供的初步参考。

**「启示」** 对音乐爱好者来说，Dettato 的吸引力在于开源、模型小且 CPU 可跑，GPU 则能显著缩短等待；但现有文章更像项目说明，转录精度和适用边界仍需实际测试。

**标签**: `#音频转MIDI`, `#Dettato`, `#音乐转录`, `#开源模型`, `#CPU/GPU性能`

---

<a id="item-tech-blog-3"></a>
### [群晖 DSM 两个严重漏洞及修复现状](https://www.appinn.com/synology-dsm-critical-vulnerabilities-2026-11/) ⭐️ 4.0/10

rss · Appinn · 11月21日 03:07

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/synology-dsm-critical-vulnerabilities-2026-11/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;2026 年 11 月 19 日，群晖连续发布两份安全公告，涉及 DSM 与 BeeStation OS 的 OAuth API 和 NGINX HTTP/2，其中前者 CVSS 评分 9.8、后者 8.1。对暴露在公网的 NAS 管理员而言，风险在于攻击者可能无需账户或用户交互，就能远程读写文件、造成拒绝服务，甚至在特定条件下执行代码。

**「方案」** 文章梳理称，OAuth API 漏洞 CVE-2026-120382 出在命令参数分隔符处理上，可被未认证的远程攻击者用于任意文件读写或拒绝服务，并可能影响依赖 OAuth 的第三方应用，例如 Amazon Echo/Alexa 连接 Audio Station；临时缓解措施是停用 OAuth Service。NGINX 漏洞 CVE-2026-123007 影响启用 HTTP/2 的 NGINX，可能让 Web 服务崩溃，并在特定条件下远程执行代码，缓解方式是关闭 HTTP/2。受影响版本包括 DSM 7.4、7.3、7.2.2、7.2.1、7.1 及 BeeStation OS 1.5；文章列出的补丁表中，DSM 7.4.1-90080 Update 2 和 7.3.2-86009 Update 6 标为已发布，其余仍处修复中。群晖称公告发布时尚未观察到实际利用，并建议避免公网暴露、改用 Tailscale 等组网方式，同时检查 Docker 或第三方套件中的 NGINX；但文章对补丁状态表述矛盾：开头称 11 月 21 日已发布修复，后文又说 11 月 20 日核对时公告仍为 Ongoing、计划日期未上线，读者需以官方更新页为准。

**「启示」** 作者的核心判断是，NAS 漏洞并非群晖独有，公开披露与修复反而说明仍有人在维护，不能把“没爆漏洞”当作安全；更稳妥的做法是尽量减少公网暴露，并做好异地备份。

**标签**: `#Synology DSM`, `#OAuth API 漏洞`, `#NGINX HTTP/2`, `#安全公告`, `#NAS 安全`

---