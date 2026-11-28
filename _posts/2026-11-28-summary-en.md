---
layout: default
title: "Horizon Summary: 2026-11-28 (EN)"
date: 2026-11-28
lang: en
---

> From 129 items, 22 important content pieces were selected

---

**Technology News**
1. [Google Research claims DeepCrossAttention is up to 3x faster](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenSec discloses 9.8-severity pre-auth Linux NFS server root flaw](#item-tech-news-2) ⭐️ 8.0/10
3. [Card-skimming scripts reportedly use WebRTC to exfiltrate payment data](#item-tech-news-3) ⭐️ 7.0/10
4. [State AGs sue SpaceX over Grok generating sexual abuse, intimate images](#item-tech-news-4) ⭐️ 7.0/10
5. [Essay on false computer-checked proofs argues for stronger assurance](#item-tech-news-5) ⭐️ 7.0/10
6. [SemiAnalysis Reports Trainium3 Cost Edge Over GB300 in Inference Benchmarks](#item-tech-news-6) ⭐️ 7.0/10
7. [Intel Pressed to Give Trump Administration 10% Stake, Lawsuit Notes Say](#item-tech-news-7) ⭐️ 7.0/10
8. [Minecraft Bedrock resource-pack flaw hits 26.52–26.63; 26.65 fixes it](#item-tech-news-8) ⭐️ 7.0/10
9. [Microsoft expands Windows built-in drivers, starting with printing](#item-tech-news-9) ⭐️ 7.0/10

**Technology Blog**
1. [What a Self-Built Audiobook Desk Taught About Iteration](#item-tech-blog-1) ⭐️ 5.0/10
2. [Six Years of Hard Drive Prices: 110 to Nearly 200 Yuan per TB](#item-tech-blog-2) ⭐️ 5.0/10
3. [Coruna and DarkSword: Web-Only Exploits Hit Old iPhones](#item-tech-blog-3) ⭐️ 4.0/10
4. [NodeWarden Update: Offline PWA, Backups and Multi-User on Cloudflare](#item-tech-blog-4) ⭐️ 4.0/10

**Financial News**
1. [China&\#x27;s State Council pledges stronger &\#x27;national team&\#x27; support for stock market, better Central Huijin stabilization fund](#item-finance-news-1) ⭐️ 8.0/10
2. [S&amp;P 500 enters correction, 11.6% below October record](#item-finance-news-2) ⭐️ 7.0/10
3. [BBC: Energy bills to rise 26% in January after gas price surge](#item-finance-news-3) ⭐️ 7.0/10
4. [中國人民銀行承諾靈活運用貨幣政策工具以維護流動性](#item-finance-news-4) ⭐️ 7.0/10
5. [Meituan swings to Q3 net profit of RMB 2.07 billion as revenue rises 22%](#item-finance-news-5) ⭐️ 7.0/10
6. [Hong Kong Stocks Climb 467 Points as Tech Index Jumps Over 6%](#item-finance-news-6) ⭐️ 7.0/10
7. [China regulators pledge to boost long-term funds in capital market, tighten shareholder and delisting rules](#item-finance-news-7) ⭐️ 7.0/10
8. [Chinese stocks surge after State Council signals market stabilization](#item-finance-news-8) ⭐️ 7.0/10
9. [PBOC Halves Large-Denomination CD Purchase Thresholds, Effective March 2027](#item-finance-news-9) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Google Research claims DeepCrossAttention is up to 3x faster](https://research.google/blog/supercharging-transformer-residual-connections/) ⭐️ 8.0/10

Google Research says its DeepCrossAttention technique for transformer residual connections and attention achieves comparable model quality while running up to 3x faster. The announcement is a research claim, not evidence of a shipped product, and the supplied material provides no implementation details or independent validation. It is relevant to developers and researchers working on transformer efficiency, but the speedup and quality results remain unverified outside the source.

hackernews · ComputedCamp995 · Nov 27, 23:06 · [Discussion](https://news.ycombinator.com/item?id=50672565)

**「Background」** DeepCrossAttention targets the residual connections that carry information between transformer layers; with standard fixed residual links, earlier layer outputs can be diluted as depth increases. The method instead uses learnable, input-dependent weights and depth-wise cross-attention to combine outputs from previous layers, letting the model focus on the most relevant earlier information. A preprint describing the approach appeared on arXiv in February 2025, and Google Research has now published a blog post on it.

**「Implementation impact」** For teams evaluating DCA, adoption is an architectural change: it replaces fixed residual sums with learnable, per-token depth-wise cross-attention over earlier layers, so it requires modifying and training a transformer rather than toggling an existing inference setting. The claimed up-to-3x speedup remains a Google research result in the supplied material, so teams should benchmark it on their own workloads before planning capacity around it.

**「Community discussion」** Commenters questioned the presentation and practical gains: one argued the comparison should use bar charts rather than line graphs because the methods have no temporal relationship, while another asked whether the claimed speedup would stack with existing MTP and Dflash optimizations.

<details><summary>References</summary>
<ul>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections - Google Research</a></li>
<li><a href="https://arxiv.org/abs/2502.06785">[2502.06785] DeepCrossAttention: Supercharging Transformer ...</a></li>
<li><a href="https://explainx.ai/blog/google-deepcrossattention-transformer-residual-connections-2026">DeepCrossAttention (DCA): Google Fix for Deep Transformers ...</a></li>
<li><a href="https://research.google/blog/supercharging-transformer-residual-connections/">Supercharging transformer residual connections - Google Research</a></li>

</ul>
</details>

**Tags**: `#transformer efficiency`, `#attention mechanisms`, `#Google Research`, `#model optimization`, `#AI infrastructure`

---

<a id="item-tech-news-2"></a>
### [OpenSec discloses 9.8-severity pre-auth Linux NFS server root flaw](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

OpenSec disclosed CVE-2026-99362, a pre-authentication heap overflow in the Linux kernel&\#x27;s nfsd server rated CVSS 9.8, which it says can give an unauthenticated attacker root on hosts with NFSv4.1 or 4.2 enabled via a single connection to tcp/2049. The flaw has existed since Linux 3.16 \(2014\) and affects file servers, NAS devices and cluster storage nodes, according to the disclosure. Fixes are in Linux 6.12.117, 6.18.61, 7.3.2 and 7.4-rc1; applying them requires a kernel upgrade and reboot, while systems that cannot be upgraded immediately should restrict access to tcp/2049. The CVE was made public on November 20, 2026; the disclosure did not include exploit details and has not been independently confirmed.

telegram · zaihuapd · Nov 27, 12:57

**「How the nfsd reply-cache flaw works」** The flaw sits in nfsd&\#x27;s NFSv4.1/4.2 session reply cache, which stores responses so retransmitted requests can be answered without redoing work. According to Red Hat&\#x27;s advisory, a remote client can negotiate a minimal cached reply size and then send crafted compound requests containing SEQUENCE operations, causing an out-of-bounds write; OpenSec&\#x27;s analysis describes the same setup as shrinking the reply cache to nothing before the server copies a full reply into it. Because this path is reachable before authentication on hosts exposing TCP port 2049, the bug is pre-auth rather than requiring an NFS login.

**「Operational impact」** Administrators of NFSv4.1/4.2 servers should treat tcp/2049 as untrusted until the host is running one of the fixed kernels and has been rebooted; installing the kernel package without restarting leaves the vulnerable nfsd code running. Where an immediate reboot is not possible, restricting tcp/2049 to trusted clients is the interim containment measure, and Red Hat&\#x27;s record confirms the flaw is remotely triggerable through crafted NFS compound requests.

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://rokkhe.hashnode.dev/nfs2root-cve-2026-99362-linux-nfsd">NFS2ROOT (CVE-2026-99362): what it is, who is exposed, and ...</a></li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://computingforgeeks.com/nfs2root-cve-2026-99362/">NFS2ROOT (CVE-2026-99362): Check, Patch, Mitigate ...</a></li>

</ul>
</details>

**Tags**: `#Linux kernel`, `#NFS`, `#security vulnerability`, `#CVE-2026-99362`, `#privilege escalation`

---

<a id="item-tech-news-3"></a>
### [Card-skimming scripts reportedly use WebRTC to exfiltrate payment data](https://www.infohawk.com/news/2026-11-27-black-friday-webrtc-skimmer) ⭐️ 7.0/10

A report published on Black Friday \(27 November 2026\) says credit-card skimming scripts found on popular shopping sites are using WebRTC to send stolen payment data out, a channel the report describes as evading common monitoring. The scripts are described as Magecart-style injections, and the write-up frames the WebRTC use as an evasion tactic rather than a flaw in WebRTC itself. No technical detail — such as affected sites, script names, indicators of compromise, or the volume of exposed transactions — was available in the supplied material, so the scope of the campaign remains unconfirmed. The item drew substantial discussion on Hacker News, with commenters debating third-party script risk and ad blocking.

hackernews · scanr · Nov 27, 15:40 · [Discussion](https://news.ycombinator.com/item?id=50668145)

**「How Magecart skimming works」** Magecart-style attacks work by injecting a card-skimming script into an e-commerce site, typically capturing payment details as shoppers type them into checkout forms. Such skimmers have conventionally sent stolen data out over HTTP requests, a channel that Content-Security-Policy rules and network monitoring can restrict or observe. A LinkedIn post describing the WebRTC variant states that its DataChannels operate outside HTTP/S and CSP controls, which is what lets the skimmer both receive its payload and exfiltrate card numbers from the browser.

**「Impact」** The practical concern for merchants is that payment-page monitoring focused on conventional outbound HTTP requests may not surface exfiltration over WebRTC data channels, so sites that embed third-party scripts — analytics, chat widgets, A/B testing, payment tags — should treat those tags as part of the cardholder-data environment and audit or restrict them. Commenters noted the technique does not depend on a WebRTC-specific weakness; the same data could leave via ordinary requests, which means blocking one channel alone is not a fix.

**「Community Discussion」** Commenters pushed back on the framing: one argued the story is not about WebRTC&\#x27;s capabilities at all but about it being less frequently monitored, adding that simple HTTP requests would work equally well and that embedding third-party scripts keeps a site vulnerable. Others used the thread to argue for sandboxing or rendering-only treatment of ad and third-party JavaScript, and one questioned why payment systems still rely on symmetric secrets — a design critique offered as opinion, not evidence about this campaign.

<details><summary>References</summary>
<ul>
<li><a href="https://www.linkedin.com/posts/write2nishan_webrtc-skimmer-bypasses-csp-to-steal-payment-activity-7443480737682526208-kq-S">WebRTC Skimmer Bypasses CSP to Steal Payment Data | LinkedIn</a></li>
<li><a href="https://www.akamai.com/glossary/what-is-magecart">What Is Magecart ? | Akamai</a></li>
<li><a href="https://www.retailtouchpoints.com/executive-viewpoints/magecart-meet-the-cybercriminals-silently-stealing-payment-data-from-websites/99630/">Magecart : Meet the Cybercriminals Silently... - Retail TouchPoints</a></li>

</ul>
</details>

**Tags**: `#web security`, `#credit card skimming`, `#WebRTC`, `#third-party scripts`, `#e-commerce`

---

<a id="item-tech-news-4"></a>
### [State AGs sue SpaceX over Grok generating sexual abuse, intimate images](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

Two state attorneys general, identified in the announcement as Jones and Rayfield, filed suit against SpaceX — which the release describes as the parent company of X, xAI and Grok — alleging that the Grok AI system generated child sexual abuse material and non-consensual intimate images and that the companies promoted the creation of such content. The action is announced in a press release on the Virginia attorney general&\#x27;s website, posted in late November 2026. The material available provides no case number, court, specific legal claims, or requested relief, and the allegations have not been adjudicated. It is therefore unclear from the release alone whether the claims target model training, output filtering, or distribution of generated images on X, and no company response is included.

hackernews · DeepLogin · Nov 27, 19:42 · [Discussion](https://news.ycombinator.com/item?id=50670855)

**「Context」** Grok is xAI&\#x27;s AI system, and the release&\#x27;s framing places xAI and X alongside Grok under SpaceX as parent — which is what makes corporate structure part of the dispute rather than just model behavior. Because the announcement is a filing notice rather than a technical account, the specific mechanism by which the images were allegedly produced has not been established.

**「What it means」** Nothing in the release indicates that a court has issued an injunction or that any new obligation has taken effect, so Grok&\#x27;s current behavior and any developer use of xAI&\#x27;s tools are unchanged for now. The practical stake for users and developers is that the guardrails on Grok&\#x27;s image generation are now the subject of litigation, and any eventual injunction or settlement would alter what the product will produce.

**「From the comments」** One commenter asked whether Grok required deliberate tricking to produce this material or was simply permissive by default, and another asked why the users requesting the images are not the focus. A third argued that liability should fall on those individuals and asserted that the U.S. Supreme Court has protected AI-generated abuse material made for personal consumption, with a carve-out barring depictions of real children — an uncited characterization in the thread that the release does not address.

**Tags**: `#AI safety`, `#content moderation`, `#generative AI`, `#legal/regulation`, `#xAI/Grok`

---

<a id="item-tech-news-5"></a>
### [Essay on false computer-checked proofs argues for stronger assurance](https://cr.yp.to/proofs/falseccp.html) ⭐️ 7.0/10

An essay titled “False computer-checked proofs,” published at cr.yp.to, argues for greater assurance in formal verification and has drawn debate among proof-assistant users about how much trust computer-checked results deserve. It is an argument piece rather than a report of a specific new verification failure or a shipped tool change, and the full essay text is not included in the supplied material. In the supplied comments, Lean is described as having had soundness bugs, while Metamath’s set.mm and iset.mm are described as requiring proofs to pass five independently created verifiers in five programming languages.

hackernews · \_tk\_ · Nov 27, 15:26 · [Discussion](https://news.ycombinator.com/item?id=50667989)

**「Background」** Proof assistants rely on a small trusted kernel to check each proof step, so a kernel soundness bug can let a false theorem—or even a proof of False—be accepted as verified. In 2026, Lean 4 disclosed such a kernel bug, CVE-2026-72844, and an independent Rust checker, nanoda, separately failed to catch an invalid proof because of an unrelated projection-node bug.

**「Practical consequence」** Teams relying on proof assistants such as Lean should treat a successful kernel check as one layer of assurance, not an absolute guarantee. Independent replay by separate checkers—such as nanoda, con-leche, and con-ron—is the concrete mitigation available for catching a single verifier&\#x27;s soundness bug before downstream code or proofs depend on the result, and projects that require multiple independent verifiers raise that bar substantially.

**「Community discussion」** twotwotwo and dwheeler disputed the implication that one incorrect verification is easy to sustain, arguing that independent verifiers and informal review mean a successful deception would require multiple failures. gr\_norm called further high-assurance work worthwhile but said existing soundness bugs are rare enough for most software, while andai raised the separate problem of proving an implementation against a mistaken specification.

<details><summary>References</summary>
<ul>
<li><a href="https://aitoolly.com/ai-news/article/2026-08-02-lean-kernel-soundness-bug-14576-postmortem-of-the-ai-assisted-collatz-conjecture-disproof-and-fix">Lean Kernel Bug #14576: Postmortem and Technical Analysis | AIToolly</a></li>
<li><a href="https://www.openwall.com/lists/oss-security/2026/10/26/2">oss-security - CVE-2026-72844: Lean 4 kernel soundness bug ...</a></li>
<li><a href="https://mathoverflow.net/questions/518109/after-the-lean-verification-of-the-riemann-hypothesis-proof-what-residual-trust">computer science - After the Lean verification of the... - MathOverflow</a></li>

</ul>
</details>

**Tags**: `#formal verification`, `#proof assistants`, `#soundness`, `#Lean`, `#Metamath`

---

<a id="item-tech-news-6"></a>
### [SemiAnalysis Reports Trainium3 Cost Edge Over GB300 in Inference Benchmarks](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

SemiAnalysis published a Trainium3 deep dive and InferenceX/UBenchX results, reporting that Trainium3 running with PDS and vLLM achieves better performance per dollar of total cost of ownership than every accelerator tested except Nvidia&\#x27;s Vera Rubin across the throughput-versus-p90-interactivity curve. The firm says Trainium3 trades blows with, or beats, Nvidia GB300 on cost to generate tokens, and that its Descriptor Generation Engines \(DGE\), the counterpart to Nvidia TMA and AMD MI455X TDM, reach peak HBM bandwidth utilization at message sizes where Nvidia GPUs cannot. The microbenchmarks cover SRAM scratchpad \(SBUF-to-PSUM\) latency and bandwidth, rack-scale bandwidth and latency, attention exponentials, and shape-dependent latency including attention head\_dim effects. The article says AWS Annapurna Labs staff helped validate the experiments, but the supplied excerpt contains no absolute benchmark numbers, and the results are SemiAnalysis&\#x27;s own measurements rather than an AWS product announcement.

rss · Semianalysis · Nov 27, 15:54

**「Background」** InferenceX, the benchmark SemiAnalysis uses for this comparison, launched in October 2025 as InferenceMAX and continuously measures LLM inference performance across accelerators and serving software. Trainium3 is AWS&\#x27;s third-generation in-house AI accelerator, and SemiAnalysis frames it against Nvidia&\#x27;s GPU lineage, which added Tensor Cores in Volta, TMA in Hopper, and Tensor Memory in Blackwell.

**「Impact」** For teams comparing inference hardware, the operative metric here is total cost per generated token on a replayed agentic coding workload, not raw accelerator throughput, and SemiAnalysis reports that Trainium3&\#x27;s advantage holds across the latency-throughput frontier when using PDS and vLLM. Because that result depends on a specific serving stack and workload shape, readers evaluating Trainium3 should confirm that their own software stack and traffic patterns match the tested configuration; the excerpt provides no absolute figures or methodology detail beyond the list of microbenchmarks.

<details><summary>References</summary>
<ul>
<li><a href="https://aiwiki.ai/wiki/inferencex">InferenceX | AI Wiki</a></li>

</ul>
</details>

**Tags**: `#AWS Trainium`, `#AI accelerators`, `#inference`, `#microarchitecture`, `#Nvidia`

---

<a id="item-tech-news-7"></a>
### [Intel Pressed to Give Trump Administration 10% Stake, Lawsuit Notes Say](https://arstechnica.com/tech-policy/2026/11/intel-faced-a-choice-give-trump-10-or-face-the-consequences/) ⭐️ 7.0/10

Intel reportedly faced pressure from the Trump administration to give the US government a 10% stake, according to internal notes from an August 2025 call cited in a federal lawsuit. Commerce Department lawyer David Shapiro told Intel’s CFO that the board could reject the offer, but warned that “rejection will have consequences that \[Shapiro\] cannot predict,” and said the president expected to announce a deal on Friday. The excerpt does not say whether Intel accepted the terms or how the litigation characterizes them.

rss · Ars Technica · Nov 27, 12:05

**「Background」** The reported August 2025 demand came amid a broader push by the Trump administration to take ownership stakes in private companies. A New York Times report from November 2025 described the government as spending billions on such stakes, citing Intel among the firms and putting the total at “$10 billion and counting,” while calling the practice unusual and showing no sign of slowing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>

</ul>
</details>

**Tags**: `#Intel`, `#semiconductor industry`, `#US tech policy`, `#government intervention`, `#corporate governance`

---

<a id="item-tech-news-8"></a>
### [Minecraft Bedrock resource-pack flaw hits 26.52–26.63; 26.65 fixes it](https://www.zaikei.co.jp/article/20261119/878386.html) ⭐️ 7.0/10

A publicly disclosed Minecraft Bedrock Edition resource-pack flaw let packs containing content.zipe files modify Ore UI files and run hidden scripts in versions 26.52 through 26.63, according to add-on developer 8Crafter, who said earlier versions may also be affected. The issue affects PC, mobile, and consoles but not Java Edition; players joining servers or Realms with automatic resource-pack downloads could receive the files without manually installing them. Reported exploit paths include deleting all saves, obtaining a player&\#x27;s IP, and, on Windows under specific conditions, silently opening arbitrary URIs or launching a batch file from the pack to download malware. Mojang fixed the flaw in version 26.65; AxmBro&\#x27;s Windows-only read-only detection tool can find content.zipe files but cannot determine whether a pack is malicious.

telegram · zaihuapd · Nov 27, 18:04

**「Background」** Ore UI is the interface framework used by Minecraft Bedrock Edition, and resource packs can replace client-side assets that the game loads for menus and in-game screens. Bedrock servers and Realms can also offer resource packs for automatic download when a player joins, so a crafted pack can reach players who never installed it manually.

**「Impact」** Players and server operators on affected Bedrock versions should move to 26.65 rather than rely on manual resource-pack review, because automatic downloads can deliver a problem pack and the available detector only flags content.zipe files without judging whether they are malicious.

<details><summary>References</summary>
<ul>
<li>Minecraft Bedrock Malware Flaw: Update, Scan, Back Up</li>

</ul>
</details>

**Tags**: `#Minecraft Bedrock`, `#security vulnerability`, `#resource packs`, `#game security`, `#patch release`

---

<a id="item-tech-news-9"></a>
### [Microsoft expands Windows built-in drivers, starting with printing](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 7.0/10

Microsoft confirmed at Ignite 2026 that it is developing new drivers for entire hardware classes and relying more heavily on Windows built-in drivers, with the goal of reducing third-party code in the system kernel. Printing is the first focus: the recently introduced Windows Ready Print mode is intended to replace legacy third-party print drivers. Windows product manager Mehmet Kucukgoz said SoundWire and SDCA audio drivers will soon become Windows built-in components, while I3C bus, USB Ethernet, and MIPI camera drivers are also in development. Microsoft also introduced a Driver Quality Initiative at its Windows Hardware Engineering Conference to raise driver reliability, quality, and security standards and encourage third-party developers and OEMs to use built-in drivers where possible.

telegram · zaihuapd · Nov 28, 02:09

**「Background」** Windows has long relied on OEM and hardware-vendor kernel-mode drivers for device classes such as printing and audio; because that code runs at high privilege, a faulty or vulnerable driver can affect the whole operating system. The current effort extends a shift already visible in printing, where Microsoft&\#x27;s Windows Ready Print is intended to replace legacy third-party print drivers.

**「Impact」** OEMs and third-party driver developers face a narrower role for custom kernel drivers: Microsoft is encouraging them to use built-in components and to apply the Driver Quality Initiative&\#x27;s standards to any custom drivers. Printer vendors are the first affected group, as Windows Ready Print is positioned to replace older third-party print drivers; audio, USB Ethernet, and camera driver vendors should expect similar built-in coverage as those drivers ship.

**Tags**: `#Windows`, `#device drivers`, `#Microsoft`, `#kernel security`, `#hardware ecosystem`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [What a Self-Built Audiobook Desk Taught About Iteration](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=197002) ⭐️ 5.0/10

rss · Dapenti Xilei · Nov 28, 03:19

**「Background」** The author&\#x27;s self-built “listening desk” for turning Dapenti content into audio had produced 241 hours, including a 700-page book that became 19 hours and 1 GB across more than 40,000 segments. The article examines why such a seemingly simple TTS workflow cannot be fully specified up front.

**「Solution」** The author argues that one-shot prompts suit simple tasks, but complex or initially unclear needs emerge only through real use. On the desk, a user&\#x27;s complaint that male podcast voices sounded too low led to a “male voice +0.5” setting—a narrow fix the author accepted because it was not disruptive; the stated upgrade principle is to accommodate most needs when changes remain manageable, while rejecting overly special ones when they do not. Other controls encode concrete frictions: editing text to work around LLM mispronunciations of polyphonic Chinese characters by temporarily substituting characters and then restoring them; auto-splitting long paragraphs the model handles poorly; inserting pauses when scenes change without chapter breaks; skipping prefaces and notes; and favoriting segments for later compilation. The review bar runs asynchronously from generation, queue-jump regeneration is available when needed, and regenerated clips return to the pending-review range before final audio or video export with a cover.

**「Takeaway」** The author concludes that even a simple application accumulates many details that cannot be anticipated at the start. Only real requirements and continual iteration yield concrete systems and the feedback needed to build real knowledge or consensus—in software and, by extension, in society.

**Tags**: `#TTS`, `#需求迭代`, `#音频生产`, `#产品设计`, `#LLM 工作流`

---

<a id="item-tech-blog-2"></a>
### [Six Years of Hard Drive Prices: 110 to Nearly 200 Yuan per TB](https://www.appinn.com/hard-drive-price-2026/) ⭐️ 5.0/10

rss · Appinn · Nov 27, 12:24

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/hard-drive-price-2026/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;Since 2020, the author of Appinn \(小众软件\) had been posting Amazon overseas-purchase deals on large external mechanical drives, and those posts turned into an accidental six-year price record. The 2026 Black Friday check turns that archive into a before-and-after comparison.

**「Solution」** Compiling his own past deal posts — mainly Western Digital Elements and My Book units — the author shows per-terabyte prices barely moving for five years: 14TB at 115.50 yuan/TB in October 2020 and 111.07 in December, 12TB at 112.47 in 2021, 16TB at about 110.09 in 2022, and in late 2025 an 18TB at 109.34 and a 20TB at 106.48 yuan/TB, all as tax-included landed prices. Even in December 2025 he quipped that stock availability mattered more than price. For 2026 he instead lists US Amazon asking prices from PerTerabyte and Disk Scout, converted at roughly 1:7 and excluding tax and cross-border shipping: 14TB at about 225 yuan/TB, 18TB at 288, 20TB at 192, 24TB at 206–292, and 30TB at 222. The concrete comparison is the Western Digital 20TB, which cost 2,129 yuan last Black Friday and roughly 3,850 yuan now — about 81% more before tax — moving the long-standing ~110 yuan/TB baseline to near 200. He corroborates this with blogger Alex Kretzschmar&\#x27;s own purchase log, where per-TB cost fell as low as $11.11 in 2023 and hit $27.50 in November 2026; the same 20TB EasyStore at Best Buy went from $249.99 in 2024 to $549.99 in 2026, a 120% rise in two years and 53% above his 2018 per-TB price, turning a $1,000 four-drive NAS into a $2,200 one. The author offers no explanation for the jump, and the samples come from promotional posts rather than a systematic price index.

**「Takeaway」** The author&\#x27;s point is that the roughly 110 yuan/TB ceiling that held for half a decade has broken, and 2026 Black Friday pricing sits near 200 yuan/TB and above — enough to reshape the economics of building a NAS.

**Tags**: `#机械硬盘价格`, `#存储成本`, `#黑五促销`, `#价格追踪`, `#NAS`

---

<a id="item-tech-blog-3"></a>
### [Coruna and DarkSword: Web-Only Exploits Hit Old iPhones](https://www.appinn.com/iphone-web-attacks-coruna-darksword/) ⭐️ 4.0/10

rss · Appinn · Nov 28, 01:13

**「Background」** Note: this summary may be AI-generated from the source and could differ from the original; verify against the linked article. Two exploit kits, Coruna and DarkSword, can compromise outdated iPhones and iPads merely when a malicious page loads—no app download or permission prompt is needed—and the payload reached visitors through tampered Optimizely scripts on major websites.

**「Solution」** Report URI examined 1,611 scripts and found 188 altered across 178 organizations, including BBC, CNN, Zoom, Salesforce, GitLab, IKEA, and HSBC. The injected code swapped copied cryptocurrency addresses for the attacker&\#x27;s and, in one variant, collected card details typed into page forms; on vulnerable iOS/iPadOS 18.7 or earlier it also attempted the Coruna and DarkSword exploits. Coruna targets iOS 13 through 17.2.1, while DarkSword targets iOS 18.4 through 18.7; Google reported finding DarkSword in real attacks from November 2025, and Apple later extended iOS 18.7.7 to more old devices. Optimizely said it removed the malicious code the same day, Report URI&\#x27;s recheck found the scripts clean, and as of November 25 Optimizely had no reports of device infection. The author&\#x27;s practical response is to install the latest available update: iOS 27.2.1 for iPhone 11 and later \(or 26.7.3 on the iOS 26 branch\), iOS 18.7.12 for XS/XS Max/XR, iOS 16.7.16 for 8/8 Plus/X, and iOS 15.8.8 for 6s/7/SE; devices on iOS 13 or 14 must first reach at least iOS 15.

**「Takeaway」** The incident shows how compromising a routine experimentation script can turn ordinary browsing into an infection path, making timely OS updates the practical defense; for devices that cannot update, the author offers little beyond reducing use.

**Tags**: `#iOS安全`, `#供应链攻击`, `#浏览器漏洞`, `#恶意脚本`, `#安全更新`

---

<a id="item-tech-blog-4"></a>
### [NodeWarden Update: Offline PWA, Backups and Multi-User on Cloudflare](https://www.appinn.com/nodewarden-update-1/) ⭐️ 4.0/10

rss · Appinn · Nov 27, 09:13

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/nodewarden-update-1/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;NodeWarden is an open-source project that runs a Bitwarden-compatible password vault on Cloudflare Workers, so users need no server and can stay within the free tier, pointing official Bitwarden clients at their own deployment.

**「Solution」** Nine months after his February introduction, the author rounds up what changed. The web vault is now an installable PWA that, once an online login has cached the vault, unlocks and shows passwords offline, including Passkey unlock on supported devices. A backup center makes scheduled incremental backups to WebDAV or S3-compatible storage, with presets for Cloudflare R2, Backblaze B2 and Tigris. Multi-user support makes the first registrant an administrator who invites others by code, each with a separate vault — Bitwarden-style organizations and shared collections are still missing. A security page flags weak, reused and breached passwords and accounts without 2FA, and 2FA itself now covers TOTP \(paid in Bitwarden, free here\), YubiKey OTP and Passkey. Upgrading means backing up, syncing the fork, updating the branch and letting Cloudflare rebuild, after which the database migrates itself; February-era deployments must confirm Node 24.22.1, keep the existing JWT\_SECRET and retain the database, attachment storage and Durable Objects bindings.

**「Takeaway」** The author presents NodeWarden as a free, serverless vault for family and friends and stresses that it is an independent third-party project unrelated to Bitwarden; because the post is a feature roundup, it leaves the architecture, free-tier limits and the trust implications of running third-party code against your vault unexamined.

**Tags**: `#Bitwarden 兼容`, `#Cloudflare Workers`, `#自建密码管理器`, `#开源项目更新`, `#PWA 离线`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China&\#x27;s State Council pledges stronger &\#x27;national team&\#x27; support for stock market, better Central Huijin stabilization fund](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 8.0/10

At a State Council executive meeting chaired by Premier Li Qiang on November 27, officials said China will step up the market-stabilizing role of state-backed investors and further optimize the quasi-&quot;stabilization fund&quot; function of Central Huijin, backed by &quot;ample liquidity guarantees.&quot; The meeting also called for policies to encourage insurers, corporate annuities and the social security fund to invest more in equities, and for tougher full-chain supervision to crack down on financial fraud and improper share reductions; no specific funding sizes, tools or timelines were disclosed.

telegram · zaihuapd · Nov 27, 05:35

**「Background」** China&\#x27;s State Council executive meeting, chaired by Premier Li Qiang, is the cabinet-level forum where such policy is coordinated; the readout said existing measures should be carried out and new ones planned, framing market support as &quot;counter-cyclical&quot; adjustment, but gave no funding size, specific instruments or timetable.

**「Who is affected」** Stock-market investors, along with savers whose money is managed by insurers, enterprise annuity funds and social security funds, are the main affected groups: an analyst cited by Eastmoney said the Central Huijin liquidity backstop is intended to interrupt self-reinforcing selloffs, while the long-term-fund measures could change equity allocation capacity; no scale or timetable was announced.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.eastmoney.com/a/202611273941634358.html">如何理解 国 常 会 对 资 本 市 场 的最新定调？ 专家解读来了 _ 东方财富网</a></li>

</ul>
</details>

**Tags**: `#资本市场政策`, `#国家队稳市`, `#中央汇金`, `#中长期资金入市`, `#监管执法`

---

<a id="item-finance-news-2"></a>
### [S&amp;P 500 enters correction, 11.6% below October record](https://www.cnbc.com/2026/11/27/the-sp-500-is-in-a-correction-bear-markets-and-recessions-dont-always-follow.html) ⭐️ 7.0/10

The S&amp;P 500 entered a correction on Nov. 20 for the first time since April 2025, closing at 6,910.39, or 11.6% below its Oct. 6 record of 7,818.93.

rss · CNBC Finance · Nov 27, 13:21

**「Background」** A correction is a drop of at least 10% from a recent high, while a bear market is 20% or more; CNBC found that 8 of 13 S&amp;P 500 bear markets overlapped recessions as defined by the National Bureau of Economic Research. Deutsche Bank strategist Henry Allen said none of the three factors that coincided with every S&amp;P 500 bear market since 1962—recession, worsening economic data or a Fed rate-hike cycle—was present so far.

**Tags**: `#S&amp;P 500`, `#market correction`, `#recession risk`, `#Federal Reserve`, `#AI spending`

---

<a id="item-finance-news-3"></a>
### [BBC: Energy bills to rise 26% in January after gas price surge](https://www.bbc.co.uk/news/videos/cwjd7y4jk581o?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

BBC Business reports that energy bills will rise 26% for millions of households in January, after a surge in gas prices linked to the Iran war. The report did not specify the current bill amount used as the baseline or the exact date the increase takes effect.

rss · BBC Business · Nov 27, 16:05

**「Background」** The 26% rise is tied to the UK energy price cap, which from January 2027 is set at £2,166 under new typical-household consumption values, after the gas-price surge.

**「Impact」** Those households will face higher winter energy costs, leaving less of their budget for other spending.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.co.uk/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>
<li><a href="https://www.bbc.com/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>

</ul>
</details>

**Tags**: `#energy bills`, `#gas prices`, `#household costs`, `#geopolitical risk`

---

<a id="item-finance-news-4"></a>
### [中國人民銀行承諾靈活運用貨幣政策工具以維護流動性](https://news.rthk.hk/rthk/ch/component/k2/1879533-20261127.htm) ⭐️ 7.0/10

中國人民銀行在其金融穩定報告中表示，將靈活高效運用多種貨幣政策工具，保持流動性充裕、社會融資條件相對寬鬆，並「切實增強資本市場內在穩定性」。報告稱，央行將研究建立在特定情景下向非銀行金融機構提供流動性的機制性安排；同日，國務院常務會議由總理李強主持，將資本市場稱為事關經濟發展全局，中國證監會則表示將研究推出新的增量政策，並鼓勵上市公司加大分紅和回購力度。

rss · RTHK Finance · Nov 27, 15:05

**「Background」** The People&\#x27;s Bank of China publishes a periodic Financial Stability Report, and this year&\#x27;s edition landed the same day as a State Council executive meeting chaired by Premier Li Qiang and a separate statement from the securities regulator. The &quot;two monetary policy tools supporting the capital market&quot; cited in the report are structural facilities the central bank had already set up; the new element is a study of a standing arrangement to supply liquidity to non-bank institutions under specified scenarios.

**Tags**: `#中國貨幣政策`, `#資本市場穩定`, `#人行`, `#中證監`, `#流動性支持`

---

<a id="item-finance-news-5"></a>
### [Meituan swings to Q3 net profit of RMB 2.07 billion as revenue rises 22%](https://news.rthk.hk/rthk/ch/component/k2/1879512-20261127.htm) ⭐️ 7.0/10

Meituan reported third-quarter net profit of RMB 2.07 billion, reversing a net loss of RMB 18.63 billion in the same period a year earlier, on revenue of about RMB 115.6 billion, up nearly 22% year on year. The company said its core local commerce segment posted RMB 5.7 billion in operating profit, compared with an operating loss of almost RMB 14.1 billion a year earlier.

rss · RTHK Finance · Nov 27, 09:28

**「Background」** A year earlier, Meituan posted its first quarterly loss in almost three years as a food-delivery subsidy war weighed on results, setting the comparison for the return to profit.

**「Impact」** Because Meituan ties its turnaround partly to more rational industry subsidies and higher average order values, the most direct effect falls on the households and restaurants that rely on delivery discounts, and on platforms now facing a state antitrust review of the delivery sector.

<details><summary>References</summary>
<ul>
<li><a href="https://money.udn.com/money/story/5603/9170382">外 賣 大戰拖累 美 團 第 3 季 虧762億 | 大陸政經 | 兩岸 | 經濟日報</a></li>
<li><a href="https://m.cnyes.com/news/id/6306238">m.cnyes.com/news/id/6306238</a></li>

</ul>
</details>

**Tags**: `#美團`, `#季度業績`, `#扭虧為盈`, `#外賣行業`, `#中國平台經濟`

---

<a id="item-finance-news-6"></a>
### [Hong Kong Stocks Climb 467 Points as Tech Index Jumps Over 6%](https://news.rthk.hk/rthk/ch/component/k2/1879507-20261127.htm) ⭐️ 7.0/10

Hong Kong&\#x27;s Hang Seng Index closed up 467 points, or 2.1%, at 22,694 on the futures settlement day of November 27, 2026, after a State Council executive meeting called for a stronger &quot;national team&quot; role in stabilizing the market. The tech index rose nearly 6.5% to 3,637, its biggest one-day gain in more than a year and a half, while main-board turnover exceeded HK$257.1 billion.

rss · RTHK Finance · Nov 27, 08:34

**「Background」** The rally followed a State Council executive meeting chaired by Premier Li Qiang on Nov. 27 that called for stepping up the “national team”—state-backed funds such as Central Huijin that buy shares to support prices—and for optimizing Central Huijin’s quasi-stabilization-fund role.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.eastmoney.com/a/202611273941564045.html">国常会：加力发挥“国家队”稳市作用 进一步优化中央汇金公司的类“平准...</a></li>
<li><a href="https://finance.sina.com.cn/roll/2026-11-28/doc-inkafyfq5072095.shtml">首提“国家队”，国常会释放稳市信号，机构火速解读_新浪财经_新浪网</a></li>
<li><a href="https://www.thepaper.cn/newsDetail_forward_34573081">国常会：加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准...</a></li>

</ul>
</details>

**Tags**: `#Hong Kong equities`, `#China policy`, `#tech rally`, `#semiconductors`, `#market stabilization`

---

<a id="item-finance-news-7"></a>
### [China regulators pledge to boost long-term funds in capital market, tighten shareholder and delisting rules](https://news.rthk.hk/rthk/ch/component/k2/1879500-20261127.htm) ⭐️ 7.0/10

China’s securities regulators pledged to push their policy for medium- and long-term funds entering the capital market to deliver more results and to tighten rules on controlling shareholders’ share sales and delistings, after a State Council executive meeting.

rss · RTHK Finance · Nov 27, 07:53

**「Background」** The State Council is China’s cabinet; the regulators’ remarks were reported by state-backed Xinhua Finance and set out priorities without new numerical targets or a timetable.

**Tags**: `#China capital markets`, `#regulatory policy`, `#long-term funds`, `#IPO regulation`, `#State Council`

---

<a id="item-finance-news-8"></a>
### [Chinese stocks surge after State Council signals market stabilization](https://news.rthk.hk/rthk/ch/component/k2/1879499-20261127.htm) ⭐️ 7.0/10

Mainland Chinese stocks jumped in afternoon trading after a State Council executive meeting released a market-stabilization signal, with the Shanghai Composite closing up 3.73% at 3,606 points and the ChiNext index up 11.61% at 2,443. The STAR 50 index rose more than 15% to 1,346, and for the full week the Shanghai Composite gained over 2%, the Shenzhen Component 5.4% and ChiNext 10.4%, ending two-week losing streaks.

rss · RTHK Finance · Nov 27, 07:39

**「Background」** The rally followed a State Council executive meeting chaired by Premier Li Qiang on 27 November, which studied ways to deepen reform of the capital market&\#x27;s investment and financing systems. State media said the meeting released five signals, including that capital markets &quot;bear on the overall economic development situation&quot; — read by media as a stabilisation message.

<details><summary>References</summary>
<ul>
<li><a href="https://www.gov.cn/zhengce/202611/content_7087453.htm">国务院常务会议解读 | 国常会关于资本市场部署释放五大鲜明信号_政策...</a></li>
<li><a href="https://baike.baidu.com/item/11%C2%B727%E5%9B%BD%E5%8A%A1%E9%99%A2%E5%B8%B8%E5%8A%A1%E4%BC%9A%E8%AE%AE/69886196">11·27国务院常务会议_百度百科</a></li>
<li><a href="https://www.xinhuanet.com/20261127/ef625930eb634a159637130d54351b94/c.html">国务院常务会议解读丨国常会新部署释放明确稳市信号-新华网</a></li>

</ul>
</details>

**Tags**: `#China stock market`, `#policy signal`, `#ChiNext`, `#STAR Market`, `#semiconductors`

---

<a id="item-finance-news-9"></a>
### [PBOC Halves Large-Denomination CD Purchase Thresholds, Effective March 2027](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

The People&\#x27;s Bank of China published new rules on Nov. 27 lowering the minimum purchase for large-denomination certificates of deposit to 100,000 yuan for individual investors and 500,000 yuan for institutions, half the previous 200,000 and 10 million yuan thresholds. The rules take effect March 21, 2027, and replace the 2015 interim measures; the same day the PBOC issued separate deposit and loan rate rules requiring banks to set rates independently and barring tactics such as luring deposits with above-market interest.

telegram · zaihuapd · Nov 27, 11:36

**「Background」** The new rules replace the PBOC&\#x27;s 2015 interim measures, which had set minimum large-denomination CD purchases at 200,000 yuan for individuals and 10 million yuan for institutions; both thresholds are halved under the new regime, effective March 21, 2027.

**「Who is affected」** Households holding 100,000–200,000 yuan in savings would newly qualify for individual large-denomination certificates of deposit once the lower minimum takes effect on March 21, 2027. The companion ban on luring deposits with unusually high interest rates could also constrain smaller banks that have recently raised deposit rates to compete for savers.

<details><summary>References</summary>
<ul>
<li><a href="https://post.smzdm.com/p/aggq3zk3/">2026 存 款 利 率 倒挂火了：10万 存 3年 利 息 差2000...</a></li>

</ul>
</details>

**Tags**: `#PBOC regulation`, `#large-denomination CDs`, `#deposit rates`, `#banking sector`, `#China financial policy`

---