---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 105 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [OpenAI 发文讨论困惑度与模型智能](#item-tech-news-1) ⭐️ 7.0/10
2. [英媒指太子集团相关人员参与英伟达芯片对华走私](#item-tech-news-2) ⭐️ 7.0/10
3. [谷歌用 Mirror Dimension 模拟互联网测试 Chrome AI 代理](#item-tech-news-3) ⭐️ 7.0/10
4. [Windows Server 2028 默认不再内置 WoW64](#item-tech-news-4) ⭐️ 7.0/10

**科技博客**
1. [当不确定时，不妨四处乱撞](#item-tech-blog-1) ⭐️ 5.0/10
2. [错误选集：失误如何推动科学](#item-tech-blog-2) ⭐️ 5.0/10
3. [Strata 0.2.18 新增 Hy4-Flash，64GB 内存起步](#item-tech-blog-3) ⭐️ 5.0/10
4. [GTA 6 早期 PC 开源项目 Leonida 的技术进展](#item-tech-blog-4) ⭐️ 4.0/10
5. [TotK Recomp 0.5.0：FSR 3.1 插帧、自由视角与性能优化](#item-tech-blog-5) ⭐️ 4.0/10

**财经新闻**
1. [沪深北交易所下调融资保证金最低比例至 80%](#item-finance-news-1) ⭐️ 8.0/10
2. [美股科技股遭遇大幅抛售，亚洲多地出台稳市措施](#item-finance-news-2) ⭐️ 8.0/10
3. [韩国称可随时动用市场稳定基金 并暂放宽回购限制三个月](#item-finance-news-3) ⭐️ 7.0/10
4. [台湾证交所与十家券商达成共识：融资担保维持率拟由 130%降至 120%](#item-finance-news-4) ⭐️ 7.0/10
5. [超级厄尔尼诺海温破纪录，世界粮食计划署警告粮食不安全加剧](#item-finance-news-5) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI 发文讨论困惑度与模型智能](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI 发布了一篇题为《Perplexity and Intelligence》的文章，讨论困惑度（perplexity）与模型智能之间的关系。该文在 Hacker News 上引发较多讨论，评论集中在交叉熵、基准测试以及推理模型是否改变了这一关系。由于提供的材料中没有文章正文，无法核实文中给出的具体数据、结论或是否提出了新的评估方法。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「背景」** 困惑度衡量模型预测下一个 token 时的不确定程度，数值越低表示预测越确定；交叉熵损失与困惑度之间只差一次指数或对数换算。OpenAI 首席科学家 Jakub Pachocki 在这篇文章中主张，把困惑度（等价地，交叉熵损失）作为比较不同模型开发者的指标，并用于共同的安全标准；Hacker News 讨论中有人批评，文章没有解释熵、对数困惑度和困惑度之间的关系。

**「社区讨论」** 有评论者指出文章没有定义困惑度，并解释它衡量模型预测下一个 token 时的“惊讶程度”：最佳情况为 1，最差情况等于词表大小。另有评论者对交叉熵在强化学习普及后仍与模型能力呈现清晰关联感到意外，并提到 Microsoft 的 Mustafa Suleyman 称 MAI-2 Base 在 OpenAI 评估集上的 log-perplexity 为 0.819，与 GPT-5.6 Sol 基座模型处于同一量级；这属于评论中的转述，尚未在给定材料中独立确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li><a href="https://news.ycombinator.com/item?id=50601525">Perplexity and Intelligence | Hacker News</a></li>

</ul>
</details>

**标签**: `#language models`, `#perplexity`, `#model evaluation`, `#cross-entropy`, `#OpenAI`

---

<a id="item-tech-news-2"></a>
### [英媒指太子集团相关人员参与英伟达芯片对华走私](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 7.0/10

英国《金融时报》援引知情人士称，被美国财政部指为柬埔寨太子集团“二号人物”的胡小伟，涉嫌参与一个将英伟达芯片运入中国的走私网络。报道称，该网络涉及空壳公司、地下融资渠道和私人飞机运输；贸易数据显示，2024 年 12 月至 2025 年 12 月，Megaspeed 马来西亚子公司申报进口货物价值约 46 亿美元，部分芯片据称流入中国黑市。太子集团否认胡小伟曾为其工作，并称有关非法网络和私人飞机走私的指控缺乏事实依据。报道主要依据知情人士和贸易数据，未披露具体芯片型号、数量和最终用户。

telegram · zaihuapd · 11月22日 04:34

**「背景」** 背景是，Megaspeed 已是这轮英伟达芯片走私争议的核心公司之一：11 月 11 日的报道称，这家总部在新加坡的云服务商在东南亚搭建了转运英伟达芯片的网络，其马来西亚子公司 Speedmatrix 在 2024 年 12 月至 2025 年 12 月间申报进口了约 46 亿美元货物，申报对象包括 Aivres。此次 FT 报道的新增点，是把柬埔寨太子集团涉案人员胡小伟与这条网络联系起来；相关说法仍属报道中的指控，太子集团已否认。

<details><summary>参考链接</summary>
<ul>
<li>FT investigation links Alice Huang&#x27;s Megaspeed to a gaming group ...</li>
<li>How Megaspeed built a network in Southeast Asia to move Nvidia ...</li>

</ul>
</details>

**标签**: `#Nvidia`, `#chip smuggling`, `#export controls`, `#AI hardware`, `#supply chain`

---

<a id="item-tech-news-3"></a>
### [谷歌用 Mirror Dimension 模拟互联网测试 Chrome AI 代理](https://www.landian.news/archives/128701.html) ⭐️ 7.0/10

据报道，谷歌为 Chrome 的 AI 代理搭建了一个名为 Mirror Dimension 的模拟互联网，让代理在隔离环境中执行打开网站、搜索浏览、登录、加购和完成任务等操作。蓝点网称，该环境包含数千个模拟网站，每名工程师单独隔离测试，每天运行超过 1000 个测试案例，重点是防御恶意网页的提示词注入攻击。现有信息来自简要的二手报道，未提供谷歌的一手说明，也未说明该系统是否会对外发布。

telegram · zaihuapd · 11月23日 01:30

**「背景」** Chrome 的 AI 代理（Google 称为 auto browse）需要代替用户打开网页、点击和填写表单，因此网页中若藏有恶意指令，就可能引发提示词注入，诱导代理执行并非用户本意的操作。为了在不接触真实网站和账号的情况下复现这类风险，Google 构建了名为 Mirror Dimension 的合成网络，用数千个模拟站点覆盖日常浏览路径，并可在其中预置攻击场景进行测试。

**「影响」** 该报道显示，Chrome AI 代理的测试重点之一是把提示词注入视作主要攻击面；但报道没有披露具体测试方法、通过标准或是否对外开放，外部开发者暂时无法复用这套环境。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/security/mirror-dimension-for-agents/">Mirror Dimension for Agents: Evaluating Browser-Use Agents ...</a></li>
<li><a href="https://explainx.ai/blog/google-mirror-dimension-synthetic-web-chrome-auto-browse-agents-prompt-injection-testing-2026">Google Mirror Dimension: Fake Web for Chrome AI Agents ...</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#Chrome`, `#prompt injection`, `#security testing`, `#browser automation`

---

<a id="item-tech-news-4"></a>
### [Windows Server 2028 默认不再内置 WoW64](https://www.windowslatest.com/2026/11/23/32-bit-apps-days-are-numbered-as-microsoft-strips-support-bit-by-bit-starting-with-windows-server-2028-but-windows-11-is-safe-for-now/) ⭐️ 7.0/10

微软在 Ignite 2026 上表示，Windows Server 2028 将默认不包含 WoW64 兼容子系统，因此系统开箱无法运行 32 位应用；该版本计划于 2027 年秋季与 Windows 11 27H2 一同发布。需要兼容旧应用的管理员可通过“按需功能”（FoD）把 WoW64 装回，在 Server Core 上通常使用 PowerShell 或 DISM 添加。微软称此举意在缩小攻击面、阻止 32 位恶意软件，并明确 Windows 11 目前仍保留 WoW64、尚未公布移除计划。上述安排来自微软在 Ignite 2026 的表态及 Windows Latest 报道，当前条目是二手摘要，部分细节仍待官方文档确认。

telegram · zaihuapd · 11月23日 03:03

**「背景」** WoW64 是 64 位 Windows 中负责运行 32 位 x86 程序的兼容层，它让这些程序无需修改就能在 64 位系统上加载并执行；此前它随系统一并提供，管理员通常不需要单独安装。据 thecommunity.ru 的报道，Windows Server 2028 取消默认预装，意味着 64 位 Windows 首次出现开箱即无法运行 32 位应用的情况。

**「影响」** 对仍依赖 32 位企业应用的组织，部署 Windows Server 2028 前需盘点兼容性，并在系统镜像或部署脚本中通过 FoD 安装 WoW64；若不装回，这些应用将无法启动。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thecommunity.ru/microsoft/windows/server/12123-windows-server-2028-po-umolchaniju-ne-budet-podderzhivat-32-bitnye-prilozhenija.html">Windows Server 2028 по умолчанию не будет поддерживать...</a></li>

</ul>
</details>

**标签**: `#Windows Server 2028`, `#WoW64`, `#32-bit compatibility`, `#Microsoft`, `#enterprise IT`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [当不确定时，不妨四处乱撞](https://seangoedecke.com/when-in-doubt-flail-about/) ⭐️ 5.0/10

rss · Sean Goedecke · 11月23日 00:00

**「背景」** 面对缺乏指引的产品、技术或组织难题，工程师往往倾向先谨慎观察、等看清全貌再行动。作者认为，在不确定的情况下，要理解问题只能通过接触现实来获得，等待反而更慢。

**「方案」** 他的建议是主动「乱撞」：大量尝试不同方案，紧盯同事、专家和现实数据给出的反馈，果断砍掉没有正反馈的方案。多试之所以关键，一是能尽可能多地触碰现实，二是多数想法本就糟糕，十个里或许只有一个可行，三是同时握有多个方案才不会对某一个过度投入。文章给出三类场景：他在 GitHub Models（现已关停）做的大部分功能没有起色，但「用 GitHub Actions token 运行 AI 推理」意外留存，成为 Continuous AI 的种子；面对过于复杂的大型系统，与其通读全貌，不如先做几个试探性改动看结果，AI agent 让批量产出重构方案更容易；组织问题中，当团队互不沟通或不满原因无人说得清时，只能尝试自动化、主动接手、提长期计划等，多数无用但显示在努力。风险是声誉：乱撞不当会被视为只会出馊主意的人，组织场景下忽视反馈、硬推失败方案，不满会转向你；及时放弃反而能建立信任。作者提醒，从内部看这确实像反复失败，但这种不适应被当作积极信号。

**「启示」** 信息不足时，与其等待确定性，不如用低成本试探换取真实反馈；只要对反馈敏感并随时放弃无效方案，「乱撞」就是快速变得有用的方式。

**标签**: `#engineering-career`, `#decision-making`, `#experimentation`, `#software-engineering`, `#organizational-dynamics`

---

<a id="item-tech-blog-2"></a>
### [错误选集：失误如何推动科学](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196917) ⭐️ 5.0/10

rss · Dapenti Xilei · 11月23日 00:01

**「背景」** 科学突破常被叙述为一连串天才的正确决定，但真实研究充满零结果、认知盲点和操作失误。文章借《Nature》对五位资深科学家的访谈，主张科研与工程的关键不是“不犯错”，而是建立容错与自纠错机制。

**「方案」** 作者用五个案例展开：LIGO 的彼得·肖汉团队在 2015 年首次探测引力波前发表约 100 篇“零结果”论文划定排除边界，而一次盲注入测试暴露出天空定位偏差，团队一天内定位到镜片运动方向镜像错误。奥马尔·亚基曾因确认偏误轻视学生提出的金属有机化合物，学生坚持一年找到稳定化学键，最终开辟 MOFs；研究者安吉拉·麦克唐纳则拒绝删除与假设冲突的离群基因数据，两年后野外调查确认那其实是新物种 Solanum nectarifolium。凯瑟琳·巴德格利在全球哺乳动物化石数据库膨胀后发现非洲与北美气候空间几乎不重叠，通用模型不成立，遂顶住沉没成本取消出版合同。另一个固氮实验因临时工把根瘤“平均分摊”而毁掉一组重复，但随机区组设计保住前四组并仍得出显著结论，说明核心工作不应外包给未受训练者，容错须在架构初期预留。

**「启示」** 这些案例共同说明，科学进步并非无错的直线，而是试错、反馈与修正的迭代。真正可迁移的能力，是让错误尽早暴露、让系统在人为失误中仍能幸存。

**标签**: `#科学方法论`, `#科研失误`, `#容错设计`, `#科普综述`, `#案例分析`

---

<a id="item-tech-blog-3"></a>
### [Strata 0.2.18 新增 Hy4-Flash，64GB 内存起步](https://www.appinn.com/strata-0-2-18/) ⭐️ 5.0/10

rss · Appinn · 11月22日 07:06

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/strata-0-2-18/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;Strata 是面向家用电脑的本地大模型运行工具，0.2.18 于 11 月 22 日加入腾讯 Hy4-Flash 原生支持，桌面版、命令行及推理和控制组件同步更新。Hy4-Flash 是总参数 224B、每 Token 激活约 12B 的 MoE 模型，支持图像理解与最高 100 万 Token 上下文，但官方起步内存升至 64GiB，使现有机器能否运行成为核心问题。

**「方案」** Strata 为此新增独立 strata-hy4 引擎、SQ-64、SQ-96、SQ-128 三档量化和 DFly2 推测解码；三档磁盘占用分别约 129.61GB、157.16GB、181.23GB，对应 64、96、128GiB 系统内存，SQ-64 还可搭配 8、12 或 16GiB 显存，另可加载 0.93GB 的 Vision 组件。升级会保留原有 Qwen 和 DeepSeek 模型、聊天记录与设置。作者引用腾讯 Hy4-Flash 模型卡称，Hy4-Flash 在三项 Agent 测试中领先，例如 OSWorld 2.1 部分得分为 68.1 对 58.8；Qwen3.8-Flash-Next 则在三项编程和终端测试中更高，Terminal-Bench 4.0 为 19.2 对 29.5，DeepSWE v1.1 仅差 0.5 分。这些对比由厂商各取最高推理档位，并非独立复现。作者据此建议，内存不足 64GB 继续用 Qwen 更实际，96GiB 或 128GiB 用户再按任务尝试 Hy4-Flash；即使配 24GB 显存的 RTX 3090，48GB 系统内存仍低于 SQ-64 的官方起步要求。

**「启示」** 作者的结论是：Hy4-Flash 在 Agent 类任务上更有吸引力，但 64GiB 内存与大容量磁盘把多数现有本地部署挡在门外；在门槛降低前，Qwen 仍是普通配置更现实的选择。

**标签**: `#本地大模型`, `#Strata`, `#Hy4-Flash`, `#量化部署`, `#基准评测`

---

<a id="item-tech-blog-4"></a>
### [GTA 6 早期 PC 开源项目 Leonida 的技术进展](https://www.appinn.com/gta-6-pc-port-leonida/) ⭐️ 4.0/10

rss · Appinn · 11月22日 13:26

**「背景」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/gta-6-pc-port-leonida/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;《GTA 6》尚未推出官方 PC 版，已有开发者尝试用静态重编译让 Xbox Series 版直接在 Windows 上原生运行，而不是走模拟器路线。项目名为 Leonida，作者明确标注它仍处于极早期，尚不能启动游戏。

**「方案」** 文章介绍，Leonida 利用 Xbox Series 与现代 PC 同为 x86-64 架构的共性，计划在 PC 上直接加载并执行游戏的 CPU 代码，同时重新实现 Xbox 系统调用、内存管理、图形、音频和运行时依赖。除 CPU 代码外，主要难点之一是把 Xbox 的 GPU 着色器转换成 PC 图形接口可理解的格式。按 README，项目已识别 Xbox 游戏文件格式，转换 26,503 个 GPU Shader 并通过 SPIR-V 静态验证，能导出模型、纹理和音频等资源（部分格式仍待处理），也开始开发系统接口兼容层并研究 D3D12 到 Vulkan 的转换。不过，当前加载器只能运行替代测试程序，游戏可执行文件尚未完成测试，也没有展示真正进入《GTA 6》的画面。项目不提供游戏文件，作者称没有可正常游玩的版本，也没有明确完成时间，因此它更像一份有实际里程碑的路线图，而非可用的 PC 移植。

**「启示」** 作者的核心判断是：Leonida 以具体进展证明了静态重编译处理封闭主机游戏二进制的可行性，但离可玩仍很远；其意义目前主要在于为移植、模拟器和静态重编译技术观察者提供早期样本。

**标签**: `#static recompilation`, `#GTA 6`, `#Xbox Series`, `#game porting`, `#shader translation`

---

<a id="item-tech-blog-5"></a>
### [TotK Recomp 0.5.0：FSR 3.1 插帧、自由视角与性能优化](https://www.appinn.com/totk-recomp-0-5-0/) ⭐️ 4.0/10

rss · Appinn · 11月22日 07:37

**「背景」** TotK Recomp 是一个把《塞尔达传说：王国之泪》以原生方式移植到 Windows 与 Linux 的项目，v0.5.0 更新同时补上了画面与操作层面的多项功能，并继续做性能优化。

**「方案」** 据作者介绍，新版内置 AMD FSR 3.1 超分辨率与 FSR 3 帧生成，覆盖 NVIDIA、AMD、Intel 显卡且无需额外插件；帧生成在两条真实画面之间插入一帧，使显示帧率接近翻倍（例如渲染 60 FPS 可输出接近 120 FPS），超分则用于改善 GPU 受限场景的帧率以及草地、电线等细节的闪烁。两项功能默认关闭，开发者建议实际渲染帧率达到 60 FPS 后再开启插帧，以避免增加输入延迟和画面瑕疵。功能上还加入了可以离开林克自由取景的自由视角、按 F6 存档与 F7 读档且不影响手动存档的快速存档（这两项需游戏版本 1.4.3）、PlayStation 手柄按键提示，以及兼容更多代码插件并能查看 Mod 冲突的 Mod 支持。性能方面，作者转述开发者的测试结果：Windows PGO 编译优化带来约 6%~12% 的 FPS 提升，sync\_ahead 优化在 GTX 1050 Ti 上提升约 6%~10%，barrier\_merge 让 RX 7900 XT 在瀑布场景从 82 FPS 升到 141 FPS；同时修复了 AMD 显卡运行一段时间后掉帧、水面闪烁、阴影异常，以及高帧率下部分神庙机关失效等问题。升级只需运行新版安装程序并指向原来的游戏目录，游戏文件、存档和配置都会保留，安装程序仅重新生成可执行文件与着色器缓存。文章属于更新日志式的复述，没有展开这些优化的实现原理，上述数字均出自开发者、未经独立验证。

**「启示」** 对已经跟进该项目的人来说，0.5.0 的意义在于一次性补齐插帧、自由视角等常用能力并顺带提速；但性能数字仍属开发者自测，帧生成带来的延迟代价也需要玩家以 60 FPS 渲染帧率为底线自行权衡。

**标签**: `#release notes`, `#game recompilation`, `#frame generation`, `#FSR upscaling`, `#PC performance tuning`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [沪深北交易所下调融资保证金最低比例至 80%](https://news.rthk.hk/rthk/ch/component/k2/1878864-20261123.htm) ⭐️ 8.0/10

上海、深圳和北京证券交易所宣布自 11 月 30 日起，将投资者融资买入证券的最低保证金比例由 100%下调至 80%；《上海证券报》引述业内测算称，此举有望释放 4000 亿元人民币增量资金。

rss · RTHK Finance · 11月22日 22:22

**「背景」** 融资保证金比例是投资者融资买入证券时必须自有资金所占的最低比例；经中证监批准，本次将该下限由 100%降至 80%，自 11 月 30 日起施行，因此同等自有资金可支撑更大融资买入规模。

**「谁受影响」** 对使用融资（借钱买股）的投资者来说，最低保证金比例从 100%降至 80%，意味着同一笔自有资金可以支撑更大的持仓；同期沪深交易所推出的免收交易单元使用费、减免数据中心服务费等降费措施，则直接降低券商和投资者的交易与数据服务成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://money18.on.cc/mobile/finnews/content/exp/bkn-20261122185844351-1122_00842_001.html">中国救 市 ！ 沪 深 北 交 所 下 调 融 资 保 证 金 比 例 至 80 % | 东网 Money18</a></li>

</ul>
</details>

**标签**: `#融资保证金`, `#交易所政策`, `#市场流动性`, `#降费`, `#创业板做市商`

---

<a id="item-finance-news-2"></a>
### [美股科技股遭遇大幅抛售，亚洲多地出台稳市措施](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

美国 AI 科技股周五遭遇大规模抛售，纳斯达克指数单日下跌 5.28%，费城半导体指数重挫近 11%；随后中国内地、韩国和中国台湾地区相继推出下调融资保证金比例、放宽回购限制和收紧卖空规则等稳市措施。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 中国内地此次将融资保证金最低比例（投资者借钱买股票所需自有资金比例）从 100%下调至 80%，逆转了今年 1 月为控制杠杆而实施的上调，新规将于 11 月 30 日生效。

**「影响」** 据彭博报道，市场对人工智能交易可持续性的担忧，正使新兴市场股市面临回吐今年全部涨幅的风险；对亚洲半导体出口企业和重仓科技股的投资者来说，这意味着估值与融资两方面都承受压力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://uecn.org/china-eases-margin-financing-requirements-to-80-amid-regional-stock-rescue-measures/">China Eases Margin Financing Requirements to 80% Amid ...</a></li>
<li><a href="https://www.investmentwatchblog.com/asian-governments-are-stepping-in-to-prop-up-stock-markets-taiwan-is-restricting-short-selling-china-is-making-it-easier-to-borrow-south-korea-is-preparing-a-rescue-fund/">Asian governments are stepping in to prop up stock markets ...</a></li>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-23/emerging-market-stocks-set-to-erase-2026-gains-on-ai-selloff">Emerging-Market Stocks Slide as AI Selloff Wipes Out 2026 ...</a></li>

</ul>
</details>

**标签**: `#US tech selloff`, `#semiconductor stocks`, `#Asian market stabilization`, `#short-selling rules`, `#margin financing`

---

<a id="item-finance-news-3"></a>
### [韩国称可随时动用市场稳定基金 并暂放宽回购限制三个月](https://news.rthk.hk/rthk/ch/component/k2/1878865-20261123.htm) ⭐️ 7.0/10

韩国财政经济部周日（11 月 22 日）表示，如果市场状况继续恶化，将随时准备启动证券市场稳定基金。与会官员同时同意暂时放宽上市公司股票回购的每日额度限制，为期 3 个月，并密切监控杠杆投资与追缴保证金情况、严厉打击非法卖空。

rss · RTHK Finance · 11月22日 22:23

**「背景」** 韩国股市稳定基金是由金融机构及韩国交易所等出资、用于在股市流动性不足时买入 KOSPI 200 等指数产品的政策工具，上一次动用是在 2008 年金融危机期间。

**「影响」** 韩国上市公司可在三个月内以更高每日额度回购股票，杠杆投资者则会受到更严密的保证金追缴监控。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.biggo.com/news/41704fd7-7d88-4cb6-8773-17f6b6f5c964">South Korea Restarts Stock Market Stabilization Fund ...</a></li>
<li><a href="https://aistockwire.com/blog/korea-stock-market-stabilization-fund-first-since-2008-kospi-november-2026">Korea readies stock stabilization fund, last used in 2008</a></li>
<li>South Korea readies its market stabilization fund and Taiwan bans ...</li>
<li>South Korea prepares stock market stabilization fund after Kospi ...</li>

</ul>
</details>

**标签**: `#South Korea`, `#market stabilization fund`, `#share buybacks`, `#short-selling rules`, `#Taiwan`

---

<a id="item-finance-news-4"></a>
### [台湾证交所与十家券商达成共识：融资担保维持率拟由 130%降至 120%](https://telegram.me/pelosi3/30391) ⭐️ 7.0/10

据台湾经济日报报道，台湾证交所今日邀请十家大型券商开会，达成将融资担保维持率从 130%降至 120%的共识，券商认为这一降幅在自身风险可承受范围内，也能缓解股民在台股下跌中的融资追缴压力。会议另达成两点共识：券商自营部门目前持仓水位很低，将会进场加码；现行规模 5000 亿元的股市稳定基金太小，不足以发挥护市功能，券商主张扩大规模。上述内容均为会议共识，尚非正式实施细节。

telegram · pelosi3 · 11月22日 14:04

**「背景」** 融资担保维持率是投资人借钱买股（融资）时，担保品市值相对融资金额的最低比率，低于门槛，券商就会要求补缴保证金，否则强制卖出股票。台股此前下跌，使不少融资账户逼近这一门槛，券商因此提出把维持率从 130%降到 120%，以减轻追缴压力。

**「影响」** 使用融资交易的台湾散户将因担保维持率从 130%降至 120%而减少追缴保证金压力，但券商指出，在股市稳定基金仅 5000 亿元规模的情况下，能否带来强力买盘仍存疑。

**标签**: `#台湾股市`, `#融资担保维持率`, `#券商自营`, `#股市稳定基金`, `#市场监管`

---

<a id="item-finance-news-5"></a>
### [超级厄尔尼诺海温破纪录，世界粮食计划署警告粮食不安全加剧](https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/) ⭐️ 7.0/10

气候学家齐克·豪斯法特称，截至 10 月，衡量厄尔尼诺强度的中热带太平洋升温已达 3.5℃，打破此前约 2.75℃的纪录，并预计在初冬升至约 4℃的峰值；世界粮食计划署 8 月警告，这可能到 2027 年底新增 4900 万急性粮食不安全人口，使总数达到 2.74 亿。

telegram · zaihuapd · 11月22日 14:09

**「背景」** 厄尔尼诺是赤道太平洋海水异常升温、会扰乱全球天气的气候现象；本轮之前的强度纪录约为 2.75℃，出现在 2015—16 年。

**「受影响群体」** 依赖粮食援助的家庭将直接承压：世界粮食计划署预计到 2027 年底新增 4900 万急性粮食不安全人口，而援助资金收紧正迫使其削减覆盖，例如加沙约 50 万人将失去月度食品支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theclimatebrink.com/p/the-strongest-el-nino-ever">The Strongest El Niño Ever - by Zeke Hausfather</a></li>
<li><a href="https://en.wikipedia.org/wiki/Gaza_Strip_famine">Gaza Strip famine - Wikipedia</a></li>
<li><a href="https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/">How This Year’s Super El Niño Will Worsen Global Hunger | WIRED</a></li>

</ul>
</details>

**标签**: `#El Niño`, `#food security`, `#humanitarian aid`, `#climate risk`, `#economic impact`

---