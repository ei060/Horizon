---
layout: default
title: "Horizon Summary: 2026-11-20 (EN)"
date: 2026-11-20
lang: en
---

> From 162 items, 25 important content pieces were selected

---

**Technology News**
1. [PostgreSQL 19 Ships With WAIT FOR LSN for Standby Reads](#item-tech-news-1) ⭐️ 9.0/10
2. [Anthropic debuts on Nasdaq with record $81 billion IPO](#item-tech-news-2) ⭐️ 8.0/10
3. [Nvidia CEO Jensen Huang reportedly resigns amid spy-linked affair](#item-tech-news-3) ⭐️ 8.0/10
4. [Microsoft agent-framework PyPI package hijacked to install credential stealer](#item-tech-news-4) ⭐️ 8.0/10
5. [OpenAI Says Models Cut Chip Area, Boost AMD GPU PPA Up to 14%](#item-tech-news-5) ⭐️ 8.0/10
6. [OpenJDK PR debate questions Java flaw discovery and disclosure](#item-tech-news-6) ⭐️ 7.0/10
7. [Anthropic reports Claude results on two open black-hole problems](#item-tech-news-7) ⭐️ 7.0/10
8. [UK tribunal rejects secrecy claim over Apple encryption order](#item-tech-news-8) ⭐️ 7.0/10
9. [European Commission rolls out Matrix to over 40,000 staff](#item-tech-news-9) ⭐️ 7.0/10
10. [Meta’s Muse AI agent reportedly mixed conversations and exposed private data](#item-tech-news-10) ⭐️ 7.0/10
11. [Students sue after school AI gun detector flagged a Doritos bag](#item-tech-news-11) ⭐️ 7.0/10
12. [Android developer verification expands globally in January 2027](#item-tech-news-12) ⭐️ 7.0/10
13. [IEA projects data-center carbon emissions to rise 70% by 2030](#item-tech-news-13) ⭐️ 7.0/10
14. [Judge Approves Google&\#x27;s $10 Million Purchase of Spirit Airlines Data](#item-tech-news-14) ⭐️ 7.0/10
15. [PHP schedules CRITICAL security release for all supported versions](#item-tech-news-15) ⭐️ 7.0/10
16. [Gemini can operate Mac apps in background with pause controls](#item-tech-news-16) ⭐️ 7.0/10
17. [Unverified claim: mixed-case HTTPS:// in PHP disables TLS](#item-tech-news-17) ⭐️ 7.0/10
18. [Telegram Post Claims TSMC and Samsung Paused Some China Chip Shipments](#item-tech-news-18) ⭐️ 7.0/10

**Technology Blog**
1. [The Brain&\#x27;s Hidden Role in Controlling Illness](#item-tech-blog-1) ⭐️ 4.0/10
2. [The Most Distracted Year: AI, Parallel Projects, and Focus](#item-tech-blog-2) ⭐️ 4.0/10

**Financial News**
1. [Anthropic raises $81bn in record IPO at $1.5tn valuation](#item-finance-news-1) ⭐️ 9.0/10
2. [Nscale warns $35bn IPO plans exposed to suppliers at risk of US blacklist](#item-finance-news-2) ⭐️ 7.0/10
3. [EU Delays Methane Rules for Fossil Fuel Imports](#item-finance-news-3) ⭐️ 7.0/10
4. [Anthropic IPO 后 AI 投资疑虑升温，亚洲股市普遍下跌](#item-finance-news-4) ⭐️ 7.0/10
5. [US Senate passes permitting reform bill to speed energy projects](#item-finance-news-5) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [PostgreSQL 19 Ships With WAIT FOR LSN for Standby Reads](https://simonwillison.net/2026/Nov/19/postgresql-19/) ⭐️ 9.0/10

PostgreSQL 19 has been released, about two months after its usual September cadence; the project attributed the delay mainly to a flurry of security issues it had to address, including AI-reported vulnerabilities. The release adds WAIT FOR LSN, which lets a session on a standby wait until the standby has replayed WAL up to a specified log sequence number before running a query, providing read-your-writes consistency for applications that send reads to replicas. An application can capture the primary&\#x27;s current WAL insert LSN and pass it to the standby; an optional TIMEOUT causes an error if the replica does not catch up in time.

rss · Simon Willison · Nov 19, 20:43

**「Why standby reads can be stale」** PostgreSQL standbys apply the primary&\#x27;s write-ahead log asynchronously, so a read sent to a replica can return data from before a write that already committed on the primary — a window that widens as replication lag grows. Before this release, applications that offloaded reads to standbys had to track a replication position themselves and poll until the standby caught up; the source notes MediaWiki built exactly this mechanism on MySQL, storing the primary&\#x27;s binlog position per session and waiting for the replica to reach it. \`WAIT FOR LSN\` moves that wait into the database itself, letting a standby session block until it has replayed through a given WAL position.

**「Impact」** Applications that route reads to standbys can now enforce read-your-writes consistency per request, but they must capture the primary&\#x27;s LSN and carry it to the standby—for example in a signed cookie—and decide whether to set a timeout that fails when replication lag is too high.

**Tags**: `#PostgreSQL`, `#databases`, `#replication`, `#open source`, `#WAIT FOR LSN`

---

<a id="item-tech-news-2"></a>
### [Anthropic debuts on Nasdaq with record $81 billion IPO](https://www.reuters.com/business/finance/anthropics-historic-debut-put-ais-promise-peril-wall-st-test-2026-11-19/) ⭐️ 8.0/10

Anthropic began trading on Nasdaq under the ticker ANT at an IPO price of $83 a share, selling 980 million shares for an $81.34 billion offering—the largest IPO on record, above SpaceX&\#x27;s roughly $75 billion June offering. Nvidia, Microsoft, Google, TSMC, AMD, Broadcom and Micron agreed to buy an additional $26 billion of Class N shares at the IPO price; after about $1.96 billion of existing shares were sold, Anthropic expects to receive roughly $105.4 billion. On the same day, nearly 100 AI researchers, founders and scientists published the MisAnthropic Statement, arguing that Anthropic is not a safe AI company and should not keep expanding its control over AI&\#x27;s future. Anthropic&\#x27;s filing discloses $900.9 billion in compute and infrastructure purchase and lease commitments, with $451.6 billion due by the end of 2030.

hackernews · wslh · Nov 19, 17:02 · [Discussion](https://news.ycombinator.com/item?id=50562754)

**「Background」** Anthropic, the company behind Claude, spent the year before its Nasdaq listing expanding its model lineup and revenue: the report cites Claude Fable 5 in June, Opus 5.5 in September, and Fable 5.2/Mythos 5.2 on November 9, with revenue rising from $4.6 billion in 2025 to $33.2 billion in the first nine months of 2026. Its prospectus also disclosed $900.9 billion in compute and infrastructure purchase and lease commitments, including $451.6 billion due by the end of 2030.

**「Vendor durability」** After raising $81.34B in its IPO, Anthropic&\#x27;s filing gives enterprises and competitors a public benchmark for a frontier lab&\#x27;s economics: $33.2B in revenue for the first nine months of 2026 against $900.9B in compute and infrastructure commitments, $451.6B of which is due by the end of 2030. That makes vendor durability and capacity funding, not just model quality, a concrete factor for organizations choosing among Claude, OpenAI and other AI suppliers.

**「Community discussion」** Commenters disagreed over how to read the first-day move: one noted that ANT closed up 17.07% from its $83 IPO price but down 12.85% from its $111.5 opening price, while another said the reported decline to a $1.26 trillion valuation from earlier $2 trillion hopes bodes poorly for OpenAI. Several software engineers used the thread to debate career risk, with one calling the programming &\#x27;gravy train&\#x27; basically over and another, after 50 years in the field, saying it may be the sunset of this way of making a living.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.yahoo.com/technology/live/anthropic-ipo-live-anthropic-stock-begins-trading-in-record-81b-raise-with-15t-valuation-192410598.html">Anthropic IPO live: Anthropic stock closes up 17% from initial price...</a></li>
<li><a href="https://roboforex.com/blog/anthropic-ipo/anthropic-nasdaq-debut/">Anthropic Nasdaq Debut : IPO at 83 USD Beats SpaceX</a></li>

</ul>
</details>

**Tags**: `#AI industry`, `#Anthropic`, `#IPO and public markets`, `#software engineering careers`, `#AI economics`

---

<a id="item-tech-news-3"></a>
### [Nvidia CEO Jensen Huang reportedly resigns amid spy-linked affair](https://techcrunch.com/2026/11/19/nvidia-ceo-jensen-huangs-affair-with-alleged-chinese-spy-a-timeline/) ⭐️ 8.0/10

Nvidia CEO Jensen Huang has reportedly resigned following an affair alleged to involve a Chinese spy, according to a TechCrunch report. The episode is framed as a U.S.-China national-security concern because of Nvidia&\#x27;s role in advanced AI infrastructure. The supplied account contains only a one-sentence summary, with no timeline, company confirmation, resignation timing, or independent corroboration, so the resignation and espionage allegation remain reported and unconfirmed.

rss · TechCrunch · Nov 19, 20:18

**「Background」** Earlier in November, Huang resigned as Nvidia&\#x27;s chief executive, and the company named CFO Colette Kress as interim replacement until a permanent successor is chosen. Reporting at the time said the affairs involved an executive who reported to him and a woman U.S. officials had identified as a Chinese spy; China&\#x27;s foreign ministry rejected the spying allegations as baseless.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/nvidia-ceo-jensen-huang-resigns">Jensen Huang resigns as Nvidia CEO after alleged affairs</a></li>
<li><a href="https://www.npr.org/2026/11/12/nx-s1-6037833/jensen-huang-nvidia-stepped-down">Nvidia CEO Jensen Huang resigns amid spy scandal : NPR</a></li>
<li><a href="https://www.nytimes.com/2026/11/12/technology/nvidia-jensen-huang.html">Jensen Huang Resigns From Nvidia After Affairs - The New York...</a></li>

</ul>
</details>

**Tags**: `#Nvidia`, `#Jensen Huang`, `#AI hardware`, `#national security`, `#corporate leadership`

---

<a id="item-tech-news-4"></a>
### [Microsoft agent-framework PyPI package hijacked to install credential stealer](https://www.solidot.org/story?sid=85931) ⭐️ 8.0/10

Microsoft&\#x27;s PyPI-hosted agent-framework package was reportedly hijacked in versions 1.26.1 and 1.26.2, which install credential-stealing malware. The package, downloaded nearly 200,000 times a month and used to build and deploy AI agents, steals environment variables and credential files for services including Azure, Git, Docker, and Hugging Face. The malicious code runs whenever the Python interpreter that installed the package starts, without requiring the package to be imported. A Microsoft spokesperson said the company made some package projects private during its investigation.

rss · Solidot · Nov 19, 08:24

**「Background」** PyPI is Python&\#x27;s main package index, and tools such as pip fetch releases directly from it, so whoever controls a package&\#x27;s release process can distribute code to everyone who installs it. Python environments can also run package-provided startup hooks, which explains how a package can execute code when the interpreter starts rather than only after an explicit import.

**「Rotate credentials and audit environments」** Developers who installed agent-framework 1.26.1 or 1.26.2 should treat every credential reachable from those Python environments as compromised and rotate tokens for Azure, Git, Docker, and Hugging Face, since the malicious versions harvested environment variables and credential files. Because StepSecurity traced the payload to a .pth file that executes when the interpreter starts, auditing site-packages for that loader and pinning to a version Microsoft confirms is clean should come before rebuilding any affected AI agent deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://www.comss.ru/page.php?id=22939">Вредоносные версии Microsoft Agent Framework в PyPI крадут...</a></li>
<li><a href="https://www.securitylab.ru/news/580343.php">Хакеры взломали инструмент Microsoft для ИИ. Вредонос...</a></li>

</ul>
</details>

**Tags**: `#supply-chain-security`, `#pypi`, `#ai-agents`, `#malware`, `#microsoft`

---

<a id="item-tech-news-5"></a>
### [OpenAI Says Models Cut Chip Area, Boost AMD GPU PPA Up to 14%](https://openai.com/index/advancing-chip-design-with-our-models/) ⭐️ 8.0/10

OpenAI said its models contributed to the design of its Jalapeño inference chip and AMD&\#x27;s flagship GPU IP, reporting roughly 13% smaller standard-cell area for a vector unit and about 10% for a matrix unit, plus up to 14% better power, performance, and area on AMD&\#x27;s IP versus a highly optimized baseline. It said the Jalapeño optimizations were validated during chip bring-up and that some AMD changes have entered a design sent for manufacturing. OpenAI also announced a partnership with Synopsys to train a GPT-Synopsys model. The figures are vendor claims, and OpenAI did not publish model versions, benchmark methodology, or independent verification.

telegram · zaihuapd · Nov 19, 09:30

**「Earlier Jalapeño announcement」** OpenAI had already announced Jalapeño as its first custom inference chip; an OpenAI post dated Aug. 25, 2026, reported first test results showing higher throughput and lower latency per unit of power. The current report concerns how OpenAI&\#x27;s models were used in Jalapeño&\#x27;s design, including standard-cell area reductions, rather than the chip&\#x27;s serving performance.

**「Practical implications」** For chip-design teams, the claim is that OpenAI models can be inserted into existing design-optimization work, but the missing model details and third-party validation mean the workflow cannot yet be assessed or reproduced from the announcement alone. The GPT-Synopsys partnership&\#x27;s availability and terms were not disclosed.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/jalapeno-first-results/">Jalapeño’s first results show industry-leading ... - OpenAI</a></li>

</ul>
</details>

**Tags**: `#AI for chip design`, `#OpenAI`, `#AMD`, `#EDA`, `#semiconductors`

---

<a id="item-tech-news-6"></a>
### [OpenJDK PR debate questions Java flaw discovery and disclosure](https://github.com/openjdk/jdk/pull/32781) ⭐️ 7.0/10

A pull request in the OpenJDK repository has become the focus of a Hacker News discussion about how a reported Java security issue was discovered and disclosed. Commenters point to an Adoptium support issue in which the PR author says Oracle asked them not to proceed with the pull request until approval, and later says Oracle had taken it over; others question whether an AI-assisted discovery duplicated an earlier report. The available material does not establish the flaw&\#x27;s technical details, severity, affected versions, or whether the “java4shell” label and September 2026 timing are accurate.

hackernews · notmine1337 · Nov 19, 11:47 · [Discussion](https://news.ycombinator.com/item?id=50558906)

**「Background」** Java 4 Shell refers to CVE-2026-114938, a memory-corruption vulnerability in OpenJDK’s Base64 decoder that Calif says it discovered and reported and that can lead to remote code execution. It affects OpenJDK 17.0.6 and later as well as distributions built from the affected code, including Oracle Java SE, Amazon Corretto, Eclipse Temurin, Microsoft Build of OpenJDK, Azul Zulu, and Red Hat OpenJDK. The name echoes Log4Shell, the 2021 Java logging flaw.

**「Patch exposure」** Organizations running affected OpenJDK-based services should prioritize patched builds: CVE-2026-114938 is an out-of-bounds write in the optimized Base64 decoder on certain Intel and AMD processors that can permit unauthenticated remote code execution or memory disclosure. Administrators should verify that their Java distribution has shipped a fix, since applications using the runtime remain exposed until that decoder is updated.

**「Community discussion」** Commenters disagree about whether the AI-assisted finding was independent: one asks whether the model may have read an earlier bug report, while another says their own offline harness independently found and exploited the issue and argues that simultaneous disclosures are now common. A separate comment notes that Oracle&\#x27;s commit message duplicates the pull request wording word for word.

<details><summary>References</summary>
<ul>
<li><a href="https://www.digitec.ch/en/page/java4shell-critical-java-vulnerability-primarily-endangers-banks-and-large-companies-44450">Java 4 Shell : Critical Java vulnerability allows attacks without... - Digitec</a></li>
<li><a href="https://calif.io/java4shell/">Java 4 Shell : Write once, RCE everywhere</a></li>
<li><a href="https://www.bleepingcomputer.com/news/security/critical-java4shell-flaw-allows-rce-attacks-on-major-java-applications/">Critical Java 4 Shell flaw allows RCE attacks on major Java applications</a></li>
<li><a href="https://www.salesforce.com/blog/java4shell-critical-openjdk-vulnerability-cve-2026-114938/">Java4Shell – Critical OpenJDK Vulnerability (CVE-2026-114938)</a></li>

</ul>
</details>

**Tags**: `#OpenJDK`, `#Java security`, `#vulnerability disclosure`, `#AI-assisted security research`, `#Oracle`

---

<a id="item-tech-news-7"></a>
### [Anthropic reports Claude results on two open black-hole problems](https://www.anthropic.com/research/claude-black-hole-physics) ⭐️ 7.0/10

Anthropic’s research announcement reports that Claude solved two open problems in theoretical black-hole physics. The available evidence is a vendor announcement; the supplied analysis says the results do not describe our universe directly or have practical applications, and that the headline overstates “solves.” No independent validation or substantive discussion of the papers was included in the supplied material.

hackernews · cybermango · Nov 19, 17:30 · [Discussion](https://news.ycombinator.com/item?id=50563148)

**「Why black-hole thermodynamics matters here」** Black-hole thermodynamics is a long-standing testing ground for reconciling quantum mechanics with general relativity, since black holes carry entropy and temperature while being described by classical geometry. Anthropic&\#x27;s announcement identifies one of the two problems as the Hawking-Page phase transition, the question of when a hot gas turns into a black hole.

**「Impact」** For researchers assessing AI-for-science claims, the practical takeaway is verification rather than deployment: the reported results have no direct application to our universe, and the claim has not been independently validated in the supplied material.

**「Community discussion」** Commenters spent little time on the papers themselves; one criticized “Claude solves” as anthropomorphizing and noted that the word “prompt” does not appear in the blog post or either paper. Another described the second result as establishing an upper limit on black-hole mass for a given central charge—a commenter’s interpretation, not independent confirmation.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/claude-black-hole-physics">Claude Fable 5.2 solves two open problems in the physics of black ...</a></li>

</ul>
</details>

**Tags**: `#AI-for-science`, `#LLM reasoning`, `#black hole physics`, `#theoretical physics`, `#Anthropic Claude`

---

<a id="item-tech-news-8"></a>
### [UK tribunal rejects secrecy claim over Apple encryption order](https://macanorak.com/uk-government-forced-to-admit-it-issued-apple-a-secret-encryption-order/) ⭐️ 7.0/10

A U.K. tribunal rejected the government&\#x27;s claim that disclosing a secret encryption order issued to Apple would damage national security, forcing London to acknowledge the order&\#x27;s existence. The order&\#x27;s contents remain secret, so the scope of what Apple was compelled to do is not public. The ruling addresses disclosure of the demand, not the merits of the encryption order itself.

hackernews · Terretta · Nov 19, 16:21 · [Discussion](https://news.ycombinator.com/item?id=50562113)

**「Background」** Secret technical demands allow governments to compel communications providers to assist surveillance without public disclosure. This tribunal ruling tests whether the government can keep even the existence of such an order confidential on national-security grounds.

**「Impact」** Because the order&\#x27;s contents remain secret, Apple users and independent researchers cannot determine which encrypted services are covered, so Apple&\#x27;s public security assurances cannot be fully verified against the demand.

**「Community Discussion」** Commenters scrutinized Apple&\#x27;s shift from saying &quot;not even Apple&quot; can access user data to saying Apple cannot, with one arguing that device-held keys may still wrap other keys and weaken the assurance. Another commenter cited the tribunal judgment as the primary source and said the media learned of the order through confidential security briefings rather than a leak, while its contents remain secret.

**Tags**: `#encryption`, `#privacy`, `#Apple`, `#UK government`, `#surveillance`

---

<a id="item-tech-news-9"></a>
### [European Commission rolls out Matrix to over 40,000 staff](https://element.io/blog/how-the-european-commission-rolled-out-matrix-to-more-than-40-000-staff/) ⭐️ 7.0/10

The European Commission has deployed a self-operated, Matrix-based collaboration tool to every staff laptop, serving more than 40,000 users as of September 2026, according to Element&\#x27;s blog. The Commission completed a proof of concept in December 2025 and concluded that the Matrix protocol and Element client met its needs; the production rollout followed in September. During the rollout, live presence was disabled because the load from the online/away indicator affected performance. Element, which develops the Element client, published the account, so the deployment details are vendor-reported.

hackernews · liotier · Nov 19, 10:58 · [Discussion](https://news.ycombinator.com/item?id=50558533)

**「Background」** Matrix is a messaging protocol, and Element is a client built on it. The European Commission&\#x27;s production deployment follows a December 2025 proof of concept that tested whether Matrix and Element met its requirements; the resulting service is operated by the Commission itself.

**「Deployment impact」** For other public-sector IT teams, the European Commission deployment is a reference model rather than a turnkey endorsement: the Commission operates the service itself for more than 40,000 users and disabled live presence after load affected performance. Organizations copying that model should plan for self-hosted operations and a presence/performance trade-off at scale, and should separately validate end-to-end encryption and session verification, since the discussion disputes Matrix E2EE maturity and notes that the MLS effort is paused while other encryption work continues.

**「Community discussion」** One commenter called Matrix&\#x27;s encryption a “tire fire” and said the MLS migration appears abandoned, while another reported daily problems with session verification, encryption errors, and a fractured client landscape. A self-hosting user, by contrast, praised the setup for making live-location sharing more private than WhatsApp or Telegram.

<details><summary>References</summary>
<ul>
<li><a href="https://element.io/blog/how-the-european-commission-rolled-out-matrix-to-more-than-40-000-staff/">How the European Commission rolled out Matrix to more than 40 ...</a></li>
<li>There&#x27;s a lot of parallel work going on to improve encryption in Matrix, includi... | Hacker News</li>

</ul>
</details>

**Tags**: `#Matrix`, `#open-source collaboration`, `#public sector IT`, `#end-to-end encryption`, `#enterprise deployment`

---

<a id="item-tech-news-10"></a>
### [Meta’s Muse AI agent reportedly mixed conversations and exposed private data](https://techcrunch.com/2026/11/19/metas-ai-agent-muse-is-mixing-up-conversations-and-exposing-private-data-report-says/) ⭐️ 7.0/10

A TechCrunch report says Meta’s AI agent Muse mixed up conversations, with employees saying it surfaced messages and personal details they never requested or that did not belong to them. The examples included childcare requests they never made, career advice they never sought, product orders they never placed, and bank account balances that were not theirs. The report does not describe the cause or scope, and it is not clear whether Meta has confirmed the incidents; the claimed cross-conversation exposure has not been independently verified.

rss · TechCrunch · Nov 19, 17:38

**「Background」** Meta has described Muse as a personal AI agent that acts on users’ behalf across email, calendar, and messaging; a report on its bug bounty program says Meta has paid roughly $1.2 million across 64 valid reports out of more than 630 submissions. Meta also warns new users that the agent can make mistakes, and its terms of service hold users responsible for what Muse does, according to a separate report.

**「Impact」** For anyone using Muse for personal or financial tasks, the reported behavior means one session may not be isolated from another person’s data, so details such as orders and bank balances could appear in the wrong conversation. That is a confidentiality risk for affected users and a trust problem for Meta’s agent, even before the cause or scale is established.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ithinkdiff.com/meta-muse-ai-agent-other-peoples-data-signal/">Meta Staff Say Muse AI Agent Sent Other People&#x27;s Data</a></li>
<li><a href="https://tifon.dev/materia/0de79688-c772-404e-9672-515f51ed2b9d">Meta &#x27;s Muse AI Agent Bug Bounty Pays $1.2M, Including $300K for...</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#privacy`, `#security`, `#Meta`, `#consumer AI`

---

<a id="item-tech-news-11"></a>
### [Students sue after school AI gun detector flagged a Doritos bag](https://arstechnica.com/tech-policy/2026/11/traumatized-teens-sue-school-cops-after-doritos-bag-triggers-ai-gun-alert/) ⭐️ 7.0/10

Four Black high school students in Baltimore County, Maryland, are suing their school district and local police over an October 2025 incident in which the district&\#x27;s AI gun-detection system flagged a student holding a bag of Cool Ranch Doritos as a possible gunman, Ars Technica reports. School officials reviewed the linked camera footage within two minutes, recognized the snack bag, and canceled the alert — a cancellation that also notified the Baltimore County Police Department that no response was needed. Police responded anyway, and the students&\#x27; suit concerns what the article describes as a traumatizing on-campus clash with officers. The available excerpt does not detail the specific legal claims, the named defendants&\#x27; positions, or any response from the district or police.

rss · Ars Technica · Nov 19, 20:19

**「Background」** AI gun-detection systems are marketed to schools as a layer on top of existing security cameras: computer-vision models scan the video feed for shapes resembling a firearm and push an alert to staff and, in many deployments, to local police. Because the models only flag a possible match, districts typically rely on a human review step, in which officials pull up the linked camera footage and decide whether a real threat exists before officers are dispatched.

**「Impact」** The case turns on a concrete operational gap: even after humans reviewed the footage and stood down the alert, officers were still dispatched, so districts and police departments using these systems face a specific question about whether a cancellation reliably reaches responding units before they arrive. For students at schools running AI camera-detection systems, that gap determines whether a false positive ends at a reviewer&\#x27;s screen or at a police encounter.

**Tags**: `#AI gun detection`, `#false positives`, `#school surveillance`, `#AI accountability`, `#civil rights`

---

<a id="item-tech-news-12"></a>
### [Android developer verification expands globally in January 2027](https://arstechnica.com/gadgets/2026/11/google-will-launch-android-app-verification-requirement-globally-in-january-2027/) ⭐️ 7.0/10

Google will begin rolling out Android developer verification worldwide in January 2027, requiring apps installed from third-party sources to come from developers registered with Google. The global rollout follows a September launch in Brazil, Indonesia, Singapore, and Thailand that blocked installation of unregistered apps, and Google says the requirement will reach all devices within &quot;several months.&quot; Registration requires government identification and a $25 fee, which Google frames as a malware and scam deterrent despite objections from developers and users.

rss · Ars Technica · Nov 19, 18:00

**「Background」** Apps distributed through Google Play already come from verified developers; the new policy extends that check to apps installed from third-party sources. Once verification is active in a region, Android will not install sideloaded apps unless their developers have completed Google&\#x27;s registration process.

**「Impact」** Developers who distribute Android apps outside the Play Store must provide government identification and pay the $25 fee to keep their apps installable in affected regions, while users will be unable to sideload apps from unregistered developers. Because Google says the global rollout will reach all devices over several months, availability will vary by region and device during that period.

**Tags**: `#Android`, `#app verification`, `#sideloading`, `#Google`, `#mobile security`

---

<a id="item-tech-news-13"></a>
### [IEA projects data-center carbon emissions to rise 70% by 2030](https://www.solidot.org/story?sid=85937) ⭐️ 7.0/10

The IEA projects that data-center carbon emissions will be 70% higher in 2030 than at current levels, driven by AI demand that is expected to double data-center electricity use. Over the next four years, AI data centers would consume an additional 350 TWh of electricity annually, more than the UK&\#x27;s total annual electricity consumption, according to the report. By the end of the decade, about half of the power for China&\#x27;s AI data centers is expected to come from coal, with the rest from renewables, a small nuclear share, and very little gas, while about 60% of US data-center power is expected to come from natural gas; as of August, about 180 GW of new US gas generation was planned to supply data centers, nearly the EU&\#x27;s current installed gas capacity.

rss · Solidot · Nov 19, 16:34

**「Earlier IEA work」** The IEA’s April 2025 special report, Energy and AI, had already examined how AI could drive a surge in data-centre electricity demand and what that meant for emissions and energy security. The latest warning extends that work with a 2030 emissions projection and country-level fuel-mix estimates for China and the US.

<details><summary>References</summary>
<ul>
<li><a href="https://www.iea.org/news/ai-is-set-to-drive-surging-electricity-demand-from-data-centres-while-offering-the-potential-to-transform-how-the-energy-sector-works">AI is set to drive surging electricity demand from data ...</a></li>
<li><a href="https://www.iea.org/reports/energy-and-ai/">Energy and AI: Data Centres and Electricity Demand - IEA - IEA</a></li>

</ul>
</details>

**Tags**: `#data centers`, `#AI infrastructure`, `#energy consumption`, `#carbon emissions`, `#IEA`

---

<a id="item-tech-news-14"></a>
### [Judge Approves Google&\#x27;s $10 Million Purchase of Spirit Airlines Data](https://www.solidot.org/story?sid=85928) ⭐️ 7.0/10

A U.S. bankruptcy judge, Sean Lane, approved Google&\#x27;s $10 million purchase of internal data from Spirit Airlines, the low-cost carrier that ceased operations in May 2026. The auctioned data includes employee emails, spreadsheets and calendar information as well as marketing, productivity and operations data; Google has said it plans to use the data for product development and AI training. After unions and members of Congress raised concerns, Google agreed last week to additional privacy protections, though the report did not detail those measures.

rss · Solidot · Nov 19, 06:46

**「Background」** Spirit Airlines halted operations in May, and its internal records became part of the bankruptcy estate&\#x27;s asset liquidation. Google placed the winning $10 million bid at an August auction; flight attendants then sued to block the sale, and Judge Sean Lane moved the approval hearing to September 9, 2026.

**「What the Approval Means for Spirit Employees」** The people most directly affected are former Spirit employees whose email, spreadsheets and calendar entries sit inside the purchased dataset: the sale was approved even after 119 members of Congress signed a letter urging the companies to protect worker privacy, and the only reported concession is a set of additional privacy protections Google accepted before the ruling, which Reuters attributes to confirmation by the employees&\#x27; union rather than to a published agreement. Because the source account does not describe what those protections actually require, employee representatives and privacy regulators would need the specific terms to determine whether personal data is excluded, anonymized, or retained under restriction.

<details><summary>References</summary>
<ul>
<li><a href="https://saify.me/blog/google-spirit-airlines-bankruptcy-data-ai-training">Google &#x27;s $ 10 M Spirit Airlines data bid puts employee privacy on trial</a></li>
<li><a href="https://www.reuters.com/business/aerospace-defense/google-agrees-addition-privacy-protections-spirit-airlines-data-sale-2026-11-10/">Google agrees to additional privacy protections in Spirit ...</a></li>
<li><a href="https://horsford.house.gov/media/press-releases/spirit-airlines-to-sell-employee-data-to-train-google-ai-horsford-and-warren-lead-call-for-worker-privacy-protections">Spirit Airlines to Sell Employee Data to Train Google AI ...</a></li>

</ul>
</details>

**Tags**: `#AI training data`, `#privacy`, `#Google`, `#data acquisition`, `#bankruptcy`

---

<a id="item-tech-news-15"></a>
### [PHP schedules CRITICAL security release for all supported versions](https://www.php.net/archive/2026.php) ⭐️ 7.0/10

PHP plans to publish a security release on November 19, 2026, from 14:00 to 14:30 UTC, fixing a vulnerability rated CRITICAL, PHP&\#x27;s highest severity level, that affects all supported PHP versions. The release follows PHP&\#x27;s regular four-week cadence, and the security team says the CRITICAL issue can be triggered only under non-default configurations or uncommon environments. Technical details and the fixed version numbers will be published with the release; specific affected versions are not yet listed.

telegram · zaihuapd · Nov 19, 07:10

**「PHP&\#x27;s release cadence and severity ratings」** PHP&\#x27;s security team issues security releases on a regular four-week cycle, so this update is a scheduled slot in that cadence rather than an out-of-band emergency patch. Within that process, advisories and fixed version numbers are held until the release goes live, which is why the affected version list and CVE identifiers are not yet public. The team&\#x27;s caveat that a CRITICAL rating applies only under non-default configurations or uncommon environments reflects how it grades exploitability rather than how widely a flaw is deployed.

**「Upgrade planning and exposure triage」** Administrators on any supported PHP branch should plan to move to the fixed builds once their distribution or hosting stack ships them; coverage indexed after the release lists 8.5.13, 8.4.28, 8.3.37 and 8.2.36 as the patched versions. Because the CRITICAL rating applies to issues triggered only under non-default or uncommon configurations, triage should prioritise deployments that deviate from stock setups rather than assume every default install is exposed. Panel-managed PHP is a separate dependency: Plesk&\#x27;s advisory maps the fix to PHP 8.2.36 for client websites, so hosting users may need to wait for the panel vendor rather than upstream PHP alone.

<details><summary>References</summary>
<ul>
<li>Critical PHP Security Release on 19 Nov 2026 - Plesk Support</li>
<li>PHP critical security release, 19 November (CVE-2026-129289, CVE-2026-115560)</li>

</ul>
</details>

**Tags**: `#PHP`, `#security`, `#vulnerability`, `#open source`, `#release`

---

<a id="item-tech-news-16"></a>
### [Gemini can operate Mac apps in background with pause controls](https://www.bloomberg.com/news/articles/2026-11-19/google-s-gemini-can-now-control-mac-devices-on-users-behalf) ⭐️ 7.0/10

Google&\#x27;s Gemini can now perform desktop tasks on Mac, including clicking, typing, browsing menus and filling forms, for eligible U.S. users. The feature is available to Google AI Plus, Pro and Ultra subscribers using the Mac Gemini app, according to a brief Bloomberg report. Gemini runs in a separate background window so users can keep using the main screen and cursor, and users can limit which apps it accesses, watch actions live, pause at any time and approve key steps. No independent testing details were provided.

telegram · zaihuapd · Nov 20, 02:51

**「Prior context: computer-use competition」** Computer-use features, in which an assistant clicks, scrolls, and types inside apps instead of only replying in a chat window, were already offered by other popular AI assistants before this Mac rollout. Bloomberg&\#x27;s report frames Google&\#x27;s addition as matching that existing competition and as increasing pressure on Apple to make Siri more capable.

**「Impact」** Eligible subscribers can hand off multi-step Mac tasks without giving up the main screen, but they must decide which apps to expose to Gemini and which actions require approval.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-19/google-s-gemini-can-now-control-mac-devices-on-users-behalf">Gemini Brings Computer - Use Capability to Mac ... - Bloomberg</a></li>

</ul>
</details>

**Tags**: `#AI agents`, `#Google Gemini`, `#macOS`, `#desktop automation`, `#human oversight`

---

<a id="item-tech-news-17"></a>
### [Unverified claim: mixed-case HTTPS:// in PHP disables TLS](https://x.com/ljachowicz/status/2123477025268924514) ⭐️ 7.0/10

A widely reposted social-media claim alleges that PHP&\#x27;s HTTP and FTP stream wrappers match URL schemes case-insensitively but enable TLS only when the scheme&\#x27;s fifth character is a lowercase &quot;s&quot;, so URLs such as HTTPS://, httpS:// and FTPS:// are allegedly sent as plaintext HTTP/FTP — potentially exposing tokens, Basic auth credentials, cookies, POST bodies and FTP logins, including after third-party redirects. The post attributes the issue to CVE-2026-128064 \(GHSA-f6gg-rchx-xw8j\) with a CVSS 4.0 score of 8.2 and says it was fixed in PHP 8.2.36, 8.3.37, 8.4.28, 8.5.13 and 8.6.0, while 8.1 and earlier are EOL and will not receive a patch, leaving lowercasing the scheme as the suggested mitigation. The claim is unconfirmed: it comes from a Telegram repost rather than a primary advisory, and the cited CVE identifier and release versions could not be verified from the supplied material.

telegram · zaihuapd · Nov 20, 03:04

**「How PHP stream wrappers decide on TLS」** PHP&\#x27;s HTTP and FTP stream wrappers handle URLs passed to functions such as fopen\(\) and file\_get\_contents\(\), and the URL scheme determines whether the connection should be wrapped in TLS. The GitHub security advisory GHSA-f6gg-rchx-xw8j states that the wrappers recognised schemes case-insensitively but enabled TLS only when a lowercase &quot;s&quot; appeared at a fixed position; the fix compares the complete scheme case-insensitively for both the HTTP and FTP wrappers.

**「Who needs to act」** Sites still on PHP 8.1 or earlier cannot receive a patch, so operators there must normalize URL schemes to lowercase before passing them to stream wrappers — and also watch code paths that follow third-party redirects, since a redirect to a mixed-case URL triggers the same plaintext fallback. For supported branches, upgrading to 8.2.36, 8.3.37, 8.4.28, 8.5.13 or 8.6.0 removes the exposure; a third-party CVE tracker records the flaw at CVSS 8.2 and notes no public exploit code is listed as of publication.

<details><summary>References</summary>
<ul>
<li><a href="https://app.opencve.io/cve/CVE-2026-128064">CVE-2026-128064 - Vulnerability Details - OpenCVE</a></li>
<li><a href="https://github.com/php/php-src/security/advisories/GHSA-f6gg-rchx-xw8j">Mixed-case HTTPS and FTPS URLs can expose data in plaintext</a></li>
<li><a href="https://everycve.com/CVE-2026-128064">CVE - 2026 - 128064 : Mixed-case HTTPS and FTPS URLs can expose...</a></li>

</ul>
</details>

**Tags**: `#PHP`, `#security vulnerability`, `#TLS`, `#CVE`, `#web security`

---

<a id="item-tech-news-18"></a>
### [Telegram Post Claims TSMC and Samsung Paused Some China Chip Shipments](https://telegram.me/pelosi3/30345) ⭐️ 7.0/10

A Telegram post claims TSMC and Samsung have paused some chip shipments to Chinese customers while awaiting U.S. licenses under new Commerce Department rules. The post says the rules remove the non-AI-use exemption and require licenses before shipment, potentially affecting AI companies such as ByteDance as well as smartphone makers Xiaomi, OPPO, and vivo. No official document, effective date, affected product list, or independent confirmation was provided, so the scope and status of the reported pause remain unverified.

telegram · pelosi3 · Nov 19, 14:06

**「Background」** The U.S. began restricting exports of advanced AI chips to China in 2022 and expanded the controls in 2023. Those measures cut off Chinese access to Nvidia’s A100, H100 and H200 data-center chips and led Nvidia to design lower-performing parts for the Chinese market.

**「Licensing bottleneck hits consumer chip orders」** Because the reported pause reportedly covers consumer chips built on advanced nodes rather than only AI accelerators, Xiaomi, OPPO and vivo — which source mobile processors from TSMC — must wait for U.S. licenses before new orders ship, making production schedules dependent on approval speed. TrendForce reports that 16nm orders are among those affected, which gives Chinese handset makers a concrete reason to draw down existing inventory or qualify alternative foundry capacity while approvals are pending.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/nvidia-prepares-h200-shipments-to-china-as-chip-war-lines-blur">Nvidia prepares shipment of 82,000 AI GPUs to China as chip war...</a></li>
<li><a href="https://www.trendforce.com/news/2026/11/20/news-tsmc-samsung-reportedly-pause-china-consumer-chip-shipments-under-new-u-s-rules-16nm-orders-affected/">[News] TSMC, Samsung Reportedly Pause China Consumer Chip ...</a></li>
<li><a href="https://www.technetbooks.com/2026/11/tsmc-and-samsung-pause-advanced-chip.html">TSMC and Samsung Pause Advanced Chip Shipments to China Under ...</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#export controls`, `#TSMC`, `#Samsung`, `#China tech`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [The Brain&\#x27;s Hidden Role in Controlling Illness](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196869) ⭐️ 4.0/10

rss · Dapenti Xilei · Nov 20, 00:17

**「Background」** The familiar view of sickness separates a broadly indiscriminate immune response from a brain that merely registers pain and fatigue. The author argues that recent neuroscience instead casts the brain as an active manager that detects pathogens, anticipates threats, and stores illness experience.

**「Solution」** Drawing on work presented at the Society for Neuroscience meeting, the article describes several mechanisms. Circumventricular organs, porous outposts at the blood-brain barrier, are said to decode bacterial versus viral signals and shape symptom-specific neural activity, so sickness is not one fixed program. In a virtual-reality experiment, visually approaching figures with skin lesions reportedly activated threat-related brain regions and, after 15 minutes, raised frontline sentinel immune cells to levels comparable with flu vaccination; healthy or merely fearful figures did not. In mice, reactivating hippocampal illness engrams with optogenetics reproduced metabolic slowing and liver inflammatory gene activity without a pathogen, while re-exposure to the illness-associated context before a toxin reduced weight loss and metabolic disruption. The author extends this to chronic inflammation, suggesting that repeatedly triggered illness memories might act like an immune PTSD, though this remains a hypothesis and the conference report gives little methodological detail.

**「Takeaway」** The article&\#x27;s larger claim is that sickness is a brain-directed survival strategy spanning perception, prediction, and memory, not an isolated immune event. If that framing holds, targeting pathological illness memories could open new ways to treat chronic inflammatory and psychosomatic conditions, but the evidence remains early.

**Tags**: `#神经免疫学`, `#室周器官`, `#记忆印迹`, `#光遗传学`, `#科普证据质量`

---

<a id="item-tech-blog-2"></a>
### [The Most Distracted Year: AI, Parallel Projects, and Focus](http://www.ruanyifeng.com/blog/2026/11/weekly-issue-420.html) ⭐️ 4.0/10

rss · Ruanyifeng Blog · Nov 20, 00:07

**「Background」** AI coding tools have made it cheap to start work on many things at once, and this weekly issue&\#x27;s lead essay asks whether that abundance is actually good for developers. It centers on a year-end reflection by Alejandro AO, a developer advocate at Hugging Face, who calls 2026 his most distracted year and whose account the newsletter author says resonated with him.

**「Solution」** AO&\#x27;s description is concrete: most of the time he had four to ten agents pushing forward three or four different projects, burning millions of tokens a day, and even so some projects sat idle. His argument, endorsed by the newsletter author, is that AI creates an illusion of near-free progress — a little prompting and a result appears — so every passing idea gets implemented, pulling attention away from the high-priority work that matters. The small projects that look like they will take an hour tend to balloon and consume far more time than expected, so the visible output is broad but shallow, since no single project receives enough sustained effort to become good. The proposed correction is arithmetic rather than technical: AI makes things easier but does not add hours to the day, so running more work in parallel necessarily reduces the time each item gets. The author&\#x27;s prescription is to prioritize ruthlessly, cut low-priority scope, and spend the largest share of time and energy on the most important project — doing subtraction with AI rather than addition. AO&\#x27;s stated wish for 2027 is to be less distracted and focus on one or two core projects; this is opinion and personal anecdote in an otherwise link-heavy digest, with no measurements offered.

**「Takeaway」** The author concludes that as AI makes every task feel easier to advance, the scarce resource becomes attention rather than capability, and the goal is not to do many things but to finish the most important one — using AI to go deeper on fewer projects instead of wider.

**Tags**: `#AI-assisted development`, `#developer productivity`, `#AI agents`, `#technology newsletter`, `#project prioritization`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Anthropic raises $81bn in record IPO at $1.5tn valuation](https://www.ft.com/content/62c0510b-ca65-441e-9baf-675b93903b9e?syn-25a6b1a6=1) ⭐️ 9.0/10

Anthropic, the AI company behind Claude, raised $81bn in a record initial public offering at a $1.5tn valuation, with its shares due to begin trading on Thursday.

rss · FT Markets · Nov 19, 07:04

**「Background」** Anthropic, the maker of the Claude chatbot, was founded in 2021 by siblings Dario and Daniela Amodei along with other former OpenAI researchers.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Dario_Amodei">Dario Amodei - Wikipedia</a></li>
<li><a href="https://capfinch.com/company-anthropic.html">Anthropic Company Profile: Valuation, Funding Rounds ...</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#IPO`, `#AI`, `#technology financing`, `#valuation`

---

<a id="item-finance-news-2"></a>
### [Nscale warns $35bn IPO plans exposed to suppliers at risk of US blacklist](https://www.ft.com/content/97912585-2412-496c-a224-78e69328bcdb?syn-25a6b1a6=1) ⭐️ 7.0/10

Nvidia-backed AI start-up Nscale warned that its $35bn IPO plans are exposed to suppliers that could be added to Washington&\#x27;s entity list, which restricts US exports to listed companies. No blacklisting has been confirmed and the company did not quantify a financial impact.

rss · FT Markets · Nov 19, 14:39

**「Background」** Nscale disclosed the potential exposure in an amended US IPO filing dated November 12, 2026, identifying an OEM supplier with reported ownership links to entities on the BIS Entity List. That US list bars companies deemed national-security risks from receiving American technology; the supplier itself is not designated, and Nscale said it found no existing customers that would be covered.

**「Impact」** If the suppliers are blacklisted, Nscale says the resulting export controls could force contract changes, delay or cancel projects, and reduce business, putting its data-centre buildout and planned listing at execution risk.

<details><summary>References</summary>
<ul>
<li><a href="https://letsdatascience.com/news/nscale-warns-of-exposure-to-suppliers-facing-us-blacklist-1671b3fe">Nscale Warns of Exposure to Suppliers Facing US Blacklist</a></li>
<li><a href="https://finance.yahoo.com/technology/ai/articles/nscale-investigates-ties-blacklisted-tech-180940823.html?fr=sycsrp_catchall">Nscale investigates ties to blacklisted tech companies</a></li>
<li>Nscale flags supplier blacklist risk ahead of planned IPO - Traders Union</li>

</ul>
</details>

**Tags**: `#Nscale`, `#IPO`, `#US entity list`, `#export controls`, `#Nvidia`

---

<a id="item-finance-news-3"></a>
### [EU Delays Methane Rules for Fossil Fuel Imports](https://www.ft.com/content/e871493f-920c-4ece-94d4-9d14317047fe?syn-25a6b1a6=1) ⭐️ 7.0/10

The EU has delayed implementation of its methane emissions rules for fossil fuel imports by at least two years, the Financial Times reported. The delay followed sustained lobbying by the US, Qatar and the oil and gas sector, according to the report.

rss · FT Markets · Nov 19, 09:26

**「Background」** The delay applies to monitoring and reporting obligations for oil, gas and coal importers under the EU Methane Regulation; EU member states and the European Parliament agreed the two-year postponement after Parliament had initially backed a three-year delay.

**「Who is affected」** U.S. and Qatari gas exporters and fossil-fuel importers covered by the rules gain at least two more years before compliance, after exporters argued the measures threatened energy security.

<details><summary>References</summary>
<ul>
<li><a href="https://www.europarl.europa.eu/news/en/press-room/20261021IPR48321/methane-rules-parliament-backs-longer-delay-for-energy-importers-and-producers">Methane rules: Parliament backs longer delay for energy ...</a></li>
<li><a href="https://www.reuters.com/business/energy/eu-countries-parliament-agree-delay-eu-methane-regulation-by-two-years-2026-11-19/">EU countries, Parliament agree to delay EU methane regulation ...</a></li>
<li><a href="https://www.straitstimes.com/world/europe/trump-administration-qatar-say-eu-methane-rules-threaten-energy-security">Trump administration, Qatar say EU methane rules ... | The Straits Times</a></li>

</ul>
</details>

**Tags**: `#EU policy`, `#methane emissions`, `#fossil fuels`, `#energy imports`, `#lobbying`

---

<a id="item-finance-news-4"></a>
### [Anthropic IPO 后 AI 投资疑虑升温，亚洲股市普遍下跌](https://www.bloomberg.com/news/articles/2026-11-19/stock-market-today-dow-s-p-live-updates) ⭐️ 7.0/10

Anthropic 上市后股价在盘后交易中下跌逾 5%、跌破每股 92 美元，随后亚洲股市普遍走低，MSCI 亚太指数下跌 1.7%，为连续第七个交易日下跌。韩国 Kospi 指数下跌 3.66%，SK 海力士下跌 6%、三星电子下跌 4.7%，东京电子下跌 7.19%、瑞萨电子下跌 6.71%。

telegram · zaihuapd · Nov 20, 01:58

**「Background」** Anthropic&\#x27;s initial public offering \(IPO\) on Nasdaq on Nov. 19, 2026, gave investors a new AI stock to trade while they were already weighing whether huge AI spending would produce matching returns.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/19/anthropic-ipo-ai-stocks-selloff.html">Anthropic IPO fails to lift AI stocks - CNBC</a></li>

</ul>
</details>

**Tags**: `#AI investment`, `#Asian equities`, `#market selloff`, `#semiconductors`, `#SoftBank/OpenAI`

---

<a id="item-finance-news-5"></a>
### [US Senate passes permitting reform bill to speed energy projects](https://telegram.me/pelosi3/30354) ⭐️ 7.0/10

The U.S. Senate passed a comprehensive permitting-reform bill 62-33 on Thursday that aims to accelerate federal approvals for large energy and infrastructure projects, including gas pipelines, transmission lines, wind and solar farms, and rail expansions, according to The New York Times. The bill, which would revise or narrow several landmark environmental laws, still must pass the Republican-controlled House, where its prospects are uncertain.

telegram · pelosi3 · Nov 20, 03:17

**「Background」** The Senate had voted earlier this month to open debate on the legislation, the Bipartisan American Affordability and Jobs Act, before Thursday’s final passage vote.

<details><summary>References</summary>
<ul>
<li><a href="https://www.theguardian.com/us-news/2026/nov/09/senate-energy-infrastructure-bill-vote">Senate advances bill to speed up projects from gas... | The Guardian</a></li>

</ul>
</details>

**Tags**: `#US Senate`, `#permitting reform`, `#energy infrastructure`, `#environmental law`, `#legislative outlook`

---