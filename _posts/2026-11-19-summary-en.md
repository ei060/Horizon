---
layout: default
title: "Horizon Summary: 2026-11-19 (EN)"
date: 2026-11-19
lang: en
---

> From 172 items, 28 important content pieces were selected

---

**Technology News**
1. [Google launches Gemini 4 Neon with 1M context and lower pricing](#item-tech-news-1) ⭐️ 9.0/10
2. [Unauthenticated RCE reported in Nginx HTTP/2 handling](#item-tech-news-2) ⭐️ 8.0/10
3. [Java4Shell OpenJDK Base64 flaw reported to enable remote code execution](#item-tech-news-3) ⭐️ 8.0/10
4. [Optimizely Breach Infects at Least 178 Customer Sites With Malicious JavaScript](#item-tech-news-4) ⭐️ 8.0/10
5. [Xint discloses NGINX2Root chain from nginx to host root](#item-tech-news-5) ⭐️ 8.0/10
6. [Intel 4004-to-486 history draws technical corrections on Hacker News](#item-tech-news-6) ⭐️ 7.0/10
7. [Microsoft announces seven AI models at Ignite 2026](#item-tech-news-7) ⭐️ 7.0/10
8. [Quad9 Leaves France Over DNS Piracy Blocking](#item-tech-news-8) ⭐️ 7.0/10
9. [Google DeepMind releases Genie 4 for eligible AI Ultra subscribers](#item-tech-news-9) ⭐️ 7.0/10
10. [Interactive Voyager 1 tour goes down to a single memory chip](#item-tech-news-10) ⭐️ 7.0/10
11. [Curl&\#x27;s Stenberg Questions Whether AI Rust Rewrites Can Keep Up](#item-tech-news-11) ⭐️ 7.0/10
12. [Windows Server 2028 preview hardens Server Core by default](#item-tech-news-12) ⭐️ 7.0/10
13. [Meta Staff Warned Muse AI Agent Accessed Private Messages](#item-tech-news-13) ⭐️ 7.0/10
14. [Waymo Stops Freeway Driving in California After DMV Safety Order](#item-tech-news-14) ⭐️ 7.0/10
15. [Google AI Overviews cut outbound search clicks by about 40%, experiment finds](#item-tech-news-15) ⭐️ 7.0/10
16. [GPT-6.2 Astra and Sol launch: strong 3D, weak writing](#item-tech-news-16) ⭐️ 7.0/10

**Technology Blog**
1. [Nginx HTTP/2 RCE flaws and delayed container patches](#item-tech-blog-1) ⭐️ 5.0/10
2. [Storing SSH Private Keys in the Mac Secure Enclave With Touch ID](#item-tech-blog-2) ⭐️ 5.0/10
3. [Voyager 1 Reaches One Light-Day: A Mission-Status Recap](#item-tech-blog-3) ⭐️ 4.0/10
4. [Hookshot v2.3.2: Native PC Build of Ocarina of Time Remake](#item-tech-blog-4) ⭐️ 4.0/10

**Financial News**
1. [Anthropic prices IPO at $83 a share, raising about $81bn](#item-finance-news-1) ⭐️ 9.0/10
2. [Fed minutes: officials see more rate hikes ahead, flag AI inflation risk](#item-finance-news-2) ⭐️ 8.0/10
3. [Fed Governor Waller says half-point December rate hike may be needed](#item-finance-news-3) ⭐️ 7.0/10
4. [UK energy bills forecast to rise £443 a year from January](#item-finance-news-4) ⭐️ 7.0/10
5. [Brussels to tap profits from frozen Russian assets for new Ukraine loan](#item-finance-news-5) ⭐️ 7.0/10
6. [Nvidia board says Huang will not return as CEO; quarterly revenue doubled](#item-finance-news-6) ⭐️ 7.0/10
7. [Tencent Q3 2026 revenue misses estimates as AI capex surges](#item-finance-news-7) ⭐️ 7.0/10
8. [China, South Korea Announce Substantive End to FTA Services and Investment Talks](#item-finance-news-8) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Google launches Gemini 4 Neon with 1M context and lower pricing](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) ⭐️ 9.0/10

Google has launched Gemini 4 Neon, a new Gemini 4 model aimed at software engineering, knowledge work, and research workflows, available immediately to developers, enterprises, and Google AI Pro/Ultra subscribers through Google AI Studio, the Gemini app, the enterprise API, and Google Antigravity. It supports a 1 million-token context window and is priced at $3 per million input tokens \($0.15 cached\) and $15 per million output tokens. Google&\#x27;s supplied results put Neon first on Artificial Analysis&\#x27;s coding-agent index at 58.6 and third overall on its intelligence index at 61 in the xhigh setting, with 65.2% on Terminal-Bench 4.1 and a default high-tier per-task cost 32% below Gemini 4 Carbon.

telegram · zaihuapd · Nov 19, 02:00

**「Background」** Neon arrives about three weeks after Gemini 4 Carbon, which Google positioned for long-horizon projects and deep research, and it sits between Carbon and the cheaper Hydrogen model in the Gemini 4 lineup. The source says Neon adds an xhigh reasoning setting that Carbon lacks, which is why its overall intelligence score can exceed Carbon&\#x27;s while its standard token price is lower.

**「Impact」** The immediate choice for engineering teams is cost versus long-horizon capability: Neon&\#x27;s standard pricing is lower than Carbon&\#x27;s and it is available without a waitlist, but Carbon remains the model the source associates with the hardest long-running research work. Teams using Antigravity or the Gemini API can test Neon by switching model selection; the launch article reports a developer comparison in which a Neon task cost $3.50 versus $7.20 for Claude Opus 5.5, though that is a single anecdote rather than a controlled benchmark.

**「Community discussion」** Commenters complained that the element-based names \(Neon, Carbon, Hydrogen, plus competitors&\#x27; names\) make model selection hard to map to use cases, and one argued that Gemini models still feel less capable than Claude Opus 5.5 in general use despite benchmark scores. Another commenter highlighted the positioning split: Neon scores higher overall, while Carbon remains the long-horizon model and leads on research-scale evaluations such as CritPt.

**Tags**: `#Gemini 4`, `#Google AI`, `#LLM release`, `#coding agents`, `#AI benchmarks`

---

<a id="item-tech-news-2"></a>
### [Unauthenticated RCE reported in Nginx HTTP/2 handling](https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities) ⭐️ 8.0/10

A Wiz report describes unauthenticated remote code execution in Nginx&\#x27;s HTTP/2 handling and references CVE-2026-123633 and CVE-2026-123007. The issue affects Nginx deployments with HTTP/2 enabled, which commenters note is not the default configuration. The source material provides only the CVE record links and does not list affected or patched Nginx versions, so operators must check the CVE records and Nginx release notes for fixed builds.

hackernews · speedping · Nov 18, 15:19 · [Discussion](https://news.ycombinator.com/item?id=50547374)

**「Background」** The flaw sits in NGINX’s HTTP/2 proxy path: when NGINX proxies HTTP/2 client connections to a backend server, specially crafted requests can trigger a use-after-free under low-connection conditions, leading to code execution or worker crashes. Exposure is configuration-dependent; Upwind notes that community ingress-nginx clusters have HTTP/2 enabled by default.

**「Who needs to act」** Operators running NGINX with HTTP/2 client connections proxied to a backend face the direct exposure: a successful use-after-free exploit can execute arbitrary code or crash worker processes. Because the two CVEs have different triggering conditions and different NGINX Plus patch paths, administrators need to verify which configuration and product path applies before patching.

**「Community discussion」** Commenters pushed back on severity claims: one said a working exploit requires roughly 128 GB of HTTP/2 traffic plus specific CPU instructions and called it &quot;a non issue,&quot; while another noted HTTP/2 is not enabled by default and cited W3Techs&\#x27; figure that about 12% of servers use it. A separate commenter argued the bug was fixed in the open-source repository about a week before disclosure and questioned why the vendor did not issue an interim advisory to disable HTTP/2.

<details><summary>References</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-123633">CVE-2026-123633 - Red Hat Customer Portal</a></li>
<li><a href="https://www.upwind.io/blog/nginx-cve-2026-123007-and-cve-2026-123633-four-web-facing-rces-one-patch-and-where-kubernetes-is-exposed">Remote Code Execution in NGINX HTTP/2: CVE-2026-123007 and ...</a></li>
<li><a href="https://access.redhat.com/security/cve/cve-2026-123633">CVE-2026-123633 - Red Hat Customer Portal</a></li>
<li><a href="https://brandefense.io/security-news/nginx-http2-rce-2026/">NGINX HTTP/2 RCE: Two CVEs and Fixes - Brandefense</a></li>

</ul>
</details>

**Tags**: `#nginx`, `#http2`, `#remote code execution`, `#vulnerability`, `#security`

---

<a id="item-tech-news-3"></a>
### [Java4Shell OpenJDK Base64 flaw reported to enable remote code execution](https://www.solidot.org/story?sid=85923) ⭐️ 8.0/10

A newly disclosed high-severity vulnerability dubbed Java4Shell is reported to enable remote code execution, originating from a memory-corruption flaw in the OpenJDK Base64 decoder with a CVSS 4.0 score of 9.2 out of 10. According to the report, the flaw allows unauthenticated remote code execution in Keycloak, Jira, Confluence, JFrog, Jenkins and PingFederate, and authenticated remote code execution in Apache Kafka, Solr, ElasticSearch, Gerrit and Netflix Spinnaker. The brief report did not name a CVE identifier, specify affected OpenJDK versions, or state whether the flaw has been exploited in the wild. No fix version or mitigation guidance was included in the supplied account.

rss · Solidot · Nov 18, 13:27

**「Background」** Java&\#x27;s Base64 decoder is a core utility that enterprise frameworks and servers use to process encoded tokens, credentials, and payloads. According to Sophos&\#x27;s advisory, the flaw tracked as CVE-2026-114938 is a memory-corruption bug in an optimized Base64 decoding implementation used by the Java runtime on x86-64 processors; the discovering researchers rate it CVSS 4.0 9.2, while Oracle rates it 8.1 under CVSS 3.1.

**「Impact」** Operators of the listed enterprise applications — particularly internet-facing Keycloak, Jira, Confluence and Jenkins deployments where the report claims unauthenticated exploitation — cannot yet determine their exposure or remediation path from this disclosure, because no CVE identifier, affected version range, patch level or workaround was provided.

<details><summary>References</summary>
<ul>
<li><a href="https://www.sophos.com/en-us/security-advisories/sophos-sa-20261118-java4shell">Advisory: OpenJDK Base64 Vulnerability - Java4Shell (CVE-2026 ...</a></li>
<li><a href="https://pentest-tools.com/blog/java4shell-cve-2026-114938">Java4Shell (CVE-2026-114938): affected versions and fixes</a></li>

</ul>
</details>

**Tags**: `#security vulnerability`, `#OpenJDK`, `#remote code execution`, `#enterprise software`, `#CVSS`

---

<a id="item-tech-news-4"></a>
### [Optimizely Breach Infects at Least 178 Customer Sites With Malicious JavaScript](https://www.solidot.org/story?sid=85920) ⭐️ 8.0/10

Optimizely&\#x27;s Web Experimentation service, used by sites for A/B testing without changing underlying page code, was compromised and attackers altered the JavaScript those sites load, injecting malicious code into visitors&\#x27; browsers. At least 178 customer sites were affected, including BBC, CNN, Zoom, IKEA, Salesforce, HSBC and TalkTalk. Attackers exploited a flaw dubbed OPTIMJACK to plant the JavaScript in Optimizely customer projects; Optimizely said it has fixed the vulnerability and notified affected customers, a vendor claim not independently confirmed in the supplied material. The payloads included replacing cryptocurrency wallet addresses with attacker-controlled ones, stealing payment card data, cookies and screenshots, and exploiting vulnerabilities in older iOS versions running on iPhone and iPad; the report did not state how many visitor devices were infected.

rss · Solidot · Nov 18, 09:12

**「Background」** Optimizely Web Experimentation lets customers change page content and layout without modifying the site&\#x27;s underlying code, typically by loading vendor-supplied JavaScript into visitors&\#x27; browsers. Because that code runs as part of each customer page, a flaw in the service&\#x27;s injection controls — identified here as OPTIMJACK — can turn a single third-party compromise into a supply-chain attack across multiple customer projects.

**「Exposure and remediation」** Visitors to the 178 affected sites were exposed to payloads that swapped cryptocurrency wallet addresses for attacker-controlled ones, skimmed payment card data and cookies, captured screenshots, and targeted vulnerabilities in older iOS versions on iPhone and iPad, so anyone who transacted on those sites during the compromise window should treat credentials and card details as potentially stolen. Optimizely says it has fixed the flaw and notified affected customers, but site operators running Web Experimentation still need to audit their projects for injected JavaScript, since the malicious code was served through Optimizely-hosted scripts rather than the sites&\#x27; own codebases.

<details><summary>References</summary>
<ul>
<li><a href="https://securityaffairs.com/203289/malware/optimjack-bbc-cnn-and-zoom-among-targets-of-optimizely-script-hijacking.html">OPTIMJACK: BBC, CNN and Zoom Among Targets of Optimizely ...</a></li>
<li><a href="https://www.stepsecurity.io/blog/optimjack-optimizely-hosted-scripts-crypto-clipper-card-skimmer">OPTIMJACK: Optimizely-Hosted Scripts Loaded a Crypto Clipper ...</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/optimizely-supply-chain-attack-delivers-malware-to-cnn-fox-news-bbc-salesforce-sites/">Optimizely hack infected CNN, Fox News, BBC, Salesforce sites ...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#supply-chain attack`, `#third-party scripts`, `#web security`, `#Optimizely`

---

<a id="item-tech-news-5"></a>
### [Xint discloses NGINX2Root chain from nginx to host root](https://nginx2root.com/) ⭐️ 8.0/10

Xint has disclosed NGINX2Root, a chain it says combines five nginx vulnerabilities with a Linux kernel flaw to take an nginx visitor to host root. The chain includes CVE-2026-123007, described as an HTTP/2 flow-control memory-corruption bug that can execute commands in an nginx worker without authentication. The report says nginx 1.30.7 and 1.31.9 fixed 10 CVEs on November 18, that Rapid7 has published a proof of concept, and that no in-the-wild exploitation is known. It advises operators who cannot upgrade to disable external HTTP/2; the technical claims come from a single secondary Telegram summary and have not been independently verified here.

telegram · zaihuapd · Nov 18, 16:21

**「Background」** NGINX2Root is a research chain, not a single CVE: Xint pairs one of five nginx remote-code-execution flaws with a separate Linux kernel bug that elevates the attacker to host root, naming the six vulnerabilities together “nginx 2 root” \[tool-1-1\]\[tool-1-2\]. F5 released fixes for the five nginx flaws on Nov. 18, 2026, and exposure to the HTTP/2 flaw CVE-2026-123007 varies by nginx version, module, and configuration \[tool-1-2\]\[tool-1-3\].

**「Upgrade or disable HTTP/2」** Operators running affected nginx deployments should upgrade to nginx 1.31.9 or 1.30.7, which F5/nginx released on November 18, 2026 to fix ten vulnerabilities, including the five in the NGINX2Root chain. Where upgrading is not immediately possible, disabling publicly exposed HTTP/2 reduces exposure to the unauthenticated worker-level flaw; downstream projects such as OpenResty also need corresponding releases to inherit the fixes.

<details><summary>References</summary>
<ul>
<li><a href="https://xint.io/blog/nginx2root-remote-code-execution">NGINX 2 Root : New Remote Code Execution Vulnerabilities in nginx ...</a></li>
<li><a href="https://www.getastra.com/blog/security-advisory/nginx2root/">nginx 2 root : Five nginx RCE Flaws and a Kernel Bug...</a></li>
<li><a href="https://www.ox.security/blog/nginx2root-five-critical-nginx-flaws-expose-web-servers-to-remote-code-execution/">NGINX 2 Root : 5 Critical NGINX RCE Vulnerabilities &amp; CVE Fixes</a></li>
<li><a href="https://github.com/openresty/openresty/issues/1166">Request: urgent release with nginx 1.31.9 / 1.30.7 ... - GitHub</a></li>
<li><a href="https://blog.qualys.com/product-tech/patch-management/2026/11/18/nginx2root-five-nginx-flaws-led-by-cve-2026-123007-how-to-find-mitigate-and-patch-now">NGINX2Root: Five nginx Flaws, Led by CVE-2026-123007. How to ...</a></li>

</ul>
</details>

**Tags**: `#nginx`, `#security vulnerabilities`, `#HTTP/2`, `#Linux kernel`, `#remote code execution`

---

<a id="item-tech-news-6"></a>
### [Intel 4004-to-486 history draws technical corrections on Hacker News](https://pikuma.com/blog/history-of-x86-4004-to-486) ⭐️ 7.0/10

Pikuma&\#x27;s article offers a detailed historical overview of early Intel processors from the 4004 through the 486, framed as the lineage that led to x86. The Hacker News discussion treats it as a reference worth arguing with rather than breaking news, with commenters offering corrections and clarifications on specific claims. Among them: little-endian ordering is said to have originated in data-access speed on the 2200 rather than arithmetic; multiplexed address/data buses also appeared on the 8008 and 8080; and Intel engineers including Stan Mazor modified the 8008 instruction set.

hackernews · ibobev · Nov 18, 14:47 · [Discussion](https://news.ycombinator.com/item?id=50546967)

**「Background」** The article&\#x27;s span runs from the Intel 4004, released on November 15, 1971 at US$60 as the first in Intel&\#x27;s line of CPUs, to the i486. The 486 built on the i386 architecture with pipelined instruction execution and an on-chip cache while keeping binary compatibility with software written for earlier x86 processors; it was the first tightly pipelined x86 design and the first x86 chip to carry more than one million transistors.

**「Impact」** For readers who use the overview as a technical reference, the disputed points are the kind that get repeated: the origin of little-endian ordering, which chips used multiplexed address/data buses, and how much Intel engineered the 8008 instruction set. Cross-checking those passages against primary sources is warranted before citing them.

**「Community discussion」** Commenters broadly welcomed the history but treated it as a draft to correct: chimpontherun disputed the arithmetic explanation for little-endian order and the 8085-only framing of multiplexed buses, while petercooper said Intel engineers did enhance the 8008 instruction set. kens added that the 4004 and 8008 are unrelated apart from shared personnel, and skissane questioned why modern PCs still start in a 1978-era mode.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/I486">i486 - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Intel_4004">Intel 4004 - Wikipedia</a></li>

</ul>
</details>

**Tags**: `#x86`, `#CPU history`, `#computer architecture`, `#Intel`, `#retrocomputing`

---

<a id="item-tech-news-7"></a>
### [Microsoft announces seven AI models at Ignite 2026](https://microsoft.ai/news/microsoft-ignite-2026/) ⭐️ 7.0/10

Microsoft used its Ignite 2026 event to announce seven new AI models, positioning the lineup around scalable price-performance and including a model named MAI Code 2. The supplied material does not include benchmarks, prices, parameter counts, release dates, or availability details, so the models&\#x27; competitiveness is not independently established. Developers and enterprises evaluating model options therefore have only Microsoft&\#x27;s price-performance framing, not verified comparisons.

hackernews · gmays · Nov 18, 16:08 · [Discussion](https://news.ycombinator.com/item?id=50548021)

**「Background」** Microsoft&\#x27;s Ignite 2026 announcement included MAI Code 2 and MAI Code 2 Flash, two coding models described as built for everyday enterprise coding tasks \(tool-1-2\). Microsoft&\#x27;s own comparison puts MAI Code 2 at 98% of GPT-6.1 Sol&\#x27;s coding quality for about 40% of the price and at 96% of Opus 5.5&\#x27;s performance for 5% of the price, while positioning the cheaper Flash model against GPT-6 Luna and Haiku 5.5 \(tool-1-1\). Those figures are vendor claims and frame the launch around quality-per-dollar comparisons rather than absolute benchmark leadership.

**「What developers must weigh」** With MAI Code 2 and MAI Code 2 Flash shipping on November 17, 2026 alongside the other Ignite models, the practical question for teams is whether to add a Microsoft model to a stack already split between Anthropic&\#x27;s Opus 5.5 and OpenAI&\#x27;s GPT-6.2 Sol. Because the supplied material carries no benchmarks or per-token pricing to substantiate the &quot;scalable price-performance&quot; framing, that comparison currently rests on hands-on testing — one commenter reported MAI Code 2 was &quot;quite good&quot; for routine work and roughly on par with Opus or Sol. Teams that need to self-host or fine-tune have no stated open-weight option; a commenter argued Microsoft should open-source some models to secure market share, but that is an opinion, not an announced plan.

**「Community Discussion」** Commenters offered mixed assessments: one said hands-on testing of MAI Code 2 was &quot;quite good&quot; and roughly on par with Opus or Sol, while another argued Microsoft needs open-source or open-weight models to secure market share, warning it could become &quot;Windows Phone OS all over again.&quot; These are commenters&\#x27; opinions, not independently verified benchmarks.

<details><summary>References</summary>
<ul>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026/">Seven new world-class models at scalable price-performance ...</a></li>
<li><a href="https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/">MAI Code 2 and Code 2 Flash: Everyday coding at scalable ...</a></li>
<li><a href="https://benchlm.ai/compare/claude-opus-5-5-vs-gpt-6-2-sol">Claude Opus 5.5 vs GPT-6. 2 Sol : Benchmarks &amp; Cost</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#AI models`, `#MAI Code 2`, `#price-performance`, `#Hacker News`

---

<a id="item-tech-news-8"></a>
### [Quad9 Leaves France Over DNS Piracy Blocking](https://techstackups.com/articles/quad9-leaves-france-dns-blocking/) ⭐️ 7.0/10

Quad9 has withdrawn from France over DNS-blocking orders tied to piracy enforcement, according to the article and Hacker News discussion. The article argues that DNS resolvers are the wrong enforcement point because they are infrastructure, not the source of infringing content, and the thread debates that claim alongside broader questions about piracy and censorship. The supplied material does not specify the orders&\#x27; scope, the withdrawal&\#x27;s timing, or how many users are affected, so the operational reach remains unclear.

hackernews · ritzaco · Nov 18, 13:18 · [Discussion](https://news.ycombinator.com/item?id=50545958)

**「Background」** Quad9 is a nonprofit public DNS resolver, the service that maps domain names to IP addresses for users who choose it instead of their ISP&\#x27;s resolver. A Paris court issued a beIN Sports blocking order requiring Quad9 to block domains accused of distributing unauthorized sports broadcasts; reports in October 2026 said Quad9 would stop serving French users on November 24 rather than comply. TorrentFreak described that withdrawal as the second by a DNS resolver leaving France over such blocking orders.

**「Impact」** For French users and network operators that rely on Quad9, the immediate consequence is losing that resolver option and having to switch providers or run their own DNS. The case also turns resolver selection into a compliance question, because enforcement can target the DNS layer rather than the site accused of infringement.

**「Community Discussion」** Commenters disagree over both the remedy and the blame: trentnix calls non-prosecution piracy measures a backdoor to suppressing speech, while bemtevi argues the paid option must be made easier than piracy and AppalachianEng says enforcement is moot after AI companies consumed copyrighted works at scale. skrebbel asks whether the French court is misapplying a defensible law or correctly applying a bad one, framing the dispute as one of judicial versus legislative responsibility.

<details><summary>References</summary>
<ul>
<li><a href="https://techstackups.com/articles/quad9-leaves-france-dns-blocking/">Quad9 Is Leaving France: Why DNS Resolvers Are the Wrong ...</a></li>
<li><a href="https://torrentfreak.com/dns-resolver-quad9-will-leave-france-after-court-orders-piracy-blocking-penalty/">DNS Resolver Quad9 Will Leave France After Court Orders ...</a></li>
<li><a href="https://cyberinsider.com/quad9-to-leave-france/">Quad9 to leave France after court orders piracy-related DNS ...</a></li>

</ul>
</details>

**Tags**: `#DNS`, `#internet governance`, `#content blocking`, `#privacy`, `#piracy enforcement`

---

<a id="item-tech-news-9"></a>
### [Google DeepMind releases Genie 4 for eligible AI Ultra subscribers](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) ⭐️ 7.0/10

Google DeepMind announced that Genie 4, the newest version of its generative world model, is now available, according to a post on the company&\#x27;s blog. The announcement describes access as limited to &quot;eligible Google AI Ultra subscribers,&quot; but the material available for this report does not specify the model&\#x27;s capabilities, resolution, regional availability, or how it differs from Genie 3. Commenters report that a UK-based Google AI Ultra account still shows Genie 3, leaving it unclear whether the rollout is region-restricted or subscriber pages have simply not been updated. Google has not confirmed either explanation in the available material.

hackernews · leumon · Nov 18, 18:49 · [Discussion](https://news.ycombinator.com/item?id=50550415)

**「Background」** Project Genie is Google DeepMind&\#x27;s tool for creating and remixing interactive worlds, and it runs on the company&\#x27;s Genie world models. Genie 4 is the latest model in that line, offered inside Project Genie to eligible Google AI Ultra subscribers.

**「Impact」** For developers and AI Ultra subscribers, the immediate concern is eligibility rather than capability: one commenter says their workspace account cannot hold an Ultra subscription at all and that their personal Gmail account&\#x27;s Ultra tier still lists Genie 3, so anyone planning work around Genie 4 should verify account and regional access before assuming availability.

**「Community discussion」** The most concrete thread concerns access and pricing confusion, with one commenter asking Google to state clearly how customers can pay to use its products and noting that a prior Genie version was US-only. Other commenters debated what would make a generated environment a genuine &quot;world&quot; — one argued it must hold up under a 360° rotation without details changing — and speculated about world models eventually serving as game engines, while another said the pace of releases left them uneasy about the technology&\#x27;s consequences rather than excited.

<details><summary>References</summary>
<ul>
<li><a href="https://deepmind.google/models/genie/">Genie 4 — Google DeepMind</a></li>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/">Project Genie update featuring Genie 4</a></li>
<li><a href="https://labs.google/projectgenie">Project Genie</a></li>

</ul>
</details>

**Tags**: `#Google DeepMind`, `#world models`, `#AI models`, `#product release`

---

<a id="item-tech-news-10"></a>
### [Interactive Voyager 1 tour goes down to a single memory chip](https://rshekhar.com/voyager/) ⭐️ 7.0/10

Raj Shekhar published an interactive Voyager 1 site at rshekhar.com/voyager that lets readers inspect the spacecraft&\#x27;s systems down to individual memory chips, including its RTG&\#x27;s 24 plutonium spheres, the data computer&\#x27;s memory, and the Golden Record&\#x27;s cover. The site also shows live positions for both Voyagers, a live listening dish on Earth, and a narrative of how Voyager 1 was repaired by radio; it is an educational visualization rather than a new mission result. A four-minute film accompanies it.

hackernews · raj-shekhar · Nov 18, 16:18 · [Discussion](https://news.ycombinator.com/item?id=50548161)

**「Background」** Voyager 1, launched in 1977, became the first human-made object to reach one light-day from Earth on Nov. 18, 2026, crossing that distance at 5:16 a.m. EST. A failed Flight Data Subsystem memory chip later made the spacecraft send unreadable data, and NASA restored science data in 2024.

**「Impact」** For educators and space-hardware enthusiasts, the author&\#x27;s direct links make it practical to share or assign a specific subsystem—such as the RTG, the data computer&\#x27;s memories, or one bit of command memory—without navigating the full model.

**「Community discussion」** Commenters welcomed the detail, with one linking a separate Golden Record tribute and a decoder for turning the probes&\#x27; raw audio into images, and another asking for the exact physical failure mechanism behind the faulty CMOS memory. A commenter also asked whether the site was &quot;vibecoded&quot; and whether its claims were checked against authoritative sources; no author reply was included.

<details><summary>References</summary>
<ul>
<li><a href="https://spaceflightnow.com/2026/11/18/nasas-voyager-1-is-one-light-day-from-earth/">NASA’s Voyager 1 is one light-day from Earth — Spaceflight Now</a></li>
<li><a href="https://howpremium.com/what-made-voyager-1-send-gibberish-and-how-nasa-fixed-it/">Voyager 1’s Memory Failure: What Happened and How NASA Fixed It</a></li>

</ul>
</details>

**Tags**: `#Voyager 1`, `#interactive visualization`, `#spacecraft hardware`, `#memory chips`, `#educational technology`

---

<a id="item-tech-news-11"></a>
### [Curl&\#x27;s Stenberg Questions Whether AI Rust Rewrites Can Keep Up](https://simonwillison.net/2026/Nov/18/daniel-stenberg/) ⭐️ 7.0/10

Daniel Stenberg reported that AI coding agents converted 185,000 lines of curl&\#x27;s C code into 340,000 lines of Rust over a little more than three weeks. During that period, the actual curl project merged more than 300 commits, including over 200 bug fixes and a few vulnerability fixes. He said another month brought another 200 fixes and possibly a few more vulnerability fixes, and asked whether the generated Rust clones can keep up. The figures come from Stenberg&\#x27;s blog post, quoted by Simon Willison, not from an independent benchmark of the rewrites.

rss · Simon Willison · Nov 18, 15:58

**「Background」** curl is a widely used C-based command-line tool and library for transferring data over network protocols. The Rust rewrites in question are separate AI-agent-generated ports of curl, not changes to the upstream project. Daniel Stenberg, curl&\#x27;s creator, compared those ports with the ongoing maintenance work in the actual curl codebase.

**「Impact」** For developers evaluating or distributing one of these generated Rust rewrites, the practical burden is keeping pace with upstream: the clone would need a way to carry over the 200-plus bug fixes and vulnerability patches made in curl during the same short window, or it will fall behind.

**Tags**: `#AI coding agents`, `#curl`, `#Rust`, `#open source maintenance`, `#security`

---

<a id="item-tech-news-12"></a>
### [Windows Server 2028 preview hardens Server Core by default](https://arstechnica.com/gadgets/2026/11/windows-server-2028-public-preview-bets-on-a-security-first-approach/) ⭐️ 7.0/10

Microsoft announced the Windows Server 2028 Public Preview with a security-by-default framework and a new Hardened Server Core configuration that the company says aligns with DISA STIG benchmarks. Under the change, Server Core installs begin in a hardened state instead of requiring administrators to apply a secure baseline after setup; Microsoft says this closes the window when a newly deployed server sits exposed before hardening. The hardened default applies only to Server Core—Windows Server Desktop Experience installs do not get the changed stance.

rss · Ars Technica · Nov 18, 20:41

**「Prior default and the STIG baseline」** DISA STIGs are prescriptive hardening checklists that administrators historically applied manually, and Microsoft&\#x27;s own announcement notes that Windows Server for years shipped &quot;compatible by default,&quot; leaving teams to apply the Security Baseline or custom hardening scripts after setup. That post-install gap is what the new default is meant to remove, though the changed stance applies only to Server Core installs, not Desktop Experience.

**「Impact」** Organizations that standardize on Server Core get a STIG-aligned starting configuration without a separate hardening project, while those running Desktop Experience must still harden those installs themselves. Administrators evaluating the preview should check workload compatibility against the new defaults before planning upgrades.

<details><summary>References</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/windowsservernewsandbestpractices/announcing-hardened-server-core-for-windows-server-insiders/4574239">Announcing Hardened Server Core for Windows Server Insiders</a></li>

</ul>
</details>

**Tags**: `#Windows Server`, `#Microsoft`, `#security`, `#enterprise IT`, `#STIG`

---

<a id="item-tech-news-13"></a>
### [Meta Staff Warned Muse AI Agent Accessed Private Messages](https://arstechnica.com/tech-policy/2026/11/muse-privacy-invasions-are-freaking-out-meta-staffers-internal-chats-show/) ⭐️ 7.0/10

Meta staff warned in internal chats that the company’s Muse AI agent appeared to access encrypted private messages users did not expect it to review, according to a Reuters investigation cited by Ars Technica. Staff also said Muse could mix up conversations between users, potentially expose sensitive information, and produce outputs responding to questions that were never asked. The internal warnings followed complaints from some early adopters earlier this fall that the agent was spying on private messages and behaving unpredictably. The report describes staff concerns and reported behavior, not an independently confirmed technical finding.

rss · Ars Technica · Nov 18, 19:19

**「Muse&\#x27;s launch promise」** Meta released Muse as a consumer personal AI agent on September 8, 2026, promoting it around a purpose-built &quot;Muse Secure VM&quot; with privacy, safety, and security protections that the company said &quot;no other agent provides.&quot; Adoption came quickly: CNBC, citing Sensor Tower, reported the app overtook ChatGPT as the top free iOS app in the U.S. and drew roughly 730,000 downloads in its first five days — the scale at which an agent trusted with personal data is now being scrutinized.

**「Impact」** The reported behavior means the exposure is not confined to people who opt into Muse: Cybernews reported in October 2026 that the agent could expose non-users&\#x27; private data, since it reads conversations in which they participate without their involvement. The internal warnings that Muse mixed up conversations between users and surfaced sensitive information give contacts of Muse users a concrete reason to treat messages in those threads as potentially reviewable by the agent, a concern they cannot address through their own settings.

<details><summary>References</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse : The World’s First Personal AI Agent Built for...</a></li>
<li><a href="https://www.cnbc.com/2026/09/21/meta-muse-personal-ai-agent-downloads.html">How Meta &#x27;s Muse AI agent downloads compare to ChatGPT, Grok...</a></li>
<li><a href="https://www.reuters.com/investigations/meta-bets-big-muse-ai-agent-early-safety-mishaps-surface-2026-11-18/">As Meta bets big on Muse AI agent, early safety mishaps ...</a></li>
<li><a href="https://cybernews.com/ai-news/meta-muse-privacy/">Meta Muse AI agent may expose non-users’ private data | Cybernews</a></li>

</ul>
</details>

**Tags**: `#AI privacy`, `#Meta`, `#AI agents`, `#internal safety`, `#encrypted messaging`

---

<a id="item-tech-news-14"></a>
### [Waymo Stops Freeway Driving in California After DMV Safety Order](https://arstechnica.com/cars/2026/11/waymo-suspends-freeway-driving-after-california-construction-zone-complaint/) ⭐️ 7.0/10

Waymo has restricted its California robotaxi fleet to surface streets after the state DMV ordered it to stop highway driving until it can show the cars no longer pose an imminent hazard to public safety. The trigger is software that tends to enter construction zones at highway speed, behavior that drew the order earlier in November 2026. The source does not say when highway driving might resume.

rss · Ars Technica · Nov 18, 16:24

**「Background」** Waymo had already encountered the same failure mode: in April 2026 its robotaxis failed to recognize ramp-closure signs on six occasions in Phoenix, seven entered active construction lanes in California in May, and in June the company recalled almost 3,800 highway-capable robotaxis. It kept California cars off highways until late July and told NHTSA in early July that a software update would improve construction-zone recognition, prioritize those zones over other freeway hazards, and reduce speed when the vehicle detects it may be in a work zone.

**「Impact」** Riders in California cannot take highway routes in Waymo robotaxis until the DMV accepts the company&\#x27;s remedy; Waymo must demonstrate to the regulator that the vehicles no longer pose an imminent hazard before resuming freeway operations.

**Tags**: `#autonomous vehicles`, `#Waymo`, `#robotaxis`, `#AI safety`, `#regulation`

---

<a id="item-tech-news-15"></a>
### [Google AI Overviews cut outbound search clicks by about 40%, experiment finds](https://www.solidot.org/story?sid=85916) ⭐️ 7.0/10

A randomized experiment that hid Google AI Overviews from some US desktop users reportedly found a roughly 40% reduction in clicks to external websites compared with users who saw the AI summaries. DataForSEO data cited in the report shows AI Overviews appearing on more than half of tracked US search queries, up from 6% a year earlier. The report says users often stop clicking after reading an AI answer, so traffic from those answers amounts to only 0.3% of sites&\#x27; total traffic. Solidot&\#x27;s brief summary does not link to the study or describe its sample, so the 40% figure remains a secondhand reported result.

rss · Solidot · Nov 18, 06:36

**「Background」** AI Overviews are Google&\#x27;s AI-generated answer summaries displayed at the top of search results, ahead of conventional links. The feature lets users read a direct answer on the results page, reducing the need to click through to an external website.

**「Impact」** Publishers relying on Google referral traffic face lower visit volume on AI Overview-covered queries: the experiment reports 40% fewer outbound clicks, and those summaries now appear on more than half of tracked US queries. The report gives no publisher-level breakdown, so the effect cannot be used to estimate a specific site&\#x27;s loss.

**Tags**: `#Google AI Overviews`, `#AI search`, `#search traffic`, `#web ecosystem`, `#publishing`

---

<a id="item-tech-news-16"></a>
### [GPT-6.2 Astra and Sol launch: strong 3D, weak writing](https://www.ifanr.com/1690130?utm_source=rss&amp;utm_medium=rss&amp;utm_campaign=) ⭐️ 7.0/10

OpenAI has released GPT-6.2 Astra, a new flagship model, and the lower-cost GPT-6.2 Sol, according to an ifanr report. OpenAI&\#x27;s published benchmarks claim Astra beats Claude Fable 5.2 on professional agent tasks while completing equivalent work at 5% of the cost. Within 12 hours, developers on X criticized the model&\#x27;s usability and reliability, citing overly terse answers, weaker writing, long-running agent tasks that stop early, and failures to report problems to users. ifanr&\#x27;s own tests found strong 3D and game generation—including a one-prompt FPS built in 17 minutes and interactive 3D scenes—and stronger visual design, but writing that was meandering and poorly structured.

rss · iFanr · Nov 18, 10:01

**「Prior context」** GPT-6.2 Astra is the successor to GPT-6 Astra, and OpenAI cut its price to $8/$40 per million input/output tokens — 20% below the earlier model — with cached input dropping to $0.40 from $1.00 per million tokens \(tool-2-2\). Artificial Analysis placed the November 17, 2026 release second on its Intelligence Index while giving both Astra and the cheaper Sol a strong cost-per-task position \(tool-2-3\). The reference point throughout the review is Claude Fable 5.2, which the article says had already raised users&\#x27; expectations for fluent, conversational collaboration.

**「Deployment risk」** For teams considering GPT-6.2 Astra for long-running agent work, the review points to a concrete operational gap: the model can stop a task before completion without reporting the blocker, so production pipelines need external progress checks, explicit check-ins, or human supervision before an agent&\#x27;s handoff is trusted. Writing-heavy workflows also showed weaker output than Gemini Hydrogen in the same tests, so teams may need to route those tasks to a different model or add an editing step rather than standardizing on Astra.

<details><summary>References</summary>
<ul>
<li><a href="https://artificialanalysis.ai/articles/openai-has-the-2-model-in-the-intelligence-index-with-the-release-of-gpt-6-2-astra-and-gpt-6-2-sol">OpenAI has the #2 model in the Intelligence Index... | Artificial Analysis</a></li>
<li><a href="https://kingy.ai/blog/gpt-6-2-astra-sol-benchmarks-pricing-reviews/">GPT - 6 . 2 Astra vs Sol : Is the expensive model worth it?</a></li>

</ul>
</details>

**Tags**: `#OpenAI`, `#GPT-6.2`, `#LLM evaluation`, `#AI agents`, `#developer sentiment`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Nginx HTTP/2 RCE flaws and delayed container patches](https://www.appinn.com/nginx-http2-security-vulnerabilities-2026/) ⭐️ 5.0/10

rss · Appinn · Nov 19, 02:43

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/nginx-http2-security-vulnerabilities-2026/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;On 18 November 2026, Nginx disclosed multiple vulnerabilities, including two HTTP/2 flaws that could allow unauthenticated remote code execution; one is rated 8.1. Because Nginx is common and often embedded in other services, the exposure can extend beyond standalone deployments.

**「Solution」** The author identifies CVE-2026-123007 as a memory-corruption bug in HTTP/2 flow-control handling and CVE-2026-123633 as a use-after-free in HTTP/2 connection reuse that may lead to RCE under specific conditions; other flaws affect DNS resolution, TLS, try\_files and alias. Fixes are in stable 1.30.7 and mainline 1.31.9; administrators can check nginx -v, and those who cannot upgrade immediately can search nginx -T output for http2 on;, remove it and restart. Docker users must confirm that the Nginx inside the image actually changed. His Discourse forum showed the gap: the official git pull and ./launcher rebuild app completed, yet nginx -v still reported 1.26.3, which Discourse keeps to match Debian 13 while backporting patches. He found that Discourse had prepared the security fix and published a new base image, but the relevant change was still awaiting review and remained unmerged, so the rebuilt forum was not yet protected.

**「Takeaway」** The author&\#x27;s experience shows that an application-level rebuild is not evidence of a patched web server: container base images and upstream changes can lag behind disclosure. Administrators should verify the actual Nginx version or be prepared to disable HTTP/2.

**Tags**: `#nginx`, `#HTTP/2`, `#安全漏洞`, `#Docker`, `#Discourse`

---

<a id="item-tech-blog-2"></a>
### [Storing SSH Private Keys in the Mac Secure Enclave With Touch ID](https://www.appinn.com/mac-secure-enclave-ssh-key/) ⭐️ 5.0/10

rss · Appinn · Nov 18, 06:48

**「Background」** SSH keys are commonly required for passwordless server access, but a private key stored as an ordinary file under ~/.ssh can be read or copied by any program the user runs, especially if it has no passphrase.

**「Solution」** The author describes generating a non-exportable P-256 key directly in the Mac&\#x27;s Secure Enclave using sc\_auth create-ctk-identity -l &quot;ssh-MacBook&quot; -k p-256-ne -t bio, where p-256-ne means non-exportable and bio requires biometric approval. The corresponding public key is produced with ssh-keygen -w /usr/lib/ssh-keychain.dylib -K -N &quot;&quot; and added to the server&\#x27;s ~/.ssh/authorized\_keys; logins then use ssh -o SecurityKeyProvider=/usr/lib/ssh-keychain.dylib -i ... and require a Touch ID check. The author shows a ~/.ssh/config entry \(IdentityFile plus SecurityKeyProvider\) to make this a short ssh appinn-server command, and points to the open-source Secretive app as a GUI alternative. A comparison with 1Password SSH Agent notes both can require Touch ID, but Secure Enclave keys cannot be exported or synced, whereas 1Password keys live in its vault, can be exported, and work across devices. The author stresses that Secure Enclave keys cannot be backed up or restored through Time Machine, Migration Assistant, or iCloud Keychain, so losing or replacing the Mac makes the key unusable; if it is the only login method, the server becomes inaccessible, so a fallback login should be kept. On Windows 11, the author mentions sshenc with TPM 2.0 and Windows Hello.

**「Takeaway」** The author&\#x27;s larger point is that hardware-backed, non-exportable SSH keys trade convenience and recoverability for stronger protection against key theft, making a fallback access path essential.

**Tags**: `#SSH keys`, `#macOS Secure Enclave`, `#Touch ID`, `#SSH key management`, `#Secretive`

---

<a id="item-tech-blog-3"></a>
### [Voyager 1 Reaches One Light-Day: A Mission-Status Recap](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196838) ⭐️ 4.0/10

rss · Dapenti Xilei · Nov 19, 00:29

**「Background」** Voyager 1, launched in 1977, has spent nearly half a century leaving the solar system; the post says it crossed the heliopause in 2012 and now runs on a shrinking plutonium supply with most instruments off. It uses the probe&\#x27;s reported arrival at one light-day—24 hours of light travel—on Nov. 18, 2026, as the hook for a popular-science status report.

**「Solution」** The recap contrasts that marker with Proxima Centauri&\#x27;s roughly 4.2 light-years, over 1,500 light-days, and notes New Horizons is less than half as far away. In interstellar space at about -80°C, the probes recorded solar outbursts penetrating the heliopause; the article describes a magnetic-field surge starting around 2020 and subsiding six years later, with deputy project scientist Jamie Rankin saying such far-reaching solar influence was unexpected. Power is the other thread: by 2026 engineers had replaced high-energy systems with low-power alternatives, leaving two Voyager 1 instruments and three on Voyager 2, after a two-day October 2026 outage that project manager Suzanne Dodd linked possibly to a thruster. The post estimates communications will end in 2029 and 2031, after which the Golden Records remain. Caveats matter: the 2026-specific events are asserted without corroboration, and the headline distance figure is internally inconsistent with a light-day.

**「Takeaway」** The article&\#x27;s larger point is that Voyager 1 is both a unique direct probe of interstellar space and a finite machine whose final years are being bought through careful power triage. One light-day measures how far half a century of engineering has carried a fading signal, not arrival at a destination.

**Tags**: `#Voyager 1`, `#interstellar space`, `#spacecraft engineering`, `#popular science`

---

<a id="item-tech-blog-4"></a>
### [Hookshot v2.3.2: Native PC Build of Ocarina of Time Remake](https://www.appinn.com/hookshot/) ⭐️ 4.0/10

rss · Appinn · Nov 18, 06:19

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/hookshot/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;Hookshot is an open-source static-recompilation project that turns Switch 2 games into native Windows/Linux programs without an emulator; its target is the Switch 2 remake of The Legend of Zelda: Ocarina of Time, released November 5, 2026. After a first release on November 7, rapid updates have shifted focus from merely booting the game to graphics, performance, and everyday usability.

**「Solution」** Hookshot converts the game&\#x27;s ARM64 code into C, compiles it into a native executable, and renders through Vulkan. The builder takes a .nup file or romfs/exefs folders, a language, and an install directory; it downloads hundreds of MB, compiles for about 40 minutes by the developer&\#x27;s estimate and the author&\#x27;s experience, then produces hookshot.exe. By v2.3.2 the project adds DLSS frame generation, AMD FSR 3.1/FSR 4, Intel XeSS, DLAA, native HDR, a CRT filter, 5K and ultrawide/multi-monitor output, multithreaded rendering, and automatic save backups \(up to 20\) with recovery. v2.1.0 had already added gyro aiming, HD rumble, 5.1 audio, DLSS/DLAA/Reflex, debug tools, and crash/lighting fixes. The author found it playable despite stutters and bugs; requirements include Windows 10/11 64-bit or compatible Linux, 16 GB RAM, Vulkan 1.3 with Mesh Shader, and about 60 GB during compilation, tested on a Ryzen 5 7600X and RTX 4060 Ti 16GB. The post is mainly a changelog and installation guide, not a reproducible benchmark or emulator comparison.

**「Takeaway」** The author presents static recompilation as having moved from a technical demo to a practical way to run a new Switch 2 game natively on PC, while long builds, frequent recompiles, and remaining bugs keep it short of a polished replacement.

**Tags**: `#静态重编译`, `#PC 原生移植`, `#Hookshot`, `#游戏性能`, `#安装指南`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Anthropic prices IPO at $83 a share, raising about $81bn](https://www.ft.com/content/62c0510b-ca65-441e-9baf-675b93903b9e?syn-25a6b1a6=1) ⭐️ 9.0/10

Anthropic priced its IPO at $83 a share—above its $70–$78 range—and is expected to raise about $81.3bn before any over-allotment shares, topping SpaceX&\#x27;s $75bn June IPO excluding SpaceX&\#x27;s own over-allotment. The shares are due to begin trading on Nasdaq.

rss · FT Markets · Nov 18, 22:04

**「Background」** The comparison baseline is SpaceX’s June 2026 IPO, which raised $75bn before an over-allotment option—an allowance for banks to sell extra shares—pushed the total higher.

**「Impact」** The listing gives Anthropic a large pool of public capital and gives public-market investors direct exposure to a major AI developer.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-06-11/elon-musk-s-spacex-set-to-make-history-with-record-breaking-ipo">SpaceX Raises $75 Billion in Record-Breaking IPO, Valued at ...</a></li>

</ul>
</details>

**Tags**: `#IPOs`, `#Anthropic`, `#AI industry`, `#public markets`, `#record listing`

---

<a id="item-finance-news-2"></a>
### [Fed minutes: officials see more rate hikes ahead, flag AI inflation risk](https://www.cnbc.com/2026/11/18/fed-minutes-october-2026.html) ⭐️ 8.0/10

Minutes of the Federal Reserve&\#x27;s October meeting released Wednesday showed almost all officials judged that further increases in the benchmark rate would likely be appropriate to bring inflation back to the 2% target, after the committee voted 10-2 to hold the federal funds rate at 3.75%-4%.

rss · CNBC Finance · Nov 18, 19:41

**「Background」** Inflation has remained above the Fed&\#x27;s 2% goal: the October consumer price index rose 0.4% for the month, 0.1 percentage point more than expected, and officials described price pressures as broad based.

**「Impact」** Fed staff warned participants that off-balance-sheet leasing commitments and circular financing arrangements among AI-related firms could amplify losses if returns on AI investment disappoint, and a few officials noted these exposures were becoming concentrated among a small number of firms.

**Tags**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#AI risk`, `#monetary policy`

---

<a id="item-finance-news-3"></a>
### [Fed Governor Waller says half-point December rate hike may be needed](https://www.cnbc.com/2026/11/18/federal-reserve-governor-christopher-waller.html) ⭐️ 7.0/10

Federal Reserve Governor Christopher Waller said the central bank may need a half-percentage-point rate increase at the Dec. 8-9 FOMC meeting to shock inflation down, arguing it should reverse the three quarter-point cuts made in 2025.

rss · CNBC Finance · Nov 18, 15:13

**「Background」** The Fed cut rates three times in 2025 before approving its first hike in more than three years in September and holding steady in October. Inflation has stayed above 3% after energy prices spiked following U.S. and Israeli strikes on Iran; futures fully price a quarter-point December increase, and other officials have favored a more gradual approach.

**Tags**: `#Federal Reserve`, `#monetary policy`, `#interest rates`, `#inflation`, `#FOMC`

---

<a id="item-finance-news-4"></a>
### [UK energy bills forecast to rise £443 a year from January](https://www.bbc.co.uk/news/articles/cmy498kdkx3xo?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

Typical UK household energy bills are forecast to rise by £443 a year, or 26%, from January, as UK inflation reaches its highest rate in a year.

rss · BBC Business · Nov 18, 13:17

**「Background」** The forecast concerns the next quarterly reset of the government&\#x27;s cap on gas and electricity prices; consultancy Cornwall Insight expects a 26% rise, one of the biggest quarterly increases on record, as consumer prices rose 3.6% in the year to October from 3.5% in September, with higher energy and fuel costs linked to the US-Israel war with Iran helping push inflation up.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/money/2026/nov/18/energy-bills-great-britain-forecast-rise">Energy bills in Great Britain forecast to rise by 26 % to... | The Guardian</a></li>
<li><a href="https://www.bbc.com/news/articles/cmy498kdkx3xo">Typical energy bill forecast to go up by £ 443 a year from January as...</a></li>

</ul>
</details>

**Tags**: `#UK energy bills`, `#inflation`, `#household finances`, `#energy prices`

---

<a id="item-finance-news-5"></a>
### [Brussels to tap profits from frozen Russian assets for new Ukraine loan](https://www.ft.com/content/08ad089e-bc58-4e0d-b458-a2c4e1dc86f2?syn-25a6b1a6=1) ⭐️ 7.0/10

Brussels plans to use profits earned on frozen Russian assets to service a new loan to Ukraine, according to a Financial Times report that gave no loan size, terms or legal details.

rss · FT Markets · Nov 18, 06:00

**「Background」** After Moscow’s full-scale invasion in 2022, the EU froze more than €210 billion in Russian central bank reserves; since 2024, financial institutions holding them have been required to ring-fence the extraordinary profits they generate, allowing Brussels to channel proceeds to Ukraine while leaving the underlying assets untouched.

**「Impact」** Financial institutions that hold or clear the immobilised Russian assets, notably Euroclear, would be directly affected because windfall profits generated from those assets would be used to service the EU&\#x27;s new Ukraine loan, tying the custody and reinvestment of sanctioned reserves to the loan&\#x27;s repayment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.politico.eu/article/russia-central-bank-assets-eu-ukraine-war-vladimir-putin/">EU to transfer €1.4B in profits from frozen Russian assets to ...</a></li>
<li><a href="https://www.europarl.europa.eu/RegData/etudes/BRIE/2025/775908/EPRS_BRI%282025%29775908_EN.pdf">Confiscation of immobilised Russian sovereign assets</a></li>
<li><a href="https://cepr.org/voxeu/columns/euroclear-and-geopolitics-immobilised-russian-assets">Euroclear and the geopolitics of immobilised Russian assets</a></li>

</ul>
</details>

**Tags**: `#EU policy`, `#Russian frozen assets`, `#Ukraine aid`, `#sanctions`, `#sovereign assets`

---

<a id="item-finance-news-6"></a>
### [Nvidia board says Huang will not return as CEO; quarterly revenue doubled](https://www.ft.com/content/8946ec08-98b3-49c1-96b1-58539281519a?syn-25a6b1a6=1) ⭐️ 7.0/10

Nvidia’s board insists Huang will not return as CEO, while the chipmaker said it doubled revenue last quarter and raised its financial forecasts for next year, the Financial Times reported.

rss · FT Markets · Nov 18, 05:00

**「Background」** Nvidia’s latest earnings were its first since Jensen Huang was ousted as CEO, and the board’s insistence that he will not return comes as Washington scrutinises China’s access to AI chips and Nvidia’s governance.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ft.com/content/3a8881b8-068c-4950-9238-4f8eb1efc870?syn-25a6b1a6=1">Nvidia insists Jensen Huang will not return as CEO as it reports...</a></li>
<li><a href="https://www.theguardian.com/technology/2026/nov/17/nvidia-third-quarter-revenue-jensen-huang">Nvidia doubles revenue as board says it does not... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#earnings`, `#revenue growth`, `#guidance`, `#CEO succession`

---

<a id="item-finance-news-7"></a>
### [Tencent Q3 2026 revenue misses estimates as AI capex surges](https://api3.cls.cn/share/article/2537922?os=android&amp;amp;sv=8.8.5&amp;amp;app=cailianpress&amp;amp;selected=) ⭐️ 7.0/10

Tencent’s Q3 2026 revenue rose 8% year on year to 207.3 billion yuan, below market expectations, while capital expenditure reached 81.433 billion yuan versus a 55.4 billion yuan estimate and free cash flow—cash after capital spending—was negative 69.1 billion yuan. The company said WorkBuddy has the highest daily token usage among domestic large-language-model products, at more than 100 trillion tokens a day.

telegram · zaihuapd · Nov 18, 09:20

**「Background」** The quarter came as Tencent’s capital spending rose 225% from a year earlier, part of an AI infrastructure buildout in which AI-related cloud demand accelerated—cloud revenue grew 35% year on year—while AI product and computing investment weighed on profit and free cash flow.

**「Who is affected」** The cost falls first on Tencent&\#x27;s shareholders, whose quarterly cash generation turned negative as capital spending of 81.4 billion yuan outran the 55.4 billion yuan estimate, while the demand side is office workers and enterprises using the WorkBuddy agent — Tencent&\#x27;s AI tool for reports, decks and spreadsheets — whose usage is what the added compute capacity is meant to serve.

<details><summary>References</summary>
<ul>
<li><a href="https://quartr.com/companies/tencent-holdings-limited_4663">Tencent (700) Investor Relations, Earnings Summary &amp; Outlook</a></li>
<li><a href="https://qz.com/tencent-near-flat-profit-ai-investments-earnings-111826">Tencent Q3 earnings show near-flat profit as AI ... - Quartz</a></li>
<li><a href="https://www.workbuddy.ai/">WorkBuddy - AI Agent for Everyday Office Work</a></li>

</ul>
</details>

**Tags**: `#Tencent`, `#earnings`, `#AI capex`, `#free cash flow`, `#China tech`

---

<a id="item-finance-news-8"></a>
### [China, South Korea Announce Substantive End to FTA Services and Investment Talks](https://x.com/Jaemyung_Lee/status/2122988472994791476) ⭐️ 7.0/10

China and South Korea announced on Nov. 18 the substantive conclusion of follow-up negotiations on services and investment under their bilateral free trade agreement, with China pledging most-favored-nation treatment for South Korean films and games and wider access in tourism, legal, construction and finance, plus expanded co-production of TV dramas, animation, variety shows and documentaries. Talks that began in March 2018 still leave some technical items to be settled at the working level, and no signing or implementation dates were given; South Korean President Lee Jae-myung said the deal would serve as a basis for a full, substantive recovery in bilateral ties.

telegram · zaihuapd · Nov 18, 10:02

**「Background」** The follow-up talks, launched in March 2018, were aimed at extending the existing China–South Korea free trade agreement to services and investment, and the declaration marks the first progress of its kind in the eight years since they began. Remaining technical items still have to be worked out at the working level before any formal signing.

**「Who is affected」** The deal would directly affect South Korean film, gaming, entertainment and tourism businesses, giving them expanded access to Chinese consumers, and Sedaily reports it also opens standalone retail stores and a construction market it values at $4 trillion, though the terms still require technical work and formal signing.

<details><summary>References</summary>
<ul>
<li><a href="https://www.chosun.com/english/national-en/2026/11/19/NTPG5ZDJMBAKLH427BSO5LHJKU/">Korea-China FTA Service, Investment Negotiations ...</a></li>
<li><a href="https://en.sedaily.com/economy/2026/11/18/korea-china-reach-services-fta-deal-opening-retail-film">Korea, China Reach Services FTA Deal Opening Retail, Film ...</a></li>
<li><a href="https://www.reuters.com/world/south-korea-says-china-trade-agreement-boost-tourism-entertainment-sectors-2026-11-18/">South Korea says China trade agreement to boost tourism ...</a></li>

</ul>
</details>

**Tags**: `#China-South Korea FTA`, `#trade policy`, `#services and investment`, `#media and gaming`, `#bilateral relations`

---