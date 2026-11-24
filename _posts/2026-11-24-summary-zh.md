---
layout: default
title: "Horizon Summary: 2026-11-24 (ZH)"
date: 2026-11-24
lang: zh
---

> 从 178 条内容中筛选出 23 条重要资讯。

---

**科技新闻**
1. [Ladybird 浏览器进入 Alpha，可在 macOS 与 Linux 安装](#item-tech-news-1) ⭐️ 8.0/10
2. [Z.ai 发布 GLM-5.4：首个循环 Transformer 编程模型](#item-tech-news-2) ⭐️ 8.0/10
3. [CrowdStrike 拟以 440 亿美元收购 Zscaler](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic 称 Claude 发现 VP≠VNP 并发布 Lean 4 证明](#item-tech-news-4) ⭐️ 8.0/10
5. [报道称 Nvidia 董事会重新任命黄仁勋为 CEO](#item-tech-news-5) ⭐️ 7.0/10
6. [Arm 要求第三方文档站于 2026 年 12 月 4 日停运](#item-tech-news-6) ⭐️ 7.0/10
7. [亚马逊据报 75 亿美元收购 Decart 的 AI 优化技术与研究团队](#item-tech-news-7) ⭐️ 7.0/10
8. [弗吉尼亚与俄勒冈起诉 SpaceX，要求叫停 Grok 有害图像生成](#item-tech-news-8) ⭐️ 7.0/10
9. [Codex2api 疑似遭投毒：3.1.11 移除鉴权并外泄 Actions 密钥](#item-tech-news-9) ⭐️ 7.0/10
10. [Meta AI 负责人称超级智能将至并警告控制风险](#item-tech-news-10) ⭐️ 7.0/10
11. [4.5 万家企业联名致信欧盟，要求调查苹果 iPhone 浏览器限制](#item-tech-news-11) ⭐️ 7.0/10
12. [黄循财：新加坡不会成为规避芯片管制通道](#item-tech-news-12) ⭐️ 7.0/10

**科技博客**
1. [ERNIE 5.5 Flash 的 vLLM Day-0 插件支持](#item-tech-blog-1) ⭐️ 6.0/10
2. [从 Megaspeed 案看算力如何绕过芯片出口管制](#item-tech-blog-2) ⭐️ 5.0/10
3. [上传图片即可入侵服务器：Upload2Shell 漏洞通报](#item-tech-blog-3) ⭐️ 4.0/10
4. [WinGet 新增 MCP 支持，AI 可代装 Windows 软件](#item-tech-blog-4) ⭐️ 4.0/10

**财经新闻**
1. [台股收涨 8.99% 台积电涨停](#item-finance-news-1) ⭐️ 8.0/10
2. [AI 抛售令 DeepSeek 等中国 AI 公司上市计划蒙上阴影](#item-finance-news-2) ⭐️ 8.0/10
3. [纽约联储威廉姆斯：通胀回落到 2%仍需努力，加息可能“随时间推移”推进](#item-finance-news-3) ⭐️ 7.0/10
4. [英伟达市值增加近 1 万亿美元，带动科技股上涨](#item-finance-news-4) ⭐️ 7.0/10
5. [Capita 股价据报道暴跌 70%，首席执行官因公务员养老金支付延误辞职](#item-finance-news-5) ⭐️ 7.0/10
6. [证监会主席黄天祐：首只无纸化新股上市，为 T+1 交收等改革铺路](#item-finance-news-6) ⭐️ 7.0/10
7. [上海地铁 12 月 1 日起调整票价，21 年来首次](#item-finance-news-7) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Ladybird 浏览器进入 Alpha，可在 macOS 与 Linux 安装](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird 项目发布了首个 Alpha 版本，用户现在可在 macOS 和 Linux 上直接安装，无需自行编译。该项目从零实现 HTML 解析、CSS 引擎、布局、JavaScript 和 WebAssembly，仅复用 HarfBuzz、Skia、FFmpeg 与 SQLite 等外部组件。实测中多数网站可正常显示，并能运行基于 WebAssembly 的 ffmpeg 图像处理工具和 Pyodide REPL，但 Datasette Lite 因缺少 navigator.serviceWorker.startMessages 而报错。官方明确这是 Alpha：部分网站尚不能工作、浏览器偶尔会崩溃，并支持在浏览器内报告故障站点和崩溃报告。

hackernews · janvdberg · 11月23日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50614249)

**「背景」** Ladybird 是 SerenityOS 的后继项目，核心的 HTML 解析、CSS、布局、JavaScript 和 WebAssembly 引擎均为自研，只借用 HarfBuzz、Skia、FFmpeg、SQLite 等少数基础库。此前它主要供开发者自行编译试用；2026 年项目又用 AI 编程代理把 LibJS 的部分 C++ 代码移植为约 2.5 万行 Rust，并在 10 月完成布局线程化、新 JavaScript JIT 和基于 Cranelift 的 WebAssembly 引擎等改动，为这次 alpha 打下基础。

**「影响」** 对 Web 开发者来说，这个 Alpha 提供了一个新的兼容性测试目标，但 Service Worker 等能力缺口意味着依赖这些 API 的应用仍可能失败；普通用户则应按官方说明回报崩溃和站点问题，而不是立即把它当作日常主力浏览器。

**「社区讨论」** 多位评论者称 Ladybird 对常见网站乃至 Proxmox 的 NoVNC 等较复杂页面渲染良好，有人甚至觉得 NoVNC 比 Firefox 更流畅，但也有人指出页面滚动略显卡顿。另有评论希望项目未来认真处理浏览器指纹识别问题，并对放弃部分自研组件、转向 SQLite 和 Skia 等成熟库表达了复杂感受。

**标签**: `#Ladybird`, `#browser engines`, `#open-source software`, `#web standards`, `#alpha release`

---

<a id="item-tech-news-2"></a>
### [Z.ai 发布 GLM-5.4：首个循环 Transformer 编程模型](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

Z.ai 发布 GLM-5.4，并称这是其首个采用循环 Transformer 架构的模型，主打通用编程能力。据 Z.ai 描述，该架构让一组共享权重的层在每次前向传播中运行多轮、持续细化隐藏状态，从而在不增加参数量的情况下加深网络。GLM-5.4 目前尚未开放权重，也无法通过普通 API 套餐访问，用户需订阅 Coding Plan；其 API 密钥可在 https://api.z.ai/api/v1 的 OpenAI 兼容 Responses API 上使用该模型。Simon Willison 为此发布了 llm-glm 插件，但现有 llm-zai 插件尚不支持新模型，他表示待后者跟上后会停用自己的插件。

hackernews · foohis · 11月23日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50609685)

**「背景」** 标准 Transformer 在一次前向传播中每层只计算一次；循环 Transformer 让一组共享权重的层重复执行，在不增加参数量的情况下获得更深的有效网络。GLM-5.4 是 Z.ai 首个采用该架构的旗舰模型，其核心的 28 层模块据报每个 token 执行两遍；11 月 20 日，Thinking Machines Lab 的 Inkling 2 Mini 也采用了让中间层重复运行的循环设计。

**「开发者接入影响」** 对开发者而言，短期内要试用 GLM-5.4 只能订阅 Z.ai 的 Coding Plan：该模型目前不在常规 API 套餐和 OpenRouter 上，也未放出开放权重；Coding Plan 签发的 API key 与常规套餐一样走 https://api.z.ai/api/v1 的 OpenAI 兼容 Responses 接口。现有社区插件 llm-zai 尚未支持新模型，需要改用专门适配的插件才能调用。

**「社区讨论」** 有评论者称赞 Zhipu 公开了较多架构技术细节，并认为循环 Transformer 是明显的发展方向，但仍有问题待解决；另一名用户则抱怨部分中国模型的“马拉松式思考”在简单任务上也会反复自我怀疑、显著拉长完成时间，并推测这与基准测试策略有关。还有评论从推理时 HBM 到芯片的内存带宽瓶颈解释了循环 Transformer 的优化动机。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wccftech.com/z-ai-debuts-glm-5-4-with-a-novel-looped-transformer-architecture-skipping-ai-benchmarks-entirely/">Z.ai Debuts GLM - 5 . 4 With a Novel Looped Transformer Architecture...</a></li>
<li><a href="https://docs.z.ai/guides/llm/glm-5.4">GLM - 5 . 4 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>

</ul>
</details>

**标签**: `#LLMs`, `#GLM-5.4`, `#looped transformers`, `#Zhipu AI`, `#coding models`

---

<a id="item-tech-news-3"></a>
### [CrowdStrike 拟以 440 亿美元收购 Zscaler](https://techcrunch.com/2026/11/23/crowdstrike-to-acquire-zscaler-for-44-billion/) ⭐️ 8.0/10

CrowdStrike 计划以 440 亿美元收购 Zscaler，后者为大型企业提供零信任安全产品。CrowdStrike 表示，这笔交易将使其客户更好地使用 AI 代理。该交易目前是一项已宣布的收购计划，监管审批和完成时间等细节尚不清楚。

rss · TechCrunch · 11月23日 16:20

**「背景」** 零信任产品通常不默认信任企业内网连接，而是对每次访问逐次验证；Zscaler 向大型企业提供这类云安全产品，其公告称约有 8,000 家客户。两家公司董事会已一致批准这项全股票交易，企业价值约 439 亿美元，按 CrowdStrike 2026 年 11 月 20 日收盘价计算；路透社称这是有记录以来最大的网络安全收购。

**「客户面临的产品连续性不确定性」** 对同时部署 CrowdStrike 端点防护与 Zscaler 零信任产品的企业来说，最直接的后果是供应商整合带来的产品路线和合同续约不确定性。报道仅给出 440 亿美元的交易金额以及“让客户更好使用 AI 代理”的理由，未披露交割时间表、监管审批条件或具体产品整合方案，因此客户目前无法判断现有 Zscaler 部署与采购合同能否延续。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.crowdstrike.com/en-us/press-releases/crowdstrike-to-acquire-zscaler-bringing-network-security-and-zero-trust-to-the-falcon-platform/">CrowdStrike to Acquire Zscaler , Bringing Network Security and ...</a></li>
<li><a href="https://www.zscaler.com/press/crowdstrike-acquire-zscaler-bringing-network-security-and-zero-trust-falcon-platform">CrowdStrike to Acquire Zscaler for Zero Trust</a></li>
<li><a href="https://www.reuters.com/legal/transactional/crowdstrike-buy-zscaler-439-billion-2026-11-23/">CrowdStrike snaps up Zscaler in $44 billion deal as cyber ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#acquisitions`, `#zero-trust`, `#enterprise security`, `#AI agents`

---

<a id="item-tech-news-4"></a>
### [Anthropic 称 Claude 发现 VP≠VNP 并发布 Lean 4 证明](https://github.com/anthropics/formal-math/blob/main/vp-vnp/README.md) ⭐️ 8.0/10

Anthropic 于 11 月 24 日公开论文《VP ≠ VNP over every field》及 Lean 4 形式化证明，称结果由内部研究用 Claude 模型发现，论文和代码均由 AI 撰写。论文给出哈密顿圈多项式的超多项式算术电路下界，据此主张 VP 是 VNP 的真子类；若成立，这将解决 Valiant 1979 年的代数复杂度猜想，但仅针对算术电路，不涉及 P 与 NP。仓库称已通过三条标准公理审计和独立内核 nanoda 复核，除预留文件外没有 sorry。不过尚无人类数学家通读，Lean 无法确认形式化陈述与所声称命题一致，附录 Q 也列出出入，结论仍待独立审阅。

telegram · zaihuapd · 11月24日 06:02

**「背景：VP 与 VNP 是什么」** VP 与 VNP 是 Valiant 1979 年提出的代数复杂度类，可视为 P 与 NP 在算术电路模型下的对应版本，讨论的是次数受多项式界约束的代数函数能否用多项式规模的算术电路计算。二者是不同的猜想：VP≠VNP 只涉及算术电路，并不直接推出 P≠NP。此次公开的论文也自述尚无人类数学家核查过证明。

**「对领域研究者的直接影响」** 对代数复杂度理论研究者而言，这一结果目前不能作为已确立的定理引用：Lean 内核通过只能说明形式化证明与其写下的形式陈述一致，无法说明该陈述就是「VP≠VNP over every field」。因此独立审阅的实际重点在于核对形式陈述与所声称命题的对应关系，尤其是附录 Q 列出的出入之处；在人类数学家完成这一步之前，任何引用都应标注为未经确认的 AI 生成结果。相关报道也指出，数学家尚未独立验证该结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.alphaxiv.org/abs/2611.vp-vnp-arithmetic-lower-bounds">VP VNP Over Every Field | alphaXiv</a></li>
<li><a href="https://cstheory.stackexchange.com/questions/529/does-vp-neq-vnp-imply-p-neq-np">cc. complexity theory - Does $ VP \neq VNP $ imply $P \neq NP</a></li>
<li>Claude claims to prove VP ≠ VNP in Valiant&#x27;s 47-year-old conjecture</li>

</ul>
</details>

**标签**: `#AI for mathematics`, `#complexity theory`, `#Lean 4`, `#formal verification`, `#Anthropic`

---

<a id="item-tech-news-5"></a>
### [报道称 Nvidia 董事会重新任命黄仁勋为 CEO](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 7.0/10

据 Ars Technica 报道，Nvidia 董事会投票决定重新任命黄仁勋为 CEO 兼董事会主席，立即生效，距他因多起丑闻辞职仅 11 天。报道称，董事会部分依据美国政府在高层级别提供的意见，认定黄仁勋回归“不构成国家安全风险”，尽管他承认的婚外情对象被指为中国从事间谍活动，Nvidia 也被指规避对华出口管制并面临多个政府部门的调查。提供的报道正文被截断，相关说法尚未获得独立确认。

hackernews · jaz · 11月23日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50611576)

**「背景」** 此次复职距黄仁勋离任仅 11 天：据 Nvidia 于 11 月 12 日发布的新闻稿，董事会当时宣布他“即刻起”辞去总裁、首席执行官及董事职务。据 Ars Technica 报道，辞职源于多起丑闻——他承认与一名被美国情报来源视为中国间谍的女性有婚外情，Nvidia 亦被指规避旨在阻止其芯片流入中国的出口管制，多个美国政府部门的调查正在进行中；这些指控尚未获得独立证实。

**「影响」** 董事会给出复职理由是：来自&quot;美国政府高层&quot;的意见保证黄仁勋回归不构成国家安全风险，而并非相关调查已有结论。因此，针对黄仁勋本人及英伟达涉嫌规避对华出口管制的多项跨部门调查仍悬而未决；依赖英伟达对华出货许可的客户与合作伙伴，无法从这一人事决定中判断自身合规环境是否发生变化。Semafor 报道称，特朗普在董事会会议前数小时亲自致电游说黄仁勋回归，这说明此次决定的实际推动力来自政治层面的直接介入，并非董事会的独立治理判断或例行的安全审查程序。

**「社区讨论」** 评论区把“董事会收到美国政府高层意见”视为声明中最关键的一句，并围绕董事会责任、全票反转以及是否存在未公开证据展开争论；有评论者以 Caremark 判例和司法部不会起诉的说法推断董事个人责任可能被削弱，也有人质疑美国在出口管制上对 Nvidia 与盟友企业采取双重标准。另有评论者借 OpenAI 2023 年事件指出，公司的名义治理结构未必等于实际治理结构。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nvidianews.nvidia.com/news/nvidia-board-reinstates-jensen-huang-as-president-ceo-and-board-director">NVIDIA Board Reinstates Jensen Huang as President, CEO and Board ...</a></li>
<li><a href="https://nvidianews.nvidia.com/news/nvidia-announces-ceo-transition">NVIDIA Announces CEO Transition</a></li>
<li><a href="https://www.semafor.com/article/11/23/2026/huang-reinstatement-came-at-trumps-behest">Huang reinstatement came at Trump’s behest | Semafor</a></li>
<li><a href="https://www.nbcnews.com/tech/tech-news/nvidia-reinstates-jensen-huang-rcna610864">Nvidia reinstates Jensen Huang as CEO</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#semiconductors`, `#corporate governance`, `#US policy`, `#national security`

---

<a id="item-tech-news-6"></a>
### [Arm 要求第三方文档站于 2026 年 12 月 4 日停运](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

第三方 Arm 架构文档网站 arm.jonpalmisc.com 将于 2026 年 12 月 4 日停止运营。站点运营者 jonpalmisc 表示，Arm 以该站使用其商标和知识产权为由要求移除内容，他认为在保持站点有用的情况下很难规避这一要求。他正在考虑他人提出的镜像托管、寻求法律意见，以及发布不含 Arm 知识产权的站点源码等方案。此次关站将影响依赖该站查阅 Arm 文档的工程师。

hackernews · tech234a · 11月23日 19:17 · [社区讨论](https://news.ycombinator.com/item?id=50617499)

**「背景」** Arm 官方以自身许可条款发布架构参考手册等文档，而这个站点是开发者自建的第三方版本，将相关文档托管在自己的域名下供查阅。Arm 此次以商标和知识产权为由要求其下线，使站点在保留原有查阅功能的同时很难继续运营。

**「对依赖该站点的工程师的影响」** 该站关闭后，习惯用这一第三方整理版查阅 Arm 架构文档的工程师将失去一个可检索的入口，只能回到 Arm 官方渠道获取同类资料；站点作者 jonpalmisc 表示，在继续维持站点可用性的前提下，很难绕开对方提出的商标与 IP 主张，因此即使有人提出代为镜像托管，同样的主张仍可能适用。评论者 ethin 指出，Arm 发布的机器可读架构规范（MRAS）中部分开源包采用 BSD 式许可，这或许为 ISA 参考部分留下有限的再利用空间，但该说法来自社区讨论，并未经独立核实，也不涵盖异常级别等其余文档。

**「社区讨论」** 评论者质疑 Arm 为何对公开硬件文档的第三方整理站采取行动，有人认为这可能属于合理使用；也有人指出，Arm 的机器可读架构规范（MRAS）中至少开源包似乎采用 BSD 风格许可证，因而对移除依据存疑。另有评论者从商业角度批评，这种做法只会给为 Arm 生态提供价值的用户增加麻烦。

**标签**: `#Arm`, `#technical documentation`, `#intellectual property`, `#hardware engineering`, `#community debate`

---

<a id="item-tech-news-7"></a>
### [亚马逊据报 75 亿美元收购 Decart 的 AI 优化技术与研究团队](https://techcrunch.com/2026/11/23/amazon-snaps-up-decarts-ai-optimization-tech-for-7-5b-as-it-prepares-to-sell-trainium-chips/) ⭐️ 7.0/10

据 TechCrunch 报道，亚马逊将以 75 亿美元收购 Decart 的 AI 优化技术及其研究团队；报道所述交易对象是技术与团队，未提及收购整家公司。报道将这笔交易与亚马逊准备对外销售自研 Trainium 芯片的计划联系在一起。目前公开信息仅有一句概述：75 亿美元为报道数字，交易的具体条款、所涉技术的细节、监管审批与完成时间均未披露。

rss · TechCrunch · 11月23日 17:14

**「背景」** Decart 是一家以色列人工智能公司，主要开发实时世界模型及其配套基础设施；这类生成式系统能够逐帧生成交互式视频和模拟环境，并保持较低延迟。此次交易涉及的研究团队和优化技术，正属于这一实时生成与运行效率方向。

**「对开发者的影响」** 对使用 Decart 优化工具的开发者而言，最直接的后果是这项技术与研究团队将归入亚马逊，并围绕亚马逊自家的 Trainium 芯片展开。来源未说明 Decart 现有工具、授权方式或对其他芯片平台的支持是否会保留；因此依赖其做模型推理优化的团队，在交易完成后需要确认是否还能以同样方式、在同类硬件上继续使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Decart">Decart - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Amazon`, `#Decart`, `#AI optimization`, `#Trainium`, `#acquisitions`

---

<a id="item-tech-news-8"></a>
### [弗吉尼亚与俄勒冈起诉 SpaceX，要求叫停 Grok 有害图像生成](https://arstechnica.com/tech-policy/2026/11/states-sue-spacex-to-stop-grok-from-generating-child-sex-images-revenge-porn/) ⭐️ 7.0/10

11 月 23 日，弗吉尼亚州和俄勒冈州成为首批就 Grok 生成有害图像起诉 SpaceX 的州，指控该模型仍会将真实人物照片——主要是女性和儿童——性化，并产出非自愿亲密图像（NCII）和儿童性虐待材料（CSAM）。SpaceX 于今年 2 月收购 xAI（现称 SpaceXSI）；两州总检察长称，公司此前声称已增加防护并重设政策具有“误导性”，实际却为争夺 AI 市场份额而纵容 Grok 的“spicy mode”性化内容。诉讼旨在阻止 Grok 继续生成此类图像；来源未提供案件编号、具体法律请求或 SpaceX 的回应。

rss · Ars Technica · 11月23日 21:30

**「背景」** Grok 的“spicy mode”是马斯克曾高调宣传的模型功能；推出后，其初始安全防护被指过于宽松，甚至会在未被要求时生成裸体图像，并引发大量非自愿私密影像和儿童性虐待材料争议。2026 年 2 月，SpaceX 收购 xAI（现称 SpaceXSI），因此这起州诉讼把 SpaceX 列为被告。

**「影响」** 这起诉讼把 SpaceXSI 此前“已追加保障措施、重新设计政策”的公开表态直接推到争议中心：两州总检察长称这些说法“具有误导性”，因此该公司对 Grok 图像生成所设防护的说明本身可能成为案件焦点。对使用 Grok 图像功能的用户和集成方而言，涉及真人照片的生成请求正处在州级执法审视之下，相关功能的使用条件与限制存在被收紧的风险。

**标签**: `#AI safety`, `#generative AI`, `#content moderation`, `#AI regulation`, `#Grok`

---

<a id="item-tech-news-9"></a>
### [Codex2api 疑似遭投毒：3.1.11 移除鉴权并外泄 Actions 密钥](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 7.0/10

据事件复盘报告，Codex2api 作者账号被黑后，攻击者绕过 main 分支直接推送 tag，使 Release 构建出带后门的版本；其中 v3.1.11 去掉了鉴权，等于可无密码远程执行命令。同时有 workflow 将仓库的 16 个 Actions secrets 外传，波及同一账号下至少 21 个仓库。该报告将此事描述为疑似供应链投毒，尚未见独立第三方确认。报告建议已安装或更新过 3.1.10–3.1.12 的用户立即停用并退回 3.1.9，同时轮换 GitHub token、SSH key、数据库及 DeepSeek 等相关密钥。

telegram · zaihuapd · 11月23日 11:21

**「背景」** Codex2api 是一个用 Go 与 React/Vite 构建的反向代理和管理系统，用于把一组上游 Codex 账号转换成统一的 OpenAI 兼容 API 服务。此次疑似事件中，攻击者绕开 main 分支、直接推 tag 触发 Release 构建，说明发布流程若只保护主分支，仍可能被标签构建绕过；而 GitHub Actions secrets 被外传，则可能让风险从单个仓库扩散到同账号下的其他仓库。

**「影响」** 已部署或更新过 Codex2api 3.1.10–3.1.12 的用户应立即停用相关实例、回退到 3.1.9，并轮换 GitHub token、SSH key、数据库和 DeepSeek 等所有相关密钥。事件复盘称，v3.1.11 移除了鉴权，等同于无密码远程执行命令；同时有 workflow 外传了仓库的 16 个 Actions secrets，影响同账号下至少 21 个仓库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepwiki.com/james-6-23/codex2api">james-6-23/ codex2api | DeepWiki</a></li>

</ul>
</details>

**标签**: `#supply-chain security`, `#GitHub Actions`, `#security incident`, `#credential rotation`, `#open source`

---

<a id="item-tech-news-10"></a>
### [Meta AI 负责人称超级智能将至并警告控制风险](https://thenextweb.com/news/metas-ai-chief-says-superintelligence-is-arriving-and-control-is-at-risk) ⭐️ 7.0/10

Meta 首席 AI 官、超级智能实验室负责人 Alexandr Wang 在 X 发长文称，超级智能已不再是“未来某天”的议题，并警告人类将难以继续控制可无限自我改进或比自己聪明 1000 倍的系统。他引用数学家 Levent Alpöge 借助 Anthropic 的 Claude 完成、并于周六经 Lean 与 Mathlib 社区机器校验的黎曼猜想证明，认为 AI 与顶尖人类只剩具体知识、工程整合和实验三方面的差距。该证明目前没有人类可读版本，报道也未提供独立确认或技术细节，因此上述证明与“超级智能将至”的判断仍应视为未经独立验证的说法；Wang 呼吁紧急投入安全、对齐与防护研究。

telegram · zaihuapd · 11月23日 12:49

**「背景」** Lean 是交互式定理证明器，Mathlib 是其社区维护的数学库；所谓“经 Lean 与 Mathlib 校验”，是指证明被拆成形式化步骤并由机器按规则检查。公开资料显示，Levent Alpöge 是 Anthropic 的技术团队成员；而这次声称的黎曼猜想证明目前没有人类可读版本，因此机器校验本身并不等同于同行评审或独立复现。

**「影响」** 若该证明确如所述通过 Lean 与 Mathlib 校验，研究界仍需人类可读的说明和独立复核才能评估其数学意义；在此之前，不宜把它当作已确立的黎曼猜想证明。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.clarin.com/us-news/who-is-levent-alpoge-the-anthropic-mathematician-who-claims-solved-the-riemann-hypothesis-with-claude_0_2WdGvYKBVM.html">Who is Levent Alpöge? The Anthropic mathematician who claims ......</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#superintelligence`, `#AI for mathematics`, `#formal verification`, `#Meta AI`

---

<a id="item-tech-news-11"></a>
### [4.5 万家企业联名致信欧盟，要求调查苹果 iPhone 浏览器限制](https://appleinsider.com/articles/26/11/23/eu-urges-to-challenge-apples-grip-on-iphone-browsers?utm_source=rss) ⭐️ 7.0/10

包括 Mozilla 和 Shopify 在内的企业及组织联名致信欧盟委员会，要求就苹果对 iPhone 浏览器的限制启动调查程序；联署方称合计代表约 4.5 万至 5.5 万家欧盟企业组织，联署征集持续到 2026 年 12 月 3 日。信方称，苹果虽已按《数字市场法》允许欧盟竞品浏览器使用自有引擎，但技术与法律要求使厂商无法把现有欧盟用户迁出 WebKit，企业触达用户仍高度依赖 App Store。联名方估算，若半数原生 iOS 应用转向 Web，欧盟企业每年可节省 110 亿欧元开发成本和 13 亿欧元 App Store 费用。目前这只是倡导性联名信，并非欧盟正式立案或裁决，相关节省估算也尚待验证。

telegram · zaihuapd · 11月24日 03:02

**「监管背景」** 欧盟《数字市场法》对大型平台设定开放义务，据此苹果已在欧盟允许竞品浏览器使用自有引擎，不再要求所有 iOS 浏览器都依赖 WebKit。联名方称，现有技术和法律门槛仍使厂商难以把已有用户迁出 WebKit，因此这封联名信要求欧盟委员会正式立案审查。

**「实际影响」** 对在欧盟运营的浏览器厂商和开发者来说，直接约束是竞品仍须维持基于 WebKit 的 iOS 版本，难以把已有用户迁移到自有引擎，应用触达用户也继续高度依赖 App Store；信中所称的成本节省能否实现，取决于欧盟是否启动调查并推动苹果调整规则，而目前尚无立案或整改时间表。

**标签**: `#EU DMA`, `#Apple`, `#浏览器竞争`, `#App Store`, `#开放 Web`

---

<a id="item-tech-news-12"></a>
### [黄循财：新加坡不会成为规避芯片管制通道](https://www.bloomberg.com/news/articles/2026-11-24/singapore-won-t-be-conduit-to-skirt-us-chip-curbs-wong-says) ⭐️ 7.0/10

新加坡总理黄循财表示，新加坡不会成为企业规避美国芯片出口管制的通道，当局正在调查 Megaspeed 采购英伟达芯片的交易。就在他表态的前一天，美国商务部将 Megaspeed 及另外 6 家东南亚企业列入贸易黑名单；《联邦公报》称这些企业存在向未获授权用户转移先进计算产品的“重大风险”，名单还包括它们在马来西亚和泰国的关联实体。路透社报道，阿里巴巴新加坡子公司 Apex Enterprise Solutions 也在名单之列，阿里巴巴表示从未转移受管制的先进计算芯片。

telegram · zaihuapd · 11月24日 05:03

**「背景」** 黄循财表态的前一天，美国商务部将 Megaspeed 及另外 6 家东南亚企业列入贸易黑名单。按《联邦公报》的说法，这些企业存在把先进计算产品转移到未获授权用户手中的“重大风险”，名单还涉及其在马来西亚和泰国的关联实体；路透社报道，阿里巴巴新加坡子公司 Apex Enterprise Solutions 也在其中，阿里否认曾转移受管制的先进计算芯片。

**「影响」** 对在东南亚采购或转运美国先进计算芯片的企业而言，相关调查和黑名单意味着经新加坡或马来西亚、泰国关联实体进行的交易需要更严格地核查最终用户与最终用途，以避免被认定为规避管制。

**标签**: `#AI chips`, `#export controls`, `#Singapore`, `#Nvidia`, `#semiconductor supply chain`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [ERNIE 5.5 Flash 的 vLLM Day-0 插件支持](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 6.0/10

rss · vLLM Blog · 11月24日 00:00

**「背景」** ERNIE 5.5 Flash Preview 是 280B 总参数、每 token 激活 14B 的稀疏 MoE 模型，支持 100 万 token 上下文、思考与工具调用，面向长程 Agent 任务。为让它发布当天就能在 vLLM 上服务，同时避免维护 fork、专用镜像或等待 nightly wheel，百度 ERNIE 团队与 vLLM 选择了独立插件 vLLM-ERNIE。

**「方案」** 该插件装在与 vllm==0.32.0 相同的环境中，通过 vllm.general\_plugins 入口自动注册；register\(\) 只把架构以模块路径登记，待 config.json 命中时才导入模型代码，因此同环境服务其他模型不受影响。模型侧，作者围绕推理成本重构注意力、残差、MoE 和输出头：37 层 HCA 加 6 层 MLA-DSA，512 个路由专家、top-10 加共享专家，并用 4 条 mHC 残差流承载 4096 隐藏维。为避免逐算子实现带来的中间张量与访存开销，团队把 VHA 混合参数预折叠进权重并融合 FP8 量化，合并多路由 GEMM 与路由链，将 MultiMax 分段激活改为单遍读写，并融合门控、norm/RoPE/KV 写入等，报告单内核比朴素实现快 1.55×–6.53×。FlashIndexer 用动态头路由和阈值预过滤降低稀疏索引成本，需冻结主干、仅用约 1B token 蒸馏轻量路由器，作者称 1M 上下文下带来 1.4× 加速。量化上，路由专家采用 MXFP4（W4A8）QAT，训练伪量化与推理粒度、scale、舍入一致，KV cache 为 FP8；DSpark 草稿模型经多阶段训练，每步最多提议 7 个 token，作者报告真实编码与 Agent 负载平均接受长度超过 4.0。上述加速数字均来自作者报告，未见独立基准复现。

**「启示」** 作者的核心论点是：新模型的 day-0 支持不必靠 fork 或专用镜像，vLLM 插件可以把模型代码与关键内核优化解耦，同时复用核心的调度、并行和服务能力；而 ERNIE 5.5 Flash 的性能来自架构、量化、稀疏索引与投机解码的协同设计，而非单一技巧。

**标签**: `#vLLM`, `#ERNIE`, `#MoE inference`, `#kernel fusion`, `#speculative decoding`

---

<a id="item-tech-blog-2"></a>
### [从 Megaspeed 案看算力如何绕过芯片出口管制](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196937) ⭐️ 5.0/10

rss · Dapenti Xilei · 11月23日 23:17

**「背景」** 先进 AI 芯片的出口管制以物理交付和海关清关为核心，但云计算的普及让算力设施的存放地与服务消费端可以完全分离——训练模型并不需要拥有芯片产权。企业从「买芯片」转向「买算力」，以许可证与边境查验为支点的监管因此出现结构性盲区。

**「方案」** 作者以新加坡云平台 Megaspeed 为线索串起这套漏洞：它 2023 年 11 月加入英伟达云计算合作伙伴计划，公开将阿里巴巴列为核心客户，并通过马来西亚子公司 Speedmatrix 在境外数据中心部署先进芯片，以「合法境外托管＋合法算力出口」完成供给。2025 年 6 月英伟达将其列入内部禁售名单，8 月核心高管 Alice Huang 称离职，同年 Novagate Cloud 在新加坡注册；据报 2026 年 1 至 5 月至少价值 3 亿美元的英伟达相关硬件运抵其马来西亚关联单位，做空机构 Culper Research 质疑两家公司网页设计与注册地址高度重合，媒体与知情人士称原团队已转投运营。刑事层面则触及红线：新加坡检方于 2025 年 2 月及 2026 年 7 月指控幕后操盘者李明及其公司 Luxuriate Your Life 在 2023 年 11 月两次向 Supermicro 提交虚假的最终用途与最终用户声明，涉案服务器绕道马来西亚，暴露出 KYC 在多层中间商与跨境物流面前的追溯乏力。作者还梳理了世纪龙腾、Aivres、世纪华通等股权与人脉网络，并明确提醒做空报告和媒体爆料不等同于起诉书或定罪。

**「启示」** 作者认为，当算力彻底无界化，基于物理国界、实物清关和单一实体名单的传统管制正不可避免地边际效用递减；真正的博弈命题已变成：未来究竟该管硬件出口，还是重新定义跨境算力与数据的边界。

**标签**: `#AI chip export controls`, `#cloud compute`, `#supply-chain compliance`, `#regulatory arbitrage`, `#Megaspeed case`

---

<a id="item-tech-blog-3"></a>
### [上传图片即可入侵服务器：Upload2Shell 漏洞通报](https://www.appinn.com/upload2shell-cve-2026-125396/) ⭐️ 4.0/10

rss · Appinn · 11月24日 03:08

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/upload2shell-cve-2026-125396/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;缩略图生成、PDF 预览、打印任务这类常见功能，背后往往由拥有数十年历史的开源工具 Ghostscript 处理 PostScript/PDF 文件。研究人员公开的 Upload2Shell（CVE-2026-125396，CVSS 4.0 评分 8.5，高危）正出在这里：特制文件可突破 Ghostscript 安全沙箱并在服务器上执行任意命令，甚至在扩展名为 .jpg、.png 的上传流程中也可能被触发。

**「方案」** 作者梳理的是一份影响面与补丁清单，而非机制剖析。据其转述，研究人员已在 WordPress 媒体上传、Roundcube 打开含恶意附件的邮件（服务端自动生成缩略图，用户无需点击附件）、CUPS 共享打印任务、Forminator 与 Elementor 相关表单上传、MediaWiki 的 PDF 上传与缩略图生成，以及 Google 部分文件处理服务中验证了攻击路径；Pillow、ImageMagick 以及 ComfyUI、Stable Diffusion WebUI 等 AI 绘图工具也被列为潜在触发面。时间线上，漏洞于 2026 年 7 月 27 日发现，11 月 21 日公开技术细节。修复侧，Ghostscript 早在 9 月 8 日发布的 10.08.0 已修补，WordPress 对应 7.0.4、6.9.7、6.8.8，Roundcube 为 1.6.20，Debian 12/13 与 Ubuntu 亦已发布更新；作者特别提醒 Docker 部署需检查容器内部的 Ghostscript 版本。安全公司 Sophos 表示，截至 11 月 23 日漏洞验证代码已公开，但尚无真实攻击的公开报告。文章本身仅用一段话概括沙箱绕过原理，未展开不同应用的触发链差异、检测方法与缓解权衡。

**「启示」** 作者的核心提醒很直接：自建服务器与自托管应用的用户应尽快核对并升级 Ghostscript 及相关软件。这件事也说明，深埋在众多应用之下的基础组件一旦失守，风险会沿调用链成倍放大，补丁能否及时下沉往往比单点漏洞本身更关键。

**标签**: `#漏洞通报`, `#Ghostscript`, `#CVE-2026-125396`, `#补丁管理`, `#供应链安全`

---

<a id="item-tech-blog-4"></a>
### [WinGet 新增 MCP 支持，AI 可代装 Windows 软件](https://www.appinn.com/winget-mcp-server/) ⭐️ 4.0/10

rss · Appinn · 11月23日 07:19

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/winget-mcp-server/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;WinGet 是微软为 Windows 提供的命令行包管理器，作用类似 macOS 的 Homebrew 或 Linux 的 apt，可用一条命令搜索、安装、升级和卸载软件。微软如今为它加入 MCP（模型上下文协议）支持，使支持 MCP 的 AI 助手能直接调用 WinGet。

**「方案」** 据作者转述，WinGet MCP Server 目前只开放两个工具：find 用于搜索软件包并获取信息，install 用于安装指定软件并支持指定版本；AI 可以先搜索，再在用户确认后执行安装。启用条件是 Windows 10 1809（Build 17763）以上以及支持 MCP 的 WinGet：在 PowerShell 中先运行 winget configure --enable，再运行 winget mcp；正常时会输出含 WindowsPackageManagerMCPServer.exe 路径的 JSON，若提示 Unrecognized command: &\#x27;mcp&\#x27; 则说明版本过旧、需要更新。配置方面，VS Code 可在项目的 .vscode/mcp.json 中以 stdio 类型填入该 exe 的完整路径，随后在 GitHub Copilot 聊天窗口切换到 Agent 模式并确认 winget-mcp 已启用；GitHub Copilot CLI 则启动 copilot 后输入 /mcp add、填入路径即可。作者认为，这能让 AI 在搭建开发环境时自行补齐缺少的 Git、Python 等工具，减少额外消耗的 Token，并预期微软会继续扩大 AI 可操作的 Windows 功能，同时希望少一些强制集成。

**「启示」** 作者的核心判断是，MCP 让软件包管理成为 AI Agent 可直接调用的能力，从而减少搭建环境时的手动步骤与 Token 消耗；不过目前仅开放 find 与 install，系统级 AI 操作的权限与安全边界仍待观察。

**标签**: `#WinGet`, `#MCP`, `#Windows 包管理器`, `#AI Agent`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [台股收涨 8.99% 台积电涨停](https://news.rthk.hk/rthk/ch/component/k2/1879065-20261124.htm) ⭐️ 8.0/10

台湾加权指数收报 40122 点，上涨 3310 点，涨幅为 8.99%，重新站上 4 万点。权重股台积电上涨近 10%，达到涨停。

rss · RTHK Finance · 11月24日 06:19

**「背景」** 加权指数是台湾股市的主要大盘指数，台积电属权重股，其升停会明显拉动指数。台股今次亦重上 4 万点关口。

**标签**: `#Taiwan stocks`, `#TAIEX`, `#TSMC`, `#market surge`, `#limit up`

---

<a id="item-finance-news-2"></a>
### [AI 抛售令 DeepSeek 等中国 AI 公司上市计划蒙上阴影](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 8.0/10

在 AI 公司 Anthropic 完成 1195 亿美元创纪录 IPO 后，全球 AI 股遭遇抛售，DeepSeek、月之暗面和阶跃星辰筹备或考虑中的上市计划因此蒙上阴影；中国科技股自 6 月底以来累计蒸发 1.7 万亿美元。

telegram · zaihuapd · 11月23日 09:31

**「背景」** Anthropic 是一家美国人工智能公司，其 1195 亿美元首次公开募股（IPO）创下纪录，却成了随后全球 AI 股抛售的导火索；中国科技股自 6 月底以来累计蒸发 1.7 万亿美元，使计划上市的 AI 公司面临更冷的发行窗口。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AI selloff`, `#Chinese tech stocks`, `#IPO market`, `#Anthropic`, `#DeepSeek`

---

<a id="item-finance-news-3"></a>
### [纽约联储威廉姆斯：通胀回落到 2%仍需努力，加息可能“随时间推移”推进](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

纽约联储主席威廉姆斯表示，要令通胀回到 2%目标“仍然有工作要做”，并暗示进一步加息可以“随时间推移”展开；在他讲话前，市场已完全定价 12 月 8-9 日议息会议加息 25 个基点，当前联邦基金利率目标区间为 3.75%-4%。他预计通胀将在 2027 年接近 2%目标、并于次年达到该目标。

rss · CNBC Finance · 11月23日 21:02

**「背景」** 美国通胀仍明显高于美联储 2%的目标，而官员们对加息速度存在分歧：部分人主张更激进，威廉姆斯等人则强调循序渐进的路径。他将当前价格压力归因于伊朗冲突、人工智能建设相关的商品需求以及关税，但称关税作为压力来源“已基本消退”。

**「影响」** 若 12 月加息落地，与政策利率挂钩的房贷、信用卡等借贷成本会随之走高，对利率敏感的家庭和企业将直接感受到融资成本上升。

**标签**: `#Federal Reserve`, `#monetary policy`, `#inflation`, `#interest rates`, `#John Williams`

---

<a id="item-finance-news-4"></a>
### [英伟达市值增加近 1 万亿美元，带动科技股上涨](https://www.bbc.co.uk/news/articles/cq62pn6j42jko?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

据 BBC 报道，黄仁勋回归后，英伟达市值增加近 1 万亿美元，并带动科技股上涨，纳斯达克指数上涨 6.5%。

rss · BBC Business · 11月23日 21:23

**「背景」** 英伟达是一家美国芯片公司，设计用于人工智能计算等领域的图形处理器（GPU），其股价大涨会通过市值加权的纳斯达克指数直接带动整体科技股走高。

**「受影响群体」** 由于纳斯达克是科技股占比较高的指数，这轮由英伟达带动的反弹会直接抬高持有纳斯达克相关指数基金和退休账户的普通投资者的持仓价值。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Nvidia">Nvidia - Wikipedia</a></li>
<li><a href="https://www.ft.com/content/20d2ebe3-e945-4659-a122-31bf85a4e4e5?syn-25a6b1a6=1">Nvidia live: Nvidia gains nearly $ 1 tn in value after Jensen Huang...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Nasdaq`, `#US equities`, `#technology sector`, `#market rally`

---

<a id="item-finance-news-5"></a>
### [Capita 股价据报道暴跌 70%，首席执行官因公务员养老金支付延误辞职](https://www.bbc.co.uk/news/articles/c65y1qqw3kjxo?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

据 BBC 报道，外包公司 Capita 的股价下跌 70%，其首席执行官在公务员养老金支付出现延误后辞职。Capita 自去年起负责管理该养老金支付计划，目前尚不清楚受影响员工人数及具体财务影响。

rss · BBC Business · 11月23日 11:24

**「背景」** Capita 自去年 12 月接手英国公务员养老金计划的管理工作；一名内阁办公室部长上月称其改善该计划运作的进展“糟糕”。

**「影响范围」** 影响直接落在两处：依赖公共部门养老金发放的退休人员面临收入到账延迟；而持有 Capita 股票的投资者则在股价下跌七成中损失了大部分市值。Capita 是一家总部位于伦敦、为政府等机构提供外包服务的上市公司。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/c65y1qqw3kjxo">Capita shares plunge 70% as boss quits after civil service pensions ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Capita">Capita - Wikipedia</a></li>

</ul>
</details>

**标签**: `#Capita`, `#pensions`, `#executive turnover`, `#share price`, `#public sector outsourcing`

---

<a id="item-finance-news-6"></a>
### [证监会主席黄天祐：首只无纸化新股上市，为 T+1 交收等改革铺路](https://news.rthk.hk/rthk/ch/component/k2/1879060-20261124.htm) ⭐️ 7.0/10

香港证监会主席黄天祐于 11 月 24 日出席首只在无纸证券市场制度下上市的新股先通医药上市仪式时表示，这标志著无纸化改革的新起点，并指该制度为未来改革创造空间，例如港交所正积极推进把港股交收及结算周期由「T+2」缩短至「T+1」。他回顾，香港自 2002 年提出无纸证券市场构想，至今近四分之一个世纪才正式实施。

rss · RTHK Finance · 11月24日 05:15

**「背景」** 香港早在 2002 年就提出无纸证券市场构想，相关法例其后全部获通过；证监会表示，视乎市场准备情况，措施于 2026 年初实施，届时投资者不能再以纸张形式持有相关证券（工具 1-1、1-2）。首家在该制度下上市的公司先通医药，正是在这一新规框架下挂牌。

**「对投资者与券商的影响」** 对散户投资者而言，新制度让他们可以用本人名义以电子方式持有证券，并更直接地行使股东权利；证监会主席提到，港交所正在推进把交收周期由「T+2」缩短至「T+1」，这项计划若落实，将改变券商与投资者的交收和资金安排。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.hk01.com/%E8%B2%A1%E7%B6%93%E5%BF%AB%E8%A8%8A/60230584/%E8%AD%89%E7%9B%A3%E6%9C%83%E6%8C%87%E8%AD%89%E5%88%B8%E5%B8%82%E5%A0%B4%E7%84%A1%E7%B4%99%E5%8C%962026%E5%B9%B4%E5%88%9D%E5%AF%A6%E6%96%BD">证 监 会 指 证 券 市 场 无 纸 化 2026 年初 实 施 | 香 港 01</a></li>
<li><a href="https://licenses.com.hk/article/5594610139481092">证 监 会 如期推进于 2026 年初 实 施 无 纸 证 券 市 场 制度的准备工作</a></li>

</ul>
</details>

**标签**: `#香港证券市场`, `#无纸证券`, `#证监会`, `#市场基建`, `#T+1交收`

---

<a id="item-finance-news-7"></a>
### [上海地铁 12 月 1 日起调整票价，21 年来首次](https://weibo.com/1699432410/5368461393397183) ⭐️ 7.0/10

据新华社报道，上海将于 12 月 1 日起调整轨道交通票价，为 21 年来首次；起步价 3 元、覆盖 0 至 4 公里，之后按 4、4、4、7、7、10、10 公里各加 1 元，50 公里以上每 15 公里加 1 元。同步推出 35 次、45 次、60 次、90 次四档计次票，定价分别为 190 元、210 元、270 元、390 元，11 月 26 日开售；同一支付渠道当月累计满 90 元享 9 折。

telegram · zaihuapd · 11月23日 10:45

**「背景」** 上海地铁于 1993 年开通运营，现行票价已沿用 21 年；因此，本次调价同步推出计次票和满额折扣，以减轻对高频出行人群的影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E4%B8%8A%E6%B5%B7%E5%9C%B0%E9%93%81%E8%BD%A6%E7%AB%99%E5%88%97%E8%A1%A8">上海地铁 车站列表 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**标签**: `#Shanghai metro`, `#public transport fares`, `#commuting costs`, `#China policy`, `#fare adjustment`

---