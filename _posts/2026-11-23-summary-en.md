---
layout: default
title: "Horizon Summary: 2026-11-23 (EN)"
date: 2026-11-23
lang: en
---

> From 105 items, 14 important content pieces were selected

---

**Technology News**
1. [OpenAI Explores Perplexity as a Measure of Model Intelligence](#item-tech-news-1) ⭐️ 7.0/10
2. [FT Alleges Prince Group Associate Helped Smuggle Nvidia Chips to China](#item-tech-news-2) ⭐️ 7.0/10
3. [Google&\#x27;s Mirror Dimension simulates the web to test Chrome&\#x27;s AI agent](#item-tech-news-3) ⭐️ 7.0/10
4. [Windows Server 2028 to omit WoW64 by default, requiring manual FoD install](#item-tech-news-4) ⭐️ 7.0/10

**Technology Blog**
1. [When in Doubt, Flail: Experimentation for Ambiguous Work](#item-tech-blog-1) ⭐️ 5.0/10
2. [Error Anthology: How Mistakes Advance Science](#item-tech-blog-2) ⭐️ 5.0/10
3. [Strata 0.2.18 adds 224B Hy4-Flash, raising local memory floor to 64GB](#item-tech-blog-3) ⭐️ 5.0/10
4. [Leonida: Early Static-Recompilation GTA 6 PC Port Project](#item-tech-blog-4) ⭐️ 4.0/10
5. [TotK Recomp 0.5.0 Adds FSR 3.1, Frame Generation, and Quick Save](#item-tech-blog-5) ⭐️ 4.0/10

**Financial News**
1. [China&\#x27;s Shanghai, Shenzhen and Beijing exchanges to cut margin financing deposit ratio to 80%](#item-finance-news-1) ⭐️ 8.0/10
2. [US tech selloff prompts Asian market stabilization measures](#item-finance-news-2) ⭐️ 8.0/10
3. [South Korea Says It Is Ready to Deploy Market Stabilization Fund](#item-finance-news-3) ⭐️ 7.0/10
4. [台湾证交所与十家券商达成共识：融资担保维持率下调至120%](#item-finance-news-4) ⭐️ 7.0/10
5. [Record El Niño warming raises pressure on food aid](#item-finance-news-5) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [OpenAI Explores Perplexity as a Measure of Model Intelligence](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI has published an article titled “Perplexity and Intelligence” that examines the relationship between language-model perplexity and model intelligence. The supplied material does not include the article’s definitions, data, model versions, or measured results, so the specific claims and their strength cannot be checked. That leaves the piece as a conceptual or evaluative discussion rather than a verifiable release or independently measured benchmark result.

hackernews · acossta · Nov 22, 17:06 · [Discussion](https://news.ycombinator.com/item?id=50601525)

**「Background」** Perplexity is the degree of surprise a model shows when predicting each next token over a sequence; a perfect predictor scores 1, while a random predictor approaches the vocabulary size. The OpenAI article, by Chief Scientist Jakub Pachocki, argues that perplexity—equivalently cross-entropy loss—should serve as a common metric across model developers and inform shared safety standards, though commenters noted it does not fully explain how entropy, log-perplexity, and perplexity relate.

**「Community Discussion」** Commenters debated the metric’s significance: one supplied a definition of perplexity and noted that the article did not define it, while another argued that prediction and compression rates naturally track progress toward richer world models. Another commenter said they were surprised cross-entropy still showed a clear trend amid RL-based reasoning models, and a further comment relayed an unverified claim that Microsoft had added MAI models to a shared chart, reporting 0.819 log-perplexity for MAI-2 Base.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>

</ul>
</details>

**Tags**: `#language models`, `#perplexity`, `#model evaluation`, `#cross-entropy`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [FT Alleges Prince Group Associate Helped Smuggle Nvidia Chips to China](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 7.0/10

The Financial Times, in a report summarized on Telegram, alleges that Hu Xiaowei—identified by the US Treasury as Cambodia&\#x27;s Prince Group&\#x27;s “number two”—helped move Nvidia chips into China through a network involving shell companies, underground financing, and private jets. Quoting trade data, the report says a Malaysian subsidiary of Megaspeed declared about $4.6 billion of imports from December 2024 to December 2025, with some chips allegedly reaching China&\#x27;s black market. Prince Group denied that Hu worked for it and said allegations about an illegal network and private-jet smuggling lack factual basis. The account is a secondary summary of the FT report, and the smuggling allegations have not been independently verified.

telegram · zaihuapd · Nov 22, 04:34

**「Background」** The report centers on Megaspeed, a Singapore-based cloud-computing provider, and its Malaysian subsidiary Speedmatrix. FT reporting reflected in search results says Speedmatrix declared about $4.6 billion in imports from Aivres between December 2024 and December 2025. The same investigation links people connected to a Cambodian criminal organization and Chinese gaming companies to the suspected smuggling network.

<details><summary>References</summary>
<ul>
<li>FT investigation links Alice Huang&#x27;s Megaspeed to a gaming group ...</li>
<li>Cambodian crime links emerge in suspected Nvidia chip smuggling ...</li>
<li>How Megaspeed built a network in Southeast Asia to move Nvidia ...</li>

</ul>
</details>

**Tags**: `#Nvidia`, `#chip smuggling`, `#export controls`, `#AI hardware`, `#supply chain`

---

<a id="item-tech-news-3"></a>
### [Google&\#x27;s Mirror Dimension simulates the web to test Chrome&\#x27;s AI agent](https://www.landian.news/archives/128701.html) ⭐️ 7.0/10

Google reportedly built a simulated internet called Mirror Dimension to test Chrome&\#x27;s AI agent in isolation, according to a brief report from Landian News. The environment contains thousands of simulated websites, with each engineer working in a separately isolated test setup, and covers actions such as opening sites, searching and browsing, logging in, adding items to a cart, and completing tasks. More than 1,000 test cases run per day, with emphasis on defending against prompt-injection and other attacks from malicious web pages. The report is a short secondary summary and does not describe how the simulated sites are generated or how test results feed into shipped Chrome builds.

telegram · zaihuapd · Nov 23, 01:30

**「Why a synthetic web」** Chrome&\#x27;s “auto browse” is a browser-use agent: it carries out tasks across websites rather than only recommending pages, so it must be tested against realistic sites and hostile page content. Google&\#x27;s security blog says Mirror Dimension is a synthetic version of the web with thousands of simulated sites for evaluating such agents without real-world security risk, and ExplainX notes that the test environment includes planted prompt-injection attacks.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.google/security/mirror-dimension-for-agents/">Mirror Dimension for Agents: Evaluating Browser-Use Agents ...</a></li>
<li><a href="https://explainx.ai/blog/google-mirror-dimension-synthetic-web-chrome-auto-browse-agents-prompt-injection-testing-2026">Google Mirror Dimension: Fake Web for Chrome AI Agents ...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#Chrome`, `#prompt injection`, `#security testing`, `#browser automation`

---

<a id="item-tech-news-4"></a>
### [Windows Server 2028 to omit WoW64 by default, requiring manual FoD install](https://www.windowslatest.com/2026/11/23/32-bit-apps-days-are-numbered-as-microsoft-strips-support-bit-by-bit-starting-with-windows-server-2028-but-windows-11-is-safe-for-now/) ⭐️ 7.0/10

Microsoft said at Ignite 2026 that Windows Server 2028 will ship without the WoW64 compatibility subsystem by default, so 32-bit applications will not run out of the box. The server release is planned for fall 2027 alongside Windows 11 27H2, and administrators who need legacy 32-bit software can add WoW64 back as a Feature on Demand, typically through PowerShell or DISM on Server Core. Microsoft cited a reduced attack surface and blocking 32-bit malware as reasons; Windows 11 still includes WoW64, and Microsoft has not announced a removal plan for it. This account is a secondary report of the Windows Latest article, so some implementation details remain unverified.

telegram · zaihuapd · Nov 23, 03:03

**「What WoW64 does」** WoW64 is the compatibility subsystem that lets 64-bit Windows run 32-bit applications. A report on the change notes that Windows Server 2028 would be the first 64-bit Windows release that cannot run 32-bit applications out of the box, with the subsystem available only as an optional add-on.

**「Impact」** Administrators running 32-bit server applications will need to add the WoW64 Feature on Demand, typically via PowerShell or DISM on Server Core, before those apps can run on a default installation. Deployment images and upgrade checklists that assume 32-bit support should be reviewed before migration.

<details><summary>References</summary>
<ul>
<li><a href="https://thecommunity.ru/microsoft/windows/server/12123-windows-server-2028-po-umolchaniju-ne-budet-podderzhivat-32-bitnye-prilozhenija.html">Windows Server 2028 по умолчанию не будет поддерживать...</a></li>

</ul>
</details>

**Tags**: `#Windows Server 2028`, `#WoW64`, `#32-bit compatibility`, `#Microsoft`, `#enterprise IT`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [When in Doubt, Flail: Experimentation for Ambiguous Work](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 5.0/10

rss · Sean Goedecke · Nov 23, 00:00

**「Background」** Engineers often face unclear product, technical, or organizational problems without clear guidance. Sean Goedecke argues that waiting for certainty is usually worse than deliberately experimenting, though he acknowledges that badly handled experimentation can damage a reputation.

**「Solution」** The author’s “flailing” method has three parts: try many different things, pay careful attention to feedback from people and results, and ruthlessly drop approaches that are not getting positive feedback. Trying many things provides direct contact with reality, raises the odds that one idea works since most will fail, and prevents overinvestment in any single plan. He applies this to product work, where he reports that many GitHub Models features failed but AI inference from a GitHub Actions token proved sticky and seeded “Continuous AI”; to engineering work, where he favors speculative changes over fully mapping huge, tangled systems and keeping only demonstrated improvements; and to organizational work, where he suggests automating manual work, volunteering, and proposing long-term plans even though most will not help. In the organizational case especially, he warns that missing feedback can turn others’ frustration toward you. He says the process feels like failure from the inside, but that feeling should not be treated as proof the approach is wrong.

**「Takeaway」** When information is insufficient, disciplined experimentation and rapid response to feedback can produce useful understanding faster than exhaustive analysis. The approach is viable only if you drop failing bets quickly enough to preserve trust.

**Tags**: `#engineering-career`, `#decision-making`, `#experimentation`, `#software-engineering`, `#organizational-dynamics`

---

<a id="item-tech-blog-2"></a>
### [Error Anthology: How Mistakes Advance Science](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196917) ⭐️ 5.0/10

rss · Dapenti Xilei · Nov 23, 00:01

**「Background」** The article challenges the familiar story of science as a chain of flawless genius by retelling five researchers&\#x27; mistakes, dead ends, and biases. It is a secondary popular-science roundup built from anecdotal cases, and its central claim is that progress depends less on avoiding error than on building mechanisms that catch and correct it.

**「Solution」** At LIGO, Peter Shawhan&\#x27;s team turned years of null results into roughly 100 papers defining exclusion bounds, and a blind-injection test caught a mirror-direction error in a candidate signal, which they traced in a day. Omar Yaghi describes dismissing a student&\#x27;s metal-organic compounds as useless &quot;sculptures&quot; before her persistence yielded stable MOFs, while plant researchers nearly deleted anomalous wild-tomato samples that later proved to be a separate species, Solanum nectarifolium. Catherine Badgley canceled a contracted book after global data showed Africa&\#x27;s and North America&\#x27;s climate spaces barely overlapped, undermining a universal predictive formula. In a nitrogen-fixation study, a temporary worker averaged nodule counts and ruined one replicate, but randomized block design preserved four independent replicates and statistical significance.

**「Takeaway」** The author&\#x27;s conclusion is that scientific success should be redefined around error-surfacing and error-containing practices—null results, outlier checks, stopping rules, and redundancy—rather than the absence of failure. The cases are illustrative and largely unverified, so they support a useful mindset more than a proven method.

**Tags**: `#科学方法论`, `#科研失误`, `#容错设计`, `#科普综述`, `#案例分析`

---

<a id="item-tech-blog-3"></a>
### [Strata 0.2.18 adds 224B Hy4-Flash, raising local memory floor to 64GB](https://www.appinn.com/strata-0-2-18/) ⭐️ 5.0/10

rss · Appinn · Nov 22, 07:06

**「Background」** Strata is a tool built to run open-weight large models at usable speed on ordinary home machines, previously centered on Qwen variants and a 1-bit DeepSeek. Version 0.2.18, released November 22, adds native support for Tencent&\#x27;s Hy4-Flash — but pushes the entry requirement up to 64 GiB of system memory.

**「Solution」** Hy4-Flash is a mixture-of-experts model with 224B total parameters, about 12B activated per token \(roughly 64B of the total are Engram lookup parameters\), image understanding, and a context window of up to one million tokens. Strata ships a separate strata-hy4 inference engine downloaded on demand, three quantization tiers — SQ-64, SQ-96 and SQ-128 at 129.61 GB, 157.16 GB and 181.23 GB on disk, targeting 64, 96 and 128 GiB of RAM respectively — plus built-in DFly2 speculative decoding, an optional 0.93 GB vision component, and support for Windows, Linux, Apple-silicon Macs and DGX Spark. Upgrades keep existing Qwen/DeepSeek models, chats and settings, and the API now accepts original model names. The author&\#x27;s comparison, drawn from Tencent&\#x27;s model card with each model run at its highest available inference tier, favors Hy4-Flash on agent and computer-use tasks \(OSWorld 2.1 partial score 68.1 vs 58.8; APEX-Agents 63.1 vs 57.6; AutomationBench 52.2 vs 49.3\) and Qwen on coding and terminal tasks \(DeepSWE 64.6 vs 65.1; Terminal-Bench 4.0 19.2 vs 29.5; ProgramBench 16.0 vs 22.0\). The author stresses the memory floor: an RTX 3090 with 24 GB of VRAM and 48 GB of RAM still falls below the official SQ-64 baseline, so he could not test it himself and advises users under 64 GB to stay on Qwen, while those with 96 or 128 GiB can experiment by workload.

**「Takeaway」** The update trades accessibility for capability: Hy4-Flash looks stronger for agentic and GUI work but weaker for coding, and only becomes practical once a machine clears 64 GB of RAM. The supporting numbers come from the vendor&\#x27;s own model card rather than independent reproduction, so the author frames them as a starting point for users to benchmark themselves.

**Tags**: `#本地大模型`, `#Strata`, `#Hy4-Flash`, `#量化部署`, `#基准评测`

---

<a id="item-tech-blog-4"></a>
### [Leonida: Early Static-Recompilation GTA 6 PC Port Project](https://www.appinn.com/gta-6-pc-port-leonida/) ⭐️ 4.0/10

rss · Appinn · Nov 22, 13:26

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/gta-6-pc-port-leonida/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;《GTA 6》 has not yet arrived on PC, and the article reports that an open-source project called Leonida is already exploring how to run the Xbox Series version natively on Windows. The author frames this as an early technical experiment rather than a usable port.

**「Solution」** Leonida uses static recompilation, the same broad approach the article links to earlier Zelda PC port projects: because Xbox Series consoles and modern PCs share x86-64, the plan is to load and execute the game&\#x27;s CPU code directly on Windows while reimplementing the Xbox system services it depends on. The article notes that the project comes from a developer previously associated with the Ocarina of Time static-recompilation port. The author stresses that this is far from just running the executable: the project must also handle Xbox system calls, memory management, graphics interfaces, audio, and many runtime dependencies. One concrete bottleneck is translating Xbox GPU shaders into a format PC graphics APIs can consume; according to the README, Leonida has converted 26,503 shaders and statically validated them through SPIR-V. It can already export models, textures, and audio, though some formats remain unfinished, and work has begun on an Xbox API compatibility layer and on D3D12-to-Vulkan graphics translation. The loader can run a substitute test program, but the article says the actual GTA 6 executable has not been tested and no real gameplay has been shown. The project does not supply game files, has no playable build, and gives no completion timeline; the author calls it a pie in the sky that nevertheless shows real progress, with evidence drawn mostly from the project README.

**「Takeaway」** The author&\#x27;s conclusion is that Leonida is not a playable GTA 6 PC port and is not yet aimed at ordinary players, but its shader and resource-conversion milestones make it a notable early test of whether static recompilation can be applied to a modern Xbox blockbuster. For readers interested in game porting, console emulation, or static recompilation, it is worth watching precisely because it documents credible groundwork before an official PC release.

**Tags**: `#static recompilation`, `#GTA 6`, `#Xbox Series`, `#game porting`, `#shader translation`

---

<a id="item-tech-blog-5"></a>
### [TotK Recomp 0.5.0 Adds FSR 3.1, Frame Generation, and Quick Save](https://www.appinn.com/totk-recomp-0-5-0/) ⭐️ 4.0/10

rss · Appinn · Nov 22, 07:37

**「Background」** TotK Recomp recompiles The Legend of Zelda: Tears of the Kingdom into a native Windows/Linux PC build; version 0.5.0 is a feature and performance update.

**「Solution」** According to the author&\#x27;s changelog recap, it bundles AMD FSR 3.1 upscaling and FSR 3 frame generation for NVIDIA, AMD, and Intel GPUs without extra plugins. Frame generation inserts an interpolated frame between two rendered frames, so a 60 FPS render can display near 120 FPS; both features are off by default, and the developer advises reaching 60 rendered FPS first to limit input latency and visual artifacts. The update adds a free camera detached from Link, F6/F7 quick save and load that do not affect manual saves, PlayStation button prompts, and better mod compatibility with conflict inspection; free camera and quick save require game version 1.4.3. Developer-reported performance work includes Windows PGO compilation for roughly 6–12% higher FPS, a sync\_ahead optimization for about 6–10% on a GTX 1050 Ti, and barrier\_merge raising a waterfall scene from 82 to 141 FPS on an RX 7900 XT. The author also notes fixes for AMD frame-rate drops after sustained play, water flicker, shadow anomalies, and some shrine mechanisms failing at high frame rates. Upgrades install in place and preserve game files, saves, and configuration while regenerating the executable and shader cache.

**「Takeaway」** The update broadens the port&\#x27;s appeal with more flexible controls and smoother output, but the headline gains are developer-reported and frame generation works best when the base render is already at 60 FPS.

**Tags**: `#release notes`, `#game recompilation`, `#frame generation`, `#FSR upscaling`, `#PC performance tuning`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s Shanghai, Shenzhen and Beijing exchanges to cut margin financing deposit ratio to 80%](https://news.rthk.hk/rthk/ch/component/k2/1878864-20261123.htm) ⭐️ 8.0/10

Shanghai, Shenzhen and Beijing stock exchanges said they will lower the minimum margin ratio for investors buying securities on margin from 100% to 80%, effective November 30. The Shanghai Securities News, citing industry estimates, said the change could free up about 400 billion yuan in additional funds — a projection, not an official figure. The exchanges said the cut reflects a legal counter-cyclical adjustment, with margin trading activity having fallen noticeably and overall leverage low.

rss · RTHK Finance · Nov 22, 22:22

**「Background」** The minimum collateral investors must post when borrowing to buy shares was set at 100% and, with China&\#x27;s securities regulator&\#x27;s approval, will fall to 80% from Nov. 30.

**「Impact」** Investors who use margin financing will be able to take larger stock positions with the same amount of their own capital, because the minimum margin they must post falls; the accompanying fee waivers also lower trading costs for market participants.

<details><summary>References</summary>
<ul>
<li><a href="https://money18.on.cc/mobile/finnews/content/exp/bkn-20261122185844351-1122_00842_001.html">中國救 市 ！ 滬 深 北 交 所 下 調 融 資 保 證 金 比 例 至 80 % | 東網 Money18</a></li>

</ul>
</details>

**Tags**: `#融資保證金`, `#交易所政策`, `#市場流動性`, `#降費`, `#創業板做市商`

---

<a id="item-finance-news-2"></a>
### [US tech selloff prompts Asian market stabilization measures](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

US AI and technology stocks sold off sharply on Friday, with the Nasdaq falling 5.28% in one day and the Philadelphia Semiconductor Index dropping nearly 11%. Mainland China, South Korea and Taiwan responded with market-stabilization measures, including a cut in mainland China&\#x27;s minimum margin financing ratio to 80% and Taiwan&\#x27;s ban on short-selling below the previous close from November 23.

telegram · zaihuapd · Nov 22, 13:24

**「Background」** China’s cut reverses a January tightening that raised the minimum margin—the cash investors must post to borrow for stock purchases—to 100% to curb leverage. Taiwan’s ban on short sales below the prior close and South Korea’s stabilization-fund preparations are emergency market-support tools.

**「Market impact」** Short sellers and leveraged investors in mainland China, South Korea and Taiwan face immediate changes to trading rules—Taiwan bars short-selling below the previous close and raises margin requirements, while Seoul temporarily relaxes daily buyback limits for listed companies—as regional authorities move to stem further selling.

<details><summary>References</summary>
<ul>
<li><a href="https://www.investmentwatchblog.com/asian-governments-are-stepping-in-to-prop-up-stock-markets-taiwan-is-restricting-short-selling-china-is-making-it-easier-to-borrow-south-korea-is-preparing-a-rescue-fund/">Asian governments are stepping in to prop up stock markets ...</a></li>
<li><a href="https://stockanalysis.com/news/taiwan-short-sale-ban-asia-stock-support/">Taiwan bans short sales below prior close as Asia moves to ...</a></li>
<li><a href="https://www.thestar.com.my/business/business-news/2026/11/23/us-futures-bounce-while-asia-markets-brace-for-ai-wipeout">US futures bounce while Asia markets brace for AI wipeout</a></li>

</ul>
</details>

**Tags**: `#US tech selloff`, `#semiconductor stocks`, `#Asian market stabilization`, `#short-selling rules`, `#margin financing`

---

<a id="item-finance-news-3"></a>
### [South Korea Says It Is Ready to Deploy Market Stabilization Fund](https://news.rthk.hk/rthk/ch/component/k2/1878865-20261123.htm) ⭐️ 7.0/10

South Korea&\#x27;s Ministry of Economy and Finance said Sunday it stands ready to activate a stock market stabilization fund at any time if market conditions keep worsening, after an emergency meeting of economic policymakers. Officials also agreed to temporarily relax listed companies&\#x27; daily share buyback limits for three months, to monitor leveraged investment and margin calls more closely, and to crack down on illegal short selling; Taiwan&\#x27;s financial authorities separately ordered tighter short-selling rules on Saturday.

rss · RTHK Finance · Nov 22, 22:23

**「Background」** South Korea’s market stabilization fund is a policy tool funded by financial companies and securities-related institutions, including the Korea Exchange, to buy domestic equities; it was last used in 2008, and reports say authorities began preparing a 10.76 trillion won \($7.99 billion\) fund on Nov. 22.

**「Impact」** South Korean listed companies stand to benefit directly: from Tuesday, Nov. 24, they may place larger daily share-buyback orders for three months, a relaxation regulators intend to support demand and reduce volatility.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.biggo.com/news/41704fd7-7d88-4cb6-8773-17f6b6f5c964">South Korea Restarts Stock Market Stabilization Fund ...</a></li>
<li><a href="https://aistockwire.com/blog/korea-stock-market-stabilization-fund-first-since-2008-kospi-november-2026">Korea readies stock stabilization fund, last used in 2008</a></li>
<li>South Korea readies its market stabilization fund and Taiwan bans ...</li>
<li>South Korea prepares stock market stabilization fund after Kospi ...</li>

</ul>
</details>

**Tags**: `#South Korea`, `#market stabilization fund`, `#share buybacks`, `#short-selling rules`, `#Taiwan`

---

<a id="item-finance-news-4"></a>
### [台湾证交所与十家券商达成共识：融资担保维持率下调至120%](https://telegram.me/pelosi3/30391) ⭐️ 7.0/10

据台湾经济日报报道，台湾证券交易所与十家大型券商开会达成共识，将融资担保维持率从130%下调至120%，以缓解台股下跌中融资追缴的压力。会中另一项共识是券商自营部门目前持仓水位偏低、将进场加码。

telegram · pelosi3 · Nov 22, 14:04

**「Background」** The margin maintenance ratio is the minimum collateral cushion brokers require against a margin loan, so cutting it from 130% to 120% gives investors more room before a falling share price triggers a margin call, which is why brokers linked the move to the market&\#x27;s recent over-correction.

**「Who is affected」** If the 120% threshold is formally adopted, it would lower the minimum collateral that margin-financed investors in Taiwan stocks must maintain and ease the margin-call pressure the brokers cited, though the report describes only a meeting consensus, not an implemented rule.

**Tags**: `#台湾股市`, `#融资担保维持率`, `#券商自营`, `#股市稳定基金`, `#市场监管`

---

<a id="item-finance-news-5"></a>
### [Record El Niño warming raises pressure on food aid](https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/) ⭐️ 7.0/10

Central tropical Pacific warming tied to El Niño reached 3.5°C in October, breaking the previous record of about 2.75°C and projected to peak near 4°C in early winter, according to climate scientist Zeke Hausfather. The World Food Programme warned in August that the event could add 49 million acutely food-insecure people by the end of 2027, for a total of 274 million, while global aid funding in 2025 was 30% below its 2022 peak.

telegram · zaihuapd · Nov 22, 14:09

**「Background」** El Niño is a periodic warming of the central tropical Pacific that disrupts rainfall and crop conditions worldwide; this event is forecast to be the strongest on record and, combined with global warming, is expected to push global temperatures to new highs in 2027, according to Nature.

**「Impact」** Households dependent on WFP assistance are already affected: the agency reported in October that funding shortages would cut monthly food support for about 500,000 people in Gaza, while its August projection warned that this El Niño could push an additional 49 million people into acute food insecurity by the end of 2027.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nature.com/articles/d41586-026-02293-y">This El Niño is set to be the largest on record by a ‘mind ...</a></li>
<li><a href="https://www.theclimatebrink.com/p/the-strongest-el-nino-ever">The Strongest El Niño Ever - by Zeke Hausfather</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gaza_Strip_famine">Gaza Strip famine - Wikipedia</a></li>
<li><a href="https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/">How This Year’s Super El Niño Will Worsen Global Hunger | WIRED</a></li>

</ul>
</details>

**Tags**: `#El Niño`, `#food security`, `#humanitarian aid`, `#climate risk`, `#economic impact`

---