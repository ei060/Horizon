---
layout: default
title: "Horizon Summary: 2026-11-24 (EN)"
date: 2026-11-24
lang: en
---

> From 178 items, 23 important content pieces were selected

---

**Technology News**
1. [Ladybird releases first alpha for macOS and Linux](#item-tech-news-1) ⭐️ 8.0/10
2. [Z.ai releases GLM-5.4, its first looped-transformer coding model](#item-tech-news-2) ⭐️ 8.0/10
3. [CrowdStrike to acquire Zscaler for $44B](#item-tech-news-3) ⭐️ 8.0/10
4. [Anthropic publishes claimed VP≠VNP proof with Lean 4 formalization, pending review](#item-tech-news-4) ⭐️ 8.0/10
5. [Report: Nvidia Board Reinstates Jensen Huang as CEO and Chairman](#item-tech-news-5) ⭐️ 7.0/10
6. [Third-Party Arm Documentation Site to Shut Down at Arm&\#x27;s Request](#item-tech-news-6) ⭐️ 7.0/10
7. [Amazon reportedly buying Decart&\#x27;s AI optimization tech for $7.5B](#item-tech-news-7) ⭐️ 7.0/10
8. [Virginia and Oregon Sue SpaceX Over Grok&\#x27;s NCII and CSAM Output](#item-tech-news-8) ⭐️ 7.0/10
9. [Codex2api suspected supply-chain compromise pushes backdoored releases](#item-tech-news-9) ⭐️ 7.0/10
10. [Meta AI chief says superintelligence is near and control is at risk](#item-tech-news-10) ⭐️ 7.0/10
11. [Mozilla, Shopify Join Call for EU Case on iPhone Browser Limits](#item-tech-news-11) ⭐️ 7.0/10
12. [Singapore Will Not Be a Conduit for Evading US Chip Controls, Wong Says](#item-tech-news-12) ⭐️ 7.0/10

**Technology Blog**
1. [vLLM Day-0 ERNIE 5.5 Flash Preview Support via Plugin](#item-tech-blog-1) ⭐️ 6.0/10
2. [Cloud Compute and the Limits of AI Chip Export Controls](#item-tech-blog-2) ⭐️ 5.0/10
3. [Upload2Shell: Ghostscript Flaw Turns Image Uploads Into Server Takeover](#item-tech-blog-3) ⭐️ 4.0/10
4. [WinGet Adds MCP Support So AI Assistants Can Install Windows Apps](#item-tech-blog-4) ⭐️ 4.0/10

**Financial News**
1. [Taiwan stocks close up about 9%; TSMC hits limit-up](#item-finance-news-1) ⭐️ 8.0/10
2. [AI selloff clouds DeepSeek, Moonshot and StepFun listing plans](#item-finance-news-2) ⭐️ 8.0/10
3. [Fed’s Williams Says More Work Needed on Inflation](#item-finance-news-3) ⭐️ 7.0/10
4. [Nvidia value climbs almost $1tn as tech stocks rally](#item-finance-news-4) ⭐️ 7.0/10
5. [Capita Shares Plunge 70% as CEO Quits After Civil Service Pension Delays](#item-finance-news-5) ⭐️ 7.0/10
6. [Hong Kong&\#x27;s first paperless IPO marks market infrastructure milestone](#item-finance-news-6) ⭐️ 7.0/10
7. [Shanghai to Adjust Metro Fares for First Time in 21 Years](#item-finance-news-7) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Ladybird releases first alpha for macOS and Linux](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird has released its first alpha, with installable builds for macOS and Linux that no longer require users to compile the browser themselves. The project implements HTML parsing, CSS, layout, JavaScript and WebAssembly in-house while relying on external components including HarfBuzz, Skia, ffmpeg and SQLite. In the source author&\#x27;s testing, most sites worked, including WebAssembly apps such as an ffmpeg video compressor and a Pyodide REPL, but Datasette Lite failed because navigator.serviceWorker.startMessages is missing. Ladybird&\#x27;s October update added 75,650 web-platform-tests passes to reach 2,184,722, ahead of Safari&\#x27;s 2,172,990 but behind Firefox&\#x27;s 2,189,315 and Chrome&\#x27;s 2,244,397, alongside a new JavaScript JIT and a Cranelift WebAssembly engine that delivered a 7x JetStream 3 WASM gain.

hackernews · janvdberg · Nov 23, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50614249)

**「Earlier development」** Ladybird grew out of SerenityOS, whose code it still reuses for components not rewritten in-house, while relying on external libraries such as HarfBuzz, Skia, ffmpeg and SQLite for text shaping, graphics, video and storage. In February 2026 the project described porting parts of its LibJS JavaScript engine from C++ to Rust with AI coding agents, and by October 2026 it reported 75,650 new web-platform-tests passes, a new JavaScript JIT and a faster WebAssembly engine. Those earlier engine and compatibility gains preceded the first installable macOS and Linux alpha.

**「Impact」** Users can now evaluate Ladybird&\#x27;s compatibility on macOS and Linux and report broken sites or crashes from inside the browser, but sites that depend on service-worker messaging may fail until missing APIs are implemented.

**「Community discussion」** Commenters report that many sites, including Proxmox and NoVNC, rendered correctly, though one noticed slightly jerky scrolling and another found NoVNC snappier than in Firefox; these are early user impressions rather than benchmarks. Others urged the project to prioritize anti-fingerprinting measures and more granular permissions, and asked what precautions are appropriate when using an alpha browser.

**Tags**: `#Ladybird`, `#browser engines`, `#open-source software`, `#web standards`, `#alpha release`

---

<a id="item-tech-news-2"></a>
### [Z.ai releases GLM-5.4, its first looped-transformer coding model](https://z.ai/blog/glm-5.4) ⭐️ 8.0/10

Z.ai has released GLM-5.4, its first model built on a looped-transformer architecture in which a group of weight-shared layers runs for multiple iterations to refine hidden states, adding depth without increasing parameter count. The model is not available as open weights and is currently accessible through Z.ai&\#x27;s Coding Plan subscription, whose API keys work with the same OpenAI-compatible Responses API at https://api.z.ai/api/v1 as the regular plan. Z.ai presents the architecture as a step toward generalized coding, but the supplied evidence is mainly the vendor announcement and early user tests; Simon Willison&\#x27;s pelican SVG comparison found GLM-5.4 similar in quality to GLM-5.3 and unlike earlier GLM generations&\#x27; distinctive outputs.

hackernews · foohis · Nov 23, 10:06 · [Discussion](https://news.ycombinator.com/item?id=50609685)

**「Background」** In a standard transformer, every layer runs once per forward pass. A looped transformer instead sends hidden states through a shared block of layers for multiple iterations, gaining depth without adding parameters. The approach was already in the news days earlier: Thinking Machines Lab&\#x27;s Inkling 2 Mini, announced November 20, was described as running its middle layers three times per token, and reporting on GLM-5.4 says Z.ai executes a 28-layer block twice per token.

**「Access and Evaluation Caveats」** Developers who want to test GLM-5.4 cannot get it through the regular Z.ai API plan or OpenRouter; they must subscribe to the Coding Plan, whose API keys nonetheless work against the same OpenAI-compatible Responses API endpoint at https://api.z.ai/api/v1. The only comparative coding evidence available is Zhipu&\#x27;s internal evaluation, where GLM-5.4 won 51.1% of comparisons against GLM-5.3 and lost 23.1% — a vendor-reported figure with no independent benchmark published alongside the launch.

**「Community discussion」** Commenters welcomed the technical detail Zhipu disclosed about looped transformers, with one arguing that the standard Transformer is like an unrolled loop and that looping is an obvious direction despite unresolved problems. Another reported that Chinese models&\#x27; long &quot;marathon thinking&quot; sessions make even conceptually simple tasks slow, while Simon Willison noted that GLM-5.4 required the Coding Plan because it was unavailable through OpenRouter or the regular Z.ai API.

<details><summary>References</summary>
<ul>
<li><a href="https://wccftech.com/z-ai-debuts-glm-5-4-with-a-novel-looped-transformer-architecture-skipping-ai-benchmarks-entirely/">Z.ai Debuts GLM - 5 . 4 With a Novel Looped Transformer Architecture...</a></li>
<li><a href="https://kingy.ai/blog/glm-5-4-launch/">GLM ‑ 5 . 4 launch: How to use it, pricing and API status</a></li>

</ul>
</details>

**Tags**: `#LLMs`, `#GLM-5.4`, `#looped transformers`, `#Zhipu AI`, `#coding models`

---

<a id="item-tech-news-3"></a>
### [CrowdStrike to acquire Zscaler for $44B](https://techcrunch.com/2026/11/23/crowdstrike-to-acquire-zscaler-for-44-billion/) ⭐️ 8.0/10

CrowdStrike plans to acquire Zscaler for $44 billion, according to a TechCrunch report published November 23, 2026. CrowdStrike said the deal is intended to better equip large-enterprise customers using Zscaler&\#x27;s zero-trust products to adopt AI agents. The transaction is an announced plan, not a completed acquisition; the supplied report did not include financing, regulatory approval, or closing timing.

rss · TechCrunch · Nov 23, 16:20

**「Background」** Zscaler sells zero-trust security products to large enterprises, and the companies said the deal would bring its network-security and zero-trust capabilities into CrowdStrike&\#x27;s Falcon platform. The transaction is all-stock, with an enterprise value of about $43.9 billion based on CrowdStrike&\#x27;s November 20, 2026 closing price; Reuters described it as the largest cybersecurity acquisition on record.

**「Impact」** For large enterprises that run both CrowdStrike&\#x27;s Falcon endpoint agent and Zscaler&\#x27;s zero-trust stack, the announced deal creates an immediate integration question: whether Zscaler&\#x27;s products remain separately deployable or are folded into CrowdStrike&\#x27;s platform. The brief announcement gave no timetable or product roadmap. That matters because Falcon works at the operating system kernel level on individual machines, a privileged position that drew scrutiny after CrowdStrike&\#x27;s faulty 2024 update caused widespread outages.

<details><summary>References</summary>
<ul>
<li><a href="https://www.crowdstrike.com/en-us/press-releases/crowdstrike-to-acquire-zscaler-bringing-network-security-and-zero-trust-to-the-falcon-platform/">CrowdStrike to Acquire Zscaler , Bringing Network Security and ...</a></li>
<li><a href="https://www.zscaler.com/press/crowdstrike-acquire-zscaler-bringing-network-security-and-zero-trust-falcon-platform">CrowdStrike to Acquire Zscaler for Zero Trust</a></li>
<li><a href="https://www.reuters.com/legal/transactional/crowdstrike-buy-zscaler-439-billion-2026-11-23/">CrowdStrike snaps up Zscaler in $44 billion deal as cyber ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/CrowdStrike">CrowdStrike - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/2024_CrowdStrike-related_IT_outages">2024 CrowdStrike -related IT outages - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#acquisitions`, `#zero-trust`, `#enterprise security`, `#AI agents`

---

<a id="item-tech-news-4"></a>
### [Anthropic publishes claimed VP≠VNP proof with Lean 4 formalization, pending review](https://github.com/anthropics/formal-math/blob/main/vp-vnp/README.md) ⭐️ 8.0/10

On November 24, Anthropic published a paper titled “VP ≠ VNP over every field” and a Lean 4 formalization in its anthropics/formal-math repository, saying an internal Claude research model discovered the result and that the paper and code were AI-written. The paper claims a superpolynomial arithmetic-circuit lower bound for the Hamiltonian cycle polynomial, implying VP is a proper subset of VNP and resolving Valiant&\#x27;s 1979 algebraic complexity conjecture; the claim concerns arithmetic circuits only, not P versus NP. The proof passed an audit against three standard axioms and an independent nanoda kernel check with no \`sorry\` outside a reserved file, but no human mathematician has read it through, Lean cannot confirm that the formal statement matches the claimed theorem, and Appendix Q lists discrepancies—independent review is still pending.

telegram · zaihuapd · Nov 24, 06:02

**「Background」** VP versus VNP, introduced by Valiant, is the algebraic analogue of P versus NP and is framed in terms of polynomial-size arithmetic circuits; it is a separate problem from P versus NP. It is regarded as a central open question in algebraic complexity theory.

**「Verification still required before reliance」** Until human mathematicians confirm that the Lean 4 statement actually encodes VP ≠ VNP — the repository&\#x27;s Appendix Q lists discrepancies and Lean alone cannot check that the formal statement matches the claimed theorem — complexity theorists and anyone building on the result should treat it as an unverified claim rather than a resolution of Valiant&\#x27;s 1979 conjecture. Independent reviewers would need to reconcile those discrepancies and re-check the proof before downstream work can safely depend on the circuit lower bound for the Hamiltonian cycle polynomial.

<details><summary>References</summary>
<ul>
<li><a href="https://www.alphaxiv.org/abs/2611.vp-vnp-arithmetic-lower-bounds">VP VNP Over Every Field | alphaXiv</a></li>
<li><a href="https://eccc.weizmann.ac.il/keyword/18289/">ECCC - Reports tagged with VNP</a></li>
<li>Claude claims to prove VP ≠ VNP in Valiant&#x27;s 47-year-old conjecture</li>

</ul>
</details>

**Tags**: `#AI for mathematics`, `#complexity theory`, `#Lean 4`, `#formal verification`, `#Anthropic`

---

<a id="item-tech-news-5"></a>
### [Report: Nvidia Board Reinstates Jensen Huang as CEO and Chairman](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 7.0/10

An Ars Technica report, citing an Nvidia announcement, says Nvidia&\#x27;s board voted to reinstate Jensen Huang as CEO and chairman of the board, effective immediately, 11 days after he resigned amid multiple scandals. The board said the decision was based in part on &quot;input from senior levels of the United States government&quot; assuring members that &quot;Mr. Huang&\#x27;s reinstatement poses no national security risk.&quot; That assurance came despite Huang&\#x27;s admitted affair with a woman US intelligence sources believe was working as a Chinese spy, allegations that Nvidia subverted export controls intended to keep its chips out of China, and what the report describes as multiple developing investigations by different government departments into national security, accounting, and corporate governance matters. The supplied article text was truncated and no primary announcement or independent confirmation was available, so the precise terms of the reinstatement and the status of those investigations remain unverified.

hackernews · jaz · Nov 23, 14:00 · [Discussion](https://news.ycombinator.com/item?id=50611576)

**「Background」** Nvidia&\#x27;s November 12, 2026 announcement said Huang had resigned as president, CEO and board member effective immediately. A subsequent Nvidia release says the board voted unanimously to reinstate him after discussions and meetings with him.

**「Impact」** Because the board reinstated Huang on the strength of U.S. government assurances rather than a completed review, Nvidia’s customers and partners still face an unsettled export-control and compliance picture while the investigations cited in the report continue. Semafor’s report that Trump called into Nvidia’s board meeting also ties the leadership decision directly to political input, not an independent resolution of those investigations.

**「Community Discussion」** Commenters seized on the board&\#x27;s citation of US government input as the operative part of the statement, with one citing Delaware&\#x27;s Caremark standard as a high bar for board culpability and expressing surprise that the reversal was unanimous less than two weeks after Huang was forced out. Others disputed the premise that a crime was covered up, arguing that intelligence officials have said they are unsure the woman was a spy and that no evidence has leaked, while several criticized what they saw as hypocrisy given US pressure on ASML and Japanese chip companies to join China sanctions, and one drew a parallel to OpenAI&\#x27;s 2023 board episode to argue that a firm&\#x27;s nominal governance structure is not necessarily its real one.

<details><summary>References</summary>
<ul>
<li><a href="https://nvidianews.nvidia.com/_gallery/download_pdf/6b04462d3d63321add7499dc/">NVIDIA Board Reinstates Jensen Huang as President, CEO and Board ...</a></li>
<li><a href="https://nvidianews.nvidia.com/news/nvidia-announces-ceo-transition">NVIDIA Announces CEO Transition</a></li>
<li><a href="https://www.semafor.com/article/11/23/2026/huang-reinstatement-came-at-trumps-behest">Huang reinstatement came at Trump’s behest | Semafor</a></li>
<li><a href="https://www.nbcnews.com/tech/tech-news/nvidia-reinstates-jensen-huang-rcna610864">Nvidia reinstates Jensen Huang as CEO</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#semiconductors`, `#corporate governance`, `#US policy`, `#national security`

---

<a id="item-tech-news-6"></a>
### [Third-Party Arm Documentation Site to Shut Down at Arm&\#x27;s Request](https://arm.jonpalmisc.com/) ⭐️ 7.0/10

The third-party Arm documentation site arm.jonpalmisc.com will be discontinued on 4 December 2026 at Arm&\#x27;s request, site operator jonpalmisc said. According to the operator, Arm asked for removal on the grounds that hosting Arm&\#x27;s documentation uses its trademarks and IP, a demand he said is difficult to work around while keeping the site useful. He said he is considering offers to host mirrors, to seek legal advice, or to release the site&\#x27;s source code without Arm IP so others can generate a similar site for personal use. The notice does not describe a court ruling or a licensing agreement with Arm.

hackernews · tech234a · Nov 23, 19:17 · [Discussion](https://news.ycombinator.com/item?id=50617499)

**「Context」** Arm treats its official architecture documentation as protected by copyright and trademark, and the site being discontinued was an unofficial, browsable copy of that material. Its operator said Arm requested removal on the grounds that hosting the documentation used Arm&\#x27;s trademarks and IP, which he said was difficult to work around without making the site less useful. A commenter noted that Arm&\#x27;s Machine Readable Architecture Specification is separately published under a BSD-style license, but that does not by itself cover the broader documentation set.

**「Impact」** Engineers who used the site as an alternative way to read Arm architecture documentation lose that access when it shuts down on 4 December 2026. The operator said the trademark/IP objection is hard to work around while keeping the site useful, and is weighing community offers to host mirrors or to release the site&\#x27;s source code without Arm IP so others can generate the same documentation locally. Whether any mirror or self-hosted version survives remains unresolved.

**「Community discussion」** Commenters questioned whether reproducing documentation for publicly sold hardware is fair use and whether Arm&\#x27;s request is enforceable, with one pointing to BSD-style licensing on Arm machine-readable specification packages. Others criticized the takedown as making life harder for engineers who rely on Arm, and the operator acknowledged offers to host mirrors or release the non-Arm source.

**Tags**: `#Arm`, `#technical documentation`, `#intellectual property`, `#hardware engineering`, `#community debate`

---

<a id="item-tech-news-7"></a>
### [Amazon reportedly buying Decart&\#x27;s AI optimization tech for $7.5B](https://techcrunch.com/2026/11/23/amazon-snaps-up-decarts-ai-optimization-tech-for-7-5b-as-it-prepares-to-sell-trainium-chips/) ⭐️ 7.0/10

Amazon is acquiring Decart&\#x27;s AI optimization technology and its research team in a deal reported at $7.5 billion, according to TechCrunch. The report links the purchase to Amazon&\#x27;s preparations to sell its Trainium AI chips. The supplied account gives no detail on deal structure, closing conditions, or exactly which optimization technology and staff are covered, so the price and scope remain reported rather than confirmed figures.

rss · TechCrunch · Nov 23, 17:14

**「Background」** Decart is an Israeli AI company focused on real-time world models—generative systems that produce interactive video and simulated environments frame by frame with low latency—and the infrastructure needed to run them, according to Wikipedia and the company. Decart describes its systems as responding instantly at millisecond latency.

**「Customer and buyer uncertainty」** Existing Decart users face uncertainty about whether products built on the acquired optimization technology will remain available or change terms, because the report gives no licensing, support, or closing details. Organizations evaluating Trainium likewise lack specifics on whether the acquired work will be packaged with the chips, sold separately, or kept internal.

<details><summary>References</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Decart">Decart - Wikipedia</a></li>
<li><a href="https://decart.ai/">Decart - The Live AI Lab the World Runs On</a></li>

</ul>
</details>

**Tags**: `#Amazon`, `#Decart`, `#AI optimization`, `#Trainium`, `#acquisitions`

---

<a id="item-tech-news-8"></a>
### [Virginia and Oregon Sue SpaceX Over Grok&\#x27;s NCII and CSAM Output](https://arstechnica.com/tech-policy/2026/11/states-sue-spacex-to-stop-grok-from-generating-child-sex-images-revenge-porn/) ⭐️ 7.0/10

Virginia and Oregon became the first states to sue SpaceX, alleging that its Grok model continues to generate non-consensual intimate imagery \(NCII\) and child sexual abuse material \(CSAM\) from real photos, mostly of women and children. The suits, filed Monday, target the company now known as SpaceXSI after SpaceX acquired xAI in February and inherited the fallout from Grok&\#x27;s &quot;spicy mode.&quot; The state attorneys general allege that earlier company statements claiming added safeguards and redesigned policies were &quot;misleading,&quot; and that the company instead quietly &quot;embraced&quot; sexualized content to gain AI market share. These are allegations in the complaints, not established findings; the supplied excerpt does not include the case numbers, the specific relief sought, or SpaceX&\#x27;s response.

rss · Ars Technica · Nov 23, 21:30

**「Background」** The lawsuits follow SpaceX’s February acquisition of xAI, which brought the maker of Grok into the rocket company and is now referred to as SpaceXSI. Before that, xAI had promoted Grok’s “spicy mode”; after it was found to generate non-consensual intimate imagery and sexualized images of children, the company apologized and said it had added safeguards—claims the states now allege were misleading.

**「Court-ordered limits on Grok」** Virginia and Oregon are asking courts to stop Grok from generating non-consensual intimate imagery and child sexual abuse material, so SpaceXSI faces externally imposed output restrictions rather than relying on its own claimed safeguards and redesigned policies. That makes the adequacy of Grok&\#x27;s image moderation a live legal question for the company, not just a product-policy choice.

**Tags**: `#AI safety`, `#generative AI`, `#content moderation`, `#AI regulation`, `#Grok`

---

<a id="item-tech-news-9"></a>
### [Codex2api suspected supply-chain compromise pushes backdoored releases](https://github.com/WormW/codex2api-incident-2026-11) ⭐️ 7.0/10

A suspected supply-chain compromise of the Codex2api project pushed backdoored releases after the maintainer&\#x27;s account was taken over, according to a Telegram-sourced incident retrospective. The attacker reportedly bypassed the main branch by pushing a tag directly so the Release build shipped the malicious versions; v3.1.11 removed authentication, leaving the service exposed to unauthenticated remote command execution, while a workflow exfiltrated 16 GitHub Actions secrets affecting at least 21 repositories under the same account. Anyone who installed or updated versions 3.1.10 through 3.1.12 is advised to stop using them immediately, roll back to 3.1.9, and rotate GitHub tokens, SSH keys, database credentials, and DeepSeek and other related secrets. The report describes a suspected incident confined to one project and has not been independently confirmed.

telegram · zaihuapd · Nov 23, 11:21

**「Context: what Codex2API is and how its releases are built」** Codex2API is an open-source Go/React reverse proxy that turns a pool of Codex accounts into a single OpenAI-compatible API endpoint, so deployments typically hold upstream credentials and database access. Its releases are produced by GitHub Actions from pushed tags rather than only from the \`main\` branch, a path that can sidestep branch protections and let a compromised account publish a build without merging code.

**「Who must act, and how」** Anyone who installed or updated Codex2api v3.1.10–v3.1.12 should stop the service immediately, roll back to v3.1.9, and rotate every credential the repository could reach — GitHub tokens, SSH keys, database passwords, and DeepSeek and other upstream API keys — since the workflow reportedly exfiltrated 16 Actions secrets and affected at least 21 repositories under the same account. Because v3.1.11 removed authentication, any instance left reachable effectively offered unauthenticated remote command execution, so exposure should be assumed until logs are reviewed. The release was reportedly built from a tag pushed around the main branch, which means branch protection and review rules on \`main\` alone would not have blocked it; maintainers of similarly tag-driven release pipelines need protection on tags and release workflows, not just on the default branch.

<details><summary>References</summary>
<ul>
<li><a href="https://deepwiki.com/james-6-23/codex2api">james-6-23/ codex2api | DeepWiki</a></li>

</ul>
</details>

**Tags**: `#supply-chain security`, `#GitHub Actions`, `#security incident`, `#credential rotation`, `#open source`

---

<a id="item-tech-news-10"></a>
### [Meta AI chief says superintelligence is near and control is at risk](https://thenextweb.com/news/metas-ai-chief-says-superintelligence-is-arriving-and-control-is-at-risk) ⭐️ 7.0/10

Meta chief AI officer Alexandr Wang said on X that superintelligence is no longer a future issue and warned that humans may struggle to control systems that can self-improve indefinitely or be 1,000 times smarter, calling for urgent safety and alignment research. He cited a Riemann Hypothesis proof that mathematician Levent Alpöge produced with Anthropic&\#x27;s Claude and that was machine-verified by the Lean and Mathlib community on Saturday, saying the remaining gap between AI and top humans is concrete knowledge, engineering integration, and experimentation. The proof has no human-readable version, and the item provides no independent confirmation, so the claim remains unverified.

telegram · zaihuapd · Nov 23, 12:49

**「Context: the mathematician and the checker」** Levent Alpöge, the mathematician Wang credits with the proof, is a Turkish-American number theorist who according to Wikipedia and press profiles holds a technical staff position at Anthropic and is known for applying AI to major unsolved problems in mathematics — which is why the work ran through Claude. The result was checked in Lean, a proof assistant whose Mathlib library lets the community machine-verify a formal proof; that is how the claim can circulate as verified while, as the source notes, no human-readable version yet exists.

**「Impact」** For mathematicians and AI-safety reviewers, the cited case makes human-readable exposition and independent review the immediate bottleneck: a Lean/Mathlib-checked proof can be machine-validated without being intelligible to people, and no such exposition is currently available.

<details><summary>References</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Levent_Alp%C3%B6ge">Levent Alpöge - Wikipedia</a></li>
<li><a href="https://www.clarin.com/us-news/who-is-levent-alpoge-the-anthropic-mathematician-who-claims-solved-the-riemann-hypothesis-with-claude_0_2WdGvYKBVM.html">Who is Levent Alpöge? The Anthropic mathematician who claims ......</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#superintelligence`, `#AI for mathematics`, `#formal verification`, `#Meta AI`

---

<a id="item-tech-news-11"></a>
### [Mozilla, Shopify Join Call for EU Case on iPhone Browser Limits](https://appleinsider.com/articles/26/11/23/eu-urges-to-challenge-apples-grip-on-iphone-browsers?utm_source=rss) ⭐️ 7.0/10

Mozilla, Shopify and other companies and civil-society groups have signed a letter asking the European Commission to open a case against Apple&\#x27;s iPhone browser restrictions. The signatories say they collectively represent roughly 45,000–55,000 EU businesses and organizations, with signatures open until Dec. 3, 2026. They argue that although Apple lets rival browsers use their own engines in the EU under the Digital Markets Act, technical and legal requirements prevent them from moving existing EU users off WebKit, while businesses still depend on the App Store for reach. The letter estimates that shifting half of native iOS apps to the web could save EU businesses €11 billion a year in development costs and €1.3 billion in App Store fees; it is an advocacy request, not an EU investigation or ruling.

telegram · zaihuapd · Nov 24, 03:02

**「Regulatory context」** Under the EU Digital Markets Act, Apple is required to let competing browsers use their own engines on iOS in the EU, a change it has implemented. The signatories say remaining technical and legal requirements still prevent them from moving existing EU users off WebKit, which is why they want the European Commission to open a formal investigation.

**「Impact」** According to the letter&\#x27;s signatories, rival browser makers can offer non-WebKit engines in the EU but cannot readily migrate their existing EU iPhone users off WebKit, so the practical reach of the DMA&\#x27;s engine allowance depends on whether the Commission opens a case.

**Tags**: `#EU DMA`, `#Apple`, `#浏览器竞争`, `#App Store`, `#开放 Web`

---

<a id="item-tech-news-12"></a>
### [Singapore Will Not Be a Conduit for Evading US Chip Controls, Wong Says](https://www.bloomberg.com/news/articles/2026-11-24/singapore-won-t-be-conduit-to-skirt-us-chip-curbs-wong-says) ⭐️ 7.0/10

Singapore Prime Minister Lawrence Wong said the country will not serve as a conduit for companies evading US chip export controls, and authorities are investigating Megaspeed&\#x27;s purchases of Nvidia chips. A day earlier, the US Commerce Department added Megaspeed and six other Southeast Asian firms to a trade blacklist, with the Federal Register citing a &quot;significant risk&quot; that advanced computing products could be diverted to unauthorized users; the listings include affiliates in Malaysia and Thailand. Reuters reported that Apex Enterprise Solutions, an Alibaba subsidiary in Singapore, was also listed; Alibaba said it has never transferred controlled advanced computing chips.

telegram · zaihuapd · Nov 24, 05:03

**「Background」** US export controls restrict the sale of advanced AI chips and related computing products to approved recipients, and the Commerce Department&\#x27;s Entity List flags parties suspected of diverting such goods to unauthorized users. Singapore&\#x27;s statement follows the prior day&\#x27;s addition of Megaspeed and six other Southeast Asian firms to that list, including affiliates in Malaysia and Thailand; the listing cited a significant risk of transferring advanced computing products to unauthorized users.

**「Impact」** Companies handling advanced chips in Southeast Asia face tighter compliance risk: the blacklisting can block listed firms and their Malaysian and Thai affiliates from receiving covered US-controlled products, while Singapore&\#x27;s investigation and the prime minister&\#x27;s pledge signal that locally routed transactions will be scrutinized.

**Tags**: `#AI chips`, `#export controls`, `#Singapore`, `#Nvidia`, `#semiconductor supply chain`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [vLLM Day-0 ERNIE 5.5 Flash Preview Support via Plugin](https://vllm.ai/blog/2026-11-24-ernie-5-5-flash-preview) ⭐️ 6.0/10

rss · vLLM Blog · Nov 24, 00:00

**「Background」** ERNIE 5.5 Flash Preview is a sparse mixture-of-experts model with 280B total parameters but only 14B activated per token, a 1M-token context, and tool-calling for long-horizon agent work. Its attention and MoE layers introduce new structures—low-rank cross-head post-mixing, Multi-Router Latent MoE, a MultiMax output head, and sigmoid gating—that, implemented op by op, generate many intermediate tensors and pay for them in memory traffic and kernel launches.

**「Solution」** Baidu and the vLLM team address this by designing a dedicated fused kernel around each structure&\#x27;s compute and memory profile and pre-folding anything fixed into the weights at load time: VHA mixing parameters collapse into a single matrix with FP8 quantization done in registers, all router weights are concatenated so one GEMM yields every router&\#x27;s logits, and MultiMax&\#x27;s four-piece transform runs in one pass. The authors report 1.55× to 6.53× per-kernel speedups with bitwise-identical outputs for several fusions, though no benchmark methodology is given. FlashIndexer, shipped with the weights, routes each query token to a few sparse indexer heads using only that token&\#x27;s hidden state, so routing cost does not grow with context, and adds threshold pre-filtering against a 2048-token top-k; a small router trained by distillation over about 1B tokens yields a 1.4× speedup at 1M context. Routed experts use MXFP4 W4A8 quantization-aware training matched exactly to inference numerics, with FP8 KV cache and FP4 indexer computation, while a 3-layer DSpark draft model proposes up to 7 tokens at a mean acceptance length above 4.0 on coding and agent workloads. Delivery is a standalone vLLM-ERNIE plugin installed alongside the official vllm==0.32.0 wheel: it registers architectures with ModelRegistry as module paths and imports model code only when a config names them, so the plugin adds no overhead for other models and needs no fork, custom image, or nightly build.

**「Takeaway」** The authors&\#x27; larger claim is that packaging model-specific code and kernels as a lazy-registered plugin lets day-0 support ship on the model&\#x27;s schedule—fixes and features need not wait for a vLLM release—while the shared serving stack \(prefix caching, CUDA graphs, speculative decoding, PD disaggregation\) keeps working untouched.

**Tags**: `#vLLM`, `#ERNIE`, `#MoE inference`, `#kernel fusion`, `#speculative decoding`

---

<a id="item-tech-blog-2"></a>
### [Cloud Compute and the Limits of AI Chip Export Controls](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196937) ⭐️ 5.0/10

rss · Dapenti Xilei · Nov 23, 23:17

**「Background」** As export controls target physical AI chips, the author argues that cloud-delivered compute exposes a regulatory gap: the chip’s location and the customer’s location can be separated, so customs checks and licences do not necessarily control access to computing capability.

**「Solution」** The article uses Megaspeed to illustrate this gap. The Singapore cloud provider joined Nvidia’s cloud partner programme in November 2023, publicly named Alibaba as a core customer, and used its Malaysian subsidiary Speedmatrix to host advanced chips abroad and sell compute across borders within an apparently legal structure. After Nvidia internally blacklisted Megaspeed in June 2025, a new Singapore entity, Novagate Cloud, appeared; short-seller Culper Research alleged overlapping web design and registration addresses and possible business continuity, while reports said at least $300 million of related hardware reached a Malaysian affiliate in early 2026. The author stresses that these are allegations and media reports, not court convictions. Separately, Singapore prosecutors charged Li Ming and his company Luxuriate Your Life in 2025 and 2026 over allegedly false end-use and end-user declarations to Supermicro for servers routed to Malaysia—a criminal case that, in the author’s view, exposes weaknesses in KYC and post-sale traceability. The article also maps family and corporate ties involving Century Longteng, Inspur’s Aivres and Century Huatong, while cautioning that associations do not establish legal liability. It frames Nvidia’s dilemma as balancing commercial expansion against export compliance and governance scrutiny.

**「Takeaway」** The author concludes that entity lists and physical export checks lose force when compute is sold as a cross-border service, leaving policymakers to decide whether to regulate hardware, cloud services, or cross-border data boundaries.

**Tags**: `#AI chip export controls`, `#cloud compute`, `#supply-chain compliance`, `#regulatory arbitrage`, `#Megaspeed case`

---

<a id="item-tech-blog-3"></a>
### [Upload2Shell: Ghostscript Flaw Turns Image Uploads Into Server Takeover](https://www.appinn.com/upload2shell-cve-2026-125396/) ⭐️ 4.0/10

rss · Appinn · Nov 24, 03:08

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/upload2shell-cve-2026-125396/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;Image upload boxes are usually treated as harmless, but many applications quietly hand uploaded files to Ghostscript, the decades-old open-source PDF/PostScript interpreter, to build thumbnails, render previews, convert documents, or process print jobs. Upload2Shell \(CVE-2026-125396, CVSS 4.0 8.5/10\) is a sandbox escape in that shared dependency, discovered 27 July 2026 and described publicly on 21 November 2026, so the exposure reaches far beyond any single product.

**「Solution」** The author&\#x27;s central point is that a crafted file can break out of Ghostscript&\#x27;s safety sandbox and run arbitrary commands on the host — and that a file named .jpg or .png may still trigger it inside certain processing pipelines, so extension checks are not a defence. The article reports validated attack paths rather than deep mechanism analysis: WordPress media uploads, CUPS print jobs sent to shared network printers, public Forminator and Elementor registration forms, and MediaWiki PDF uploads with thumbnail generation. The most striking is Roundcube, where simply opening an email containing a malicious attachment makes the server render a thumbnail through Ghostscript — no attachment click needed — turning one user&\#x27;s inbox view into a compromise of the whole mail server. The report also lists parts of Google&\#x27;s file-processing services and flags ComfyUI and Stable Diffusion WebUI as potential paths. Ghostscript 10.08.0, released 8 September, fixes the flaw; downstream fixes include WordPress 7.0.4/6.9.7/6.8.8, Roundcube 1.6.20, and specific Debian 12/13 packages, with Ubuntu updates published. The author stresses that Docker deployments must be checked for the Ghostscript version inside the container, and cites Sophos as saying proof-of-concept code is public while no real attacks had been publicly reported as of 23 November.

**「Takeaway」** Because a single buried interpreter underpins countless image and PDF pipelines, the patched surface is the whole stack, not just the visible application — which is why the author frames this as an urgent inventory-and-update task for anyone self-hosting.

**Tags**: `#漏洞通报`, `#Ghostscript`, `#CVE-2026-125396`, `#补丁管理`, `#供应链安全`

---

<a id="item-tech-blog-4"></a>
### [WinGet Adds MCP Support So AI Assistants Can Install Windows Apps](https://www.appinn.com/winget-mcp-server/) ⭐️ 4.0/10

rss · Appinn · Nov 23, 07:19

**「Background」** Installing software on Windows usually means downloading an installer and clicking through setup wizards, though Microsoft&\#x27;s free WinGet \(Windows Package Manager\) already allows searching, installing, upgrading, and uninstalling apps from a terminal with a single command — roughly what Homebrew does on macOS or apt on Linux, alongside third-party options like Chocolatey and Scoop. Microsoft has now added support for MCP \(Model Context Protocol\) to WinGet, meaning MCP-capable AI assistants can drive the package manager directly.

**「Solution」** The WinGet MCP Server exposes two tools: find, which searches packages and returns their information, and install, which installs a named package and can target a specific version. With it configured, a user can tell a compatible assistant things like &quot;install Firefox,&quot; &quot;find a free PDF reader,&quot; or &quot;install Git and Visual Studio Code&quot;; per the author, the AI calls WinGet to search and fetch package details, then installs after user confirmation. Setup requires Windows 10 1809 \(Build 17763\) or later plus a WinGet build with MCP support: running \`winget configure --enable\` and then \`winget mcp\` in PowerShell prints a JSON configuration containing the path to WindowsPackageManagerMCPServer.exe, while the error \`Unrecognized command: &\#x27;mcp&\#x27;\` signals the installed WinGet is too old. Microsoft documents two official routes — adding a stdio server entry to a project&\#x27;s \`.vscode/mcp.json\` and enabling winget-mcp in Copilot Chat&\#x27;s Agent mode, or the simpler \`/mcp add\` command in GitHub Copilot CLI. Only find and install are currently offered, so upgrading and uninstalling are not yet exposed.

**「Takeaway」** The author&\#x27;s point is that MCP lets an agent install the tools it discovers it needs mid-task — for instance while setting up a development environment — without burning extra tokens on workarounds, and he expects AI to control more of Windows over time. His hope is that Microsoft leans toward genuinely useful capabilities rather than forced integration, given how wary Windows users have become.

**Tags**: `#WinGet`, `#MCP`, `#Windows 包管理器`, `#AI Agent`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Taiwan stocks close up about 9%; TSMC hits limit-up](https://news.rthk.hk/rthk/ch/component/k2/1879065-20261124.htm) ⭐️ 8.0/10

Taiwan&\#x27;s TAIEX closed up 8.99%, or 3,310 points, at 40,122, according to RTHK. Heavyweight TSMC rose nearly 10% to its daily limit, though the report gave no reason for the surge.

rss · RTHK Finance · Nov 24, 06:19

**「Background」** Before the cash market opened, Taiwan futures had risen 3,170 points in the night session and TSMC briefly hit limit-up, according to a Goodinfo news roundup citing local reports. TSMC is a heavyweight in the TAIEX, so its near-10% limit-up move magnified the benchmark’s gain.

<details><summary>References</summary>
<ul>
<li><a href="https://goodinfo.tw/">首頁 - Goodinfo!台灣股市資訊網</a></li>

</ul>
</details>

**Tags**: `#Taiwan stocks`, `#TAIEX`, `#TSMC`, `#market surge`, `#limit up`

---

<a id="item-finance-news-2"></a>
### [AI selloff clouds DeepSeek, Moonshot and StepFun listing plans](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 8.0/10

A global AI selloff that followed Anthropic’s record $119.5 billion IPO is clouding planned or considered listings by Chinese AI developers DeepSeek, Moonshot and StepFun, Bloomberg reported, as Chinese tech stocks have shed $1.7 trillion in market value since the end of June.

telegram · zaihuapd · Nov 23, 09:31

**「Background」** Anthropic, the US developer of the Claude chatbot, is the reference point for the pullback: Chinese AI shares had rallied steeply beforehand — Zhipu gained 2,000% in the six months before its June peak — and the selloff is now unwinding those gains.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Anthropic">Anthropic - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#AI selloff`, `#Chinese tech stocks`, `#IPO market`, `#Anthropic`, `#DeepSeek`

---

<a id="item-finance-news-3"></a>
### [Fed’s Williams Says More Work Needed on Inflation](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

New York Fed President John Williams said more work is needed to bring inflation back to the Fed’s 2% target, indicating further rate increases can unfold over time. Markets fully price a quarter-percentage-point increase from the current 3.75%-4% target range at the Fed’s Dec. 8-9 meeting.

rss · CNBC Finance · Nov 23, 21:02

**「Background」** Williams has previously favored a measured approach, while other Fed officials have pushed for more aggressive rate increases as inflation stays above the 2% target.

**Tags**: `#Federal Reserve`, `#monetary policy`, `#inflation`, `#interest rates`, `#John Williams`

---

<a id="item-finance-news-4"></a>
### [Nvidia value climbs almost $1tn as tech stocks rally](https://www.bbc.co.uk/news/articles/cq62pn6j42jko?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

Nvidia&\#x27;s market value rose by almost $1 trillion and technology stocks rallied after Jensen Huang&\#x27;s return, with the Nasdaq up 6.5%, the BBC reported.

rss · BBC Business · Nov 23, 21:23

**「Background」** Nvidia designs graphics processing units used in AI and high-performance computing. The report does not specify the period over which the nearly $1tn value gain occurred or give the starting level for the Nasdaq&\#x27;s 6.5% rise.

**「Who is affected」** The rebound mattered most to ordinary investors holding broad US tech index funds, since the Nasdaq 100 had already fallen into a bear market — a drop of 20% or more from its recent peak — before Friday&\#x27;s sell-off, and the rally erased those losses.

<details><summary>References</summary>
<ul>
<li><a href="https://en.m.wikipedia.org/wiki/Nvidia">Nvidia - Wikipedia</a></li>
<li><a href="https://www.ft.com/content/20d2ebe3-e945-4659-a122-31bf85a4e4e5?syn-25a6b1a6=1">Nvidia live: Nvidia gains nearly $ 1 tn in value after Jensen Huang...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Nasdaq`, `#US equities`, `#technology sector`, `#market rally`

---

<a id="item-finance-news-5"></a>
### [Capita Shares Plunge 70% as CEO Quits After Civil Service Pension Delays](https://www.bbc.co.uk/news/articles/c65y1qqw3kjxo?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

Capita&\#x27;s shares reportedly fell 70% and its chief executive quit after delays to civil service pension payments under a scheme the outsourcing company has overseen since last year, the BBC reported. The report did not specify the share-price baseline, the number of affected workers, or the financial cost to Capita.

rss · BBC Business · Nov 23, 11:24

**「Background」** Capita took over administration of the Civil Service Pension Scheme in December last year, and a Cabinet Office minister last month called its progress on running the scheme “abysmal.” Capita has said it expects to lose up to £40m from the pension contract problems.

**「Impact」** Public-sector workers in the pension scheme Capita oversees face delayed payments, directly reducing household income for those affected.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/business/2026/nov/23/capita-boss-exits-shares-crash-civil-service-pensions-failures">Capita boss exits and shares crash after civil service pensions failures</a></li>
<li><a href="https://www.bbc.com/news/articles/c65y1qqw3kjxo">Capita shares plunge 70% as boss quits after civil service pensions ...</a></li>

</ul>
</details>

**Tags**: `#Capita`, `#pensions`, `#executive turnover`, `#share price`, `#public sector outsourcing`

---

<a id="item-finance-news-6"></a>
### [Hong Kong&\#x27;s first paperless IPO marks market infrastructure milestone](https://news.rthk.hk/rthk/ch/component/k2/1879060-20261124.htm) ⭐️ 7.0/10

Hong Kong&\#x27;s first IPO under its paperless securities regime listed, with Securities and Futures Commission Chairman Wong Tin-yau saying the new system lets investors hold shares electronically in their own names and supports future reforms such as the planned shortening of settlement from T+2 to T+1.

rss · RTHK Finance · Nov 24, 05:15

**「Background」** Hong Kong first raised the idea of a paperless securities market in 2002, and the regime, under which investors can no longer hold the relevant securities in paper form, took effect in early 2026 after the necessary legislation was passed; this was the first IPO under the new system.

**「Who is affected」** Investors buying into paperless IPOs will hold shares electronically in their own names rather than through paper certificates, which SFC Chairman Wong Tin-yau said gives them a more direct way to exercise shareholder rights, while listed companies gain an easier channel to communicate with shareholders.

<details><summary>References</summary>
<ul>
<li><a href="https://www.hk01.com/%E8%B2%A1%E7%B6%93%E5%BF%AB%E8%A8%8A/60230584/%E8%AD%89%E7%9B%A3%E6%9C%83%E6%8C%87%E8%AD%89%E5%88%B8%E5%B8%82%E5%A0%B4%E7%84%A1%E7%B4%99%E5%8C%962026%E5%B9%B4%E5%88%9D%E5%AF%A6%E6%96%BD">證 監 會 指 證 券 市 場 無 紙 化 2026 年初 實 施 | 香 港 01</a></li>
<li><a href="https://licenses.com.hk/article/5594610139481092">證 監 會 如期推進於 2026 年初 實 施 無 紙 證 券 市 場 制度的準備工作</a></li>

</ul>
</details>

**Tags**: `#香港證券市場`, `#無紙證券`, `#證監會`, `#市場基建`, `#T+1交收`

---

<a id="item-finance-news-7"></a>
### [Shanghai to Adjust Metro Fares for First Time in 21 Years](https://weibo.com/1699432410/5368461393397183) ⭐️ 7.0/10

Shanghai will adjust metro fares for the first time in 21 years beginning Dec. 1, setting a 3-yuan base fare for trips of 0–4 km and adding 1 yuan at set distance intervals thereafter, Xinhua reported. Multi-ride tickets and a 10% monthly discount after 90 yuan in same-channel spending are intended to reduce the impact on frequent riders.

telegram · zaihuapd · Nov 23, 10:45

**「Background」** Shanghai’s metro began operating in 1993, and its fares had not changed for 21 years before this adjustment, according to the source.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/wiki/%E4%B8%8A%E6%B5%B7%E5%9C%B0%E9%93%81%E8%BD%A6%E7%AB%99%E5%88%97%E8%A1%A8">上海地铁 车站列表 - 维基百科，自由的百科全书</a></li>

</ul>
</details>

**Tags**: `#Shanghai metro`, `#public transport fares`, `#commuting costs`, `#China policy`, `#fare adjustment`

---