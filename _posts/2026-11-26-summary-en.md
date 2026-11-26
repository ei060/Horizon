---
layout: default
title: "Horizon Summary: 2026-11-26 (EN)"
date: 2026-11-26
lang: en
---

> From 168 items, 21 important content pieces were selected

---

**Technology News**
1. [1Password confirms customer account data theft after GitHub compromise](#item-tech-news-1) ⭐️ 8.0/10
2. [Shorter, more readable Lean version of Anthropic-linked GRH verification posted](#item-tech-news-2) ⭐️ 8.0/10
3. [FCC conditionally authorizes SpaceX&\#x27;s 1 million Starmind orbital data centers](#item-tech-news-3) ⭐️ 8.0/10
4. [Ubuntu security patch delays prompt some users to move to Debian](#item-tech-news-4) ⭐️ 7.0/10
5. [State AGs challenge Character.AI bankruptcy sale over private chat data](#item-tech-news-5) ⭐️ 7.0/10
6. [Ladybird releases first downloadable alpha for macOS and Linux](#item-tech-news-6) ⭐️ 7.0/10
7. [Ars Live recap: Military attacks on data centers are a lasting cloud risk](#item-tech-news-7) ⭐️ 7.0/10
8. [French intelligence links mass fridge attack to Iran IRGC&\#x27;s Shahid Kaveh](#item-tech-news-8) ⭐️ 7.0/10
9. [Claude and ChatGPT Reported to Challenge AlphaFold in Protein Work](#item-tech-news-9) ⭐️ 7.0/10
10. [XPeng tech day: IRON robot speaks untethered, driverless robotaxi operations planned](#item-tech-news-10) ⭐️ 7.0/10
11. [Tencent open-sources Hy4 flash GGUF weights, smallest runs on 64 GB Mac mini](#item-tech-news-11) ⭐️ 7.0/10
12. [Minecraft Java RCE via server resource-pack fonts affects 1.20.5–1.21.10](#item-tech-news-12) ⭐️ 7.0/10
13. [Samsung, SK Hynix reportedly to adopt YMTC Xtacking NAND tech](#item-tech-news-13) ⭐️ 7.0/10

**Technology Blog**
1. [A 2-Meter Asteroid Briefly Became Earth’s Mini-Moon](#item-tech-blog-1) ⭐️ 5.0/10
2. [Five Open-Source Chinese Input Methods: A Stability Check](#item-tech-blog-2) ⭐️ 5.0/10
3. [Ladybird Alpha: A Browser Built on an Independent Engine](#item-tech-blog-3) ⭐️ 4.0/10

**Financial News**
1. [Report: US Commerce Department Pressured Intel for 10% Stake](#item-finance-news-1) ⭐️ 9.0/10
2. [US Proposes New Tariffs on 14 Trading Partners, Including China and EU](#item-finance-news-2) ⭐️ 8.0/10
3. [UK energy bills to rise 26% from January as gas costs surge](#item-finance-news-3) ⭐️ 7.0/10
4. [Shein to pay $100mn to settle US customer-deception allegations](#item-finance-news-4) ⭐️ 7.0/10
5. [Bank of Korea raises rates to 3.25%, expects inflation above target](#item-finance-news-5) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [1Password confirms customer account data theft after GitHub compromise](https://1password.com/blog/update-on-nov-2026-security-incident) ⭐️ 8.0/10

1Password confirmed that intruders accessed internal systems and downloaded some customer account information—names, email addresses, account identifiers, and account creation and last-login times—while customer vaults and their contents were unaffected. The company said it began investigating on Nov. 19 after detecting compromise of an employee’s corporate GitHub account, which the attacker used to reach source code and push malicious code to backend services; it did not disclose how many customers were affected. 1Password said it disabled the involved account, rotated or revoked potentially exposed internal credentials, and strengthened verification codes for invitation and recovery emails; it said users do not need to change their accounts but should watch for phishing.

hackernews · lxhrstn · Nov 25, 17:18 · [Discussion](https://news.ycombinator.com/item?id=50644817)

**「Background」** 1Password&\#x27;s cloud service runs on backend systems that engineers build and deploy from source code kept in GitHub repositories, so control of an employee&\#x27;s GitHub account can be a route into production code rather than just into a personal workspace. That pattern — compromise a single employee account or laptop, then push altered code that backend services deploy — is the commonly cited mechanism behind SaaS supply-chain breaches. According to the disclosure, 1Password began investigating signs of a compromised employee enterprise GitHub account on November 19, before confirming the intrusion on November 25.

**「Phishing risk for affected customers」** Customers whose names, email addresses, account identifiers, and login timestamps were stolen should treat unsolicited 1Password-branded messages as suspect, because that metadata can make phishing more convincing. 1Password says vault contents were not affected and users do not need to change their accounts, so the practical step is to verify any warning through the official app or website rather than through links in an email.

**「Community discussion」** Several commenters argued that this fits a standard SaaS supply-chain risk in which a compromised employee laptop can lead to malicious code being pushed and deployed, and one asked whether branch protections on pushes to main were missing or bypassed. A longtime user who keeps a local-only vault said the production-code push is exactly the scenario they worry about, while another commenter reported receiving a detailed phishing email—not from an official 1Password domain—that appeared to draw on the exposed data.

<details><summary>References</summary>
<ul>
<li><a href="https://1password.com/blog/update-on-nov-2026-security-incident">Update on a security incident involving 1Password’s backend ...</a></li>
<li><a href="https://thehackernews.com/2026/11/1password-hacked-customer-data-and.html">1Password Hacked, Customer Data and Source Code Stolen in ...</a></li>

</ul>
</details>

**Tags**: `#security incident`, `#1Password`, `#supply chain security`, `#phishing`, `#SaaS security`

---

<a id="item-tech-news-2"></a>
### [Shorter, more readable Lean version of Anthropic-linked GRH verification posted](https://github.com/lsernau/grh-lean) ⭐️ 8.0/10

A GitHub repository \(lsernau/grh-lean\) now hosts a substantially shorter, restructured Lean version of GRH-related formal verification work associated with Anthropic. Commenters describe the new version as far more readable: spootydooty highlights a clear split between &quot;known math&quot; and &quot;new math&quot; plus human-readable documentation throughout, and bananaflag cites a reduction from roughly 17 million lines to about 76,000 lines. Those figures come from commenters rather than the item itself, and the reported sizes are not consistent — spootydooty refers to a &quot;300kloc proof&quot; — so the exact scale of the new formalization is unconfirmed. The change is a readability and restructuring effort, not a new mathematical result.

hackernews · nb-t · Nov 25, 21:48 · [Discussion](https://news.ycombinator.com/item?id=50648050)

**「Background」** On 20 November 2026, Levent Alpöge announced a proof—found with Anthropic&\#x27;s Claude—of the Riemann Hypothesis and the Generalized Riemann Hypothesis for Dirichlet L-functions, released as a Lean formal proof spanning 175,187 files and about 17 million lines. The Lean FRO and Mathlib Initiative verified that original proof on 21 November 2026, and Anthropic researcher Luke Sernau published a more efficient 300,000-line version on 25 November 2026. The grh-lean repository offers a still shorter Lean 4 proof built on Mathlib and using only the axioms propext, Classical.choice and Quot.sound.

**「Why it matters」** For formal-verification readers, the practical gain is auditability: the documented separation of established mathematics from new material gives reviewers a way to see which parts of the argument rest on unproven assumptions, which is hard to do in a multi-million-line proof. The discussion also notes that no conventional mathematical paper presenting the argument has appeared, so Lean code remains the primary artifact.

**「Discussion」** gre asks whether a compact, well-explained proof undercuts Tao&\#x27;s recent argument that enormous proofs lacking insight are a problem, and whether smarter models can now &quot;golf&quot; proofs while explaining them; that question was posed, not settled, in the thread. AIShill101 argues that Lean code, however readable, is not a substitute for a mathematical paper written by someone who understands the core argument and can present it at a conference.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Alp%C3%B6ge&#x27;s_proof_of_the_Riemann_hypothesis">Alpöge&#x27;s proof of the Riemann hypothesis - Wikipedia</a></li>
<li><a href="https://www.math.uwaterloo.ca/~mrubinst/alpoge_claude_grh/">Alpöge/Claude proof of the Generalized Riemann Hypothesis</a></li>
<li><a href="https://github.com/lsernau/grh-lean">GitHub - lsernau/grh-lean: A short Lean 4 proof of the ...</a></li>

</ul>
</details>

**Tags**: `#Lean`, `#formal verification`, `#AI-assisted mathematics`, `#Generalized Riemann Hypothesis`

---

<a id="item-tech-news-3"></a>
### [FCC conditionally authorizes SpaceX&\#x27;s 1 million Starmind orbital data centers](https://arstechnica.com/space/2026/11/the-fcc-has-authorized-spacex-to-deploy-1-million-satellites/) ⭐️ 8.0/10

The FCC on Wednesday granted SpaceX conditional authorization to deploy up to 1 million Starmind satellites intended to operate as orbital data centers. If fully deployed, the constellation would increase the number of satellites in orbit roughly 50-fold; the decision authorizes the constellation rather than reporting its completed deployment. The FCC dismissed some opponent concerns, including potential threats to scientific research, after determining they fell outside its regulatory authority.

rss · Ars Technica · Nov 25, 18:22

**「Background」** SpaceX&\#x27;s proposed Starmind constellation is designed to process data in orbit for use on Earth, with the company arguing that near-constant solar power could deliver cost and energy efficiency while reducing environmental impact on Earth. The proposal drew opposition from Amazon, Viasat and the American Astronomical Society, CNBC reported.

**「Conditions and Unresolved Concerns」** The approval is conditional rather than an immediate deployment: SpaceX must deploy the first Starmind satellite by Nov. 25, 2033, so the one-million-satellite constellation remains a long-lead buildout. The FCC also dismissed opponents&\#x27; concerns about threats to scientific research after determining they fall outside its regulatory authority, so this proceeding does not resolve those concerns.

<details><summary>References</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/25/spacex-fcc-satellite-approval.html">SpaceX wins FCC approval for 1 million orbital data center satellites</a></li>
<li><a href="https://cointelegraph.com/news/fcc-authorizes-spacex-1m-satellites-orbital-ai-data-centers">SpaceX Wins FCC Approval for Orbital AI Computing Network</a></li>
<li><a href="https://nypost.com/2026/11/25/business/fcc-approves-elon-musks-spacex-to-launch-1-million-satellites-for-data-centers-in-space/">FCC approves Elon Musk&#x27;s SpaceX to launch 1 million satellites for...</a></li>
<li><a href="https://spaceflightnow.com/2026/11/26/fcc-green-lights-spacexs-plan-to-launch-1-million-starmind-data-center-satellites/">FCC green lights SpaceX’s plan to launch 1 million ‘Starmind ...</a></li>

</ul>
</details>

**Tags**: `#FCC`, `#SpaceX`, `#orbital data centers`, `#satellite constellations`, `#computing infrastructure`

---

<a id="item-tech-news-4"></a>
### [Ubuntu security patch delays prompt some users to move to Debian](https://www.openwall.com/lists/oss-security/2026/11/25/9) ⭐️ 7.0/10

A Hacker News thread, opened from an oss-security mailing list post titled &quot;Slow Ubuntu security response times,&quot; focused on complaints that Ubuntu is slow to ship security fixes in 2026. The linked post&\#x27;s technical details were not available in the supplied material, so the specific vulnerabilities, packages, or measured delays under discussion cannot be verified here. Commenters described acting on the perceived latency: one said their employer moved all server images from Ubuntu to Debian over it, another said they chose Debian for a &quot;generic Linux VM&quot; for the first time after hesitating over slow patches, and a third said security fixes appear in Ubuntu&\#x27;s -updates pocket hours before reaching the security repository. Other commenters pushed back, noting that major distributions spend substantial time on regression testing and that Debian&\#x27;s lighter QA resourcing has produced regressions of its own.

hackernews · gslin · Nov 25, 20:38 · [Discussion](https://news.ycombinator.com/item?id=50647181)

**「Background」** Ubuntu is derived from Debian but maintains its own security update process and supported releases, so its patch timing is separate from Debian&\#x27;s. The thread began with Hanno Böck&\#x27;s Nov. 25, 2026 oss-security post stating that Ubuntu&\#x27;s response to severe security flaws had become concerning.

**「Practical consequences」** The thread documents concrete operational changes rather than a general trend: one commenter said their organization standardized server images on Debian because of Ubuntu&\#x27;s security response, and another said they stopped running unattended upgrades from the security repository alone and now install all updates, accepting the risk of breaking a system. For teams still on Ubuntu, that second report points to a compatibility tradeoff — pulling only security-pocket updates may lag, while pulling everything from -updates widens exposure to less-tested changes.

**「Debate in the comments」** The main disagreement is whether patch latency reflects negligence or deliberate regression testing: one commenter called slow response &quot;absolutely unacceptable&quot; for a widely used distribution in 2026, while another argued that most major distributions invest heavily in QA and linked a Debian bug as an example of regressions that lighter testing can let through. A third commenter questioned why the delay persists, saying Ubuntu had long been their default for a generic Linux VM and that they did not understand what justified it.

<details><summary>References</summary>
<ul>
<li><a href="https://www.openwall.com/lists/oss-security/2026/11/25/9">oss-security - Slow Ubuntu security response times - openwall.com</a></li>
<li><a href="https://seclists.org/oss-sec/2026/q4/890">oss-sec: Slow Ubuntu security response times</a></li>

</ul>
</details>

**Tags**: `#Ubuntu`, `#Linux security`, `#vulnerability response`, `#open source`, `#distribution maintenance`

---

<a id="item-tech-news-5"></a>
### [State AGs challenge Character.AI bankruptcy sale over private chat data](https://techcrunch.com/2026/11/25/state-ags-fight-character-ais-plan-to-auction-off-users-private-chats/) ⭐️ 7.0/10

State attorneys general are challenging a proposed Character.AI bankruptcy sale that would include sensitive personal data from more than 21 million U.S. accounts, 2.1 million of which are registered to minors, according to the AGs. The dispute concerns whether users&\#x27; private chat data can be transferred as a saleable asset in the bankruptcy process. The available reporting does not identify which states have intervened, the prospective buyer, or a timetable for court review, and no ruling on the transfer has been reported.

rss · TechCrunch · Nov 25, 17:35

**「Background」** Character.AI’s proposed sale is a bankruptcy asset transfer, which requires court approval and can include customer records among the assets unless a judge or regulator blocks or conditions the transfer. According to ppc.land, 39 states and the District of Columbia have asked for nine conditions on any buyer, including a privacy ombudsman for the data.

**「Impact」** If the transfer goes forward as proposed, private conversations tied to 21 million U.S. accounts — including 2.1 million minor-registered accounts — would pass to a new owner under terms set by the bankruptcy proceeding, and the AGs&\#x27; intervention could delay that handover or attach conditions to it. The reporting provided describes no opt-out mechanism for affected users.

<details><summary>References</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/25/state-ags-fight-character-ais-plan-to-auction-off-users-private-chats/">Character . AI ’s plan to auction off users’ private chats ... | TechCrunch</a></li>
<li><a href="https://ppc.land/what-the-therapist-bot-heard-character-ais-chats-are-on-the-block/">What the therapist bot heard: Character . ai &#x27;s chats are on the block</a></li>

</ul>
</details>

**Tags**: `#AI privacy`, `#data governance`, `#Character.AI`, `#bankruptcy sale`, `#consumer protection`

---

<a id="item-tech-news-6"></a>
### [Ladybird releases first downloadable alpha for macOS and Linux](https://arstechnica.com/gadgets/2026/11/ladybirds-new-alpha-shows-theres-life-beyond-chromium/) ⭐️ 7.0/10

Ladybird released its first downloadable alpha on November 23, after four years of building a browser engine from scratch, with prebuilt packages for macOS and Linux. Previously, users had to compile the browser from source; the alpha is now an installable package with automatic updating. The project says both its rendering engine and LibJS JavaScript engine are its own rather than a fork, and that the browser around the engine is &\#x27;modest, but functional.&\#x27; Ars Technica&\#x27;s item does not provide compatibility, performance, or security details, so the release should be treated as an early alpha.

rss · Ars Technica · Nov 25, 17:33

**「Why Ladybird is different」** Ladybird has been under development for about four years as an engine built without reusing an existing browser codebase. Most mainstream browsers rely on Google&\#x27;s Blink or Mozilla&\#x27;s Gecko, while Ladybird&\#x27;s renderer and its LibJS JavaScript engine are original implementations. Before the alpha, users who wanted to try it had to build the browser from source.

**「Impact」** The prebuilt package lowers the barrier for macOS and Linux users to test an independent browser engine, since they no longer need to compile it themselves, and automatic updating makes repeated testing easier. The source gives no compatibility, performance, or security details, so those evaluating it should treat it as alpha software.

**Tags**: `#browser engines`, `#open source`, `#Ladybird`, `#software releases`, `#web platforms`

---

<a id="item-tech-news-7"></a>
### [Ars Live recap: Military attacks on data centers are a lasting cloud risk](https://arstechnica.com/gadgets/2026/11/ars-live-recap-dont-expect-military-attacks-on-data-centers-to-stop/) ⭐️ 7.0/10

An Ars Live discussion with Joseph Jarnecki of the Royal United Services Institute examined why data centers have become military targets, citing the first military attack on Amazon data centers in the Middle East this year and drone strikes exchanged by Russia and Ukraine. Jarnecki said public and private cloud facilities are dual-use because militaries run battlefield management, HR, and resource management on them; once a military uses civilian infrastructure, targeting principles can make it a military object. He also noted that relatively cheap kamikaze drones can impose disproportionate economic costs and cause widespread cloud disruptions when they hit data centers.

rss · Ars Technica · Nov 25, 16:47

**「Background」** Public cloud data centers increasingly run military workloads alongside civilian ones—battlefield management systems, HR, and resource planning—and under international targeting principles that dual use can make a civilian facility a military objective. The discussion follows 2026 attacks in which Iran struck Amazon data centers in the Middle East, causing what Ars reported as permanent loss of customer data, while Russia and Ukraine exchanged drone strikes on each other&\#x27;s data centers.

**「Impact」** For cloud customers, especially those running military or government workloads, the discussion identifies a physical-resilience and dependency problem: hosting such work can make a civilian facility a military object of interest to an adversary, so continuity planning cannot assume that civilian status protects a provider&\#x27;s sites.

<details><summary>References</summary>
<ul>
<li><a href="https://www.rusi.org/explore-our-research/publications/commentary/iranian-data-strikes-shake-global-digital-infrastructure">Iranian Data Strikes Shake Global Digital Infrastructure | Royal United ...</a></li>
<li><a href="https://arstechnica.com/gadgets/2026/11/ars-live-can-the-cloud-survive-drone-strikes-on-data-centers/">Ars Live: What drone attacks on data centers mean for... - Ars Technica</a></li>

</ul>
</details>

**Tags**: `#data center security`, `#cloud infrastructure`, `#drone attacks`, `#critical infrastructure`, `#military conflict`

---

<a id="item-tech-news-8"></a>
### [French intelligence links mass fridge attack to Iran IRGC&\#x27;s Shahid Kaveh](https://arstechnica.com/security/2026/11/a-familiar-iranian-hacking-group-has-found-a-new-way-to-cause-chaos/) ⭐️ 7.0/10

Hackers remotely raised temperatures in refrigeration systems at hundreds of supermarkets across France one night in October, destroying millions of euros of food. French intelligence agencies traced the intrusion to Shahid Kaveh, an Islamic Revolutionary Guard Corps Cyber Electronic Command unit already known to Western agencies, citing Farsi-language traces and other digital clues, according to the report. The report describes the operation as unprecedented in scale for commercial refrigeration attacks and as the first such incident in the heart of Europe, while providing few technical details about how the systems were compromised.

rss · Ars Technica · Nov 25, 14:29

**「Background」** Shahid Kaveh is one of several offensive units under the IRGC&\#x27;s Cyber Electronic Command, named after an Iranian commander who died in the 1980s Iran-Iraq war. Before the French refrigeration incident, the unit was linked to a wave of attacks on US industrial control devices in 2024, and on November 9 France formally attributed last month&\#x27;s operation against roughly 700 supermarkets to it.

**「Impact」** For operators of networked commercial refrigeration, the case makes remote-access controls, network segmentation, and temperature monitoring a direct operational and financial concern rather than a back-office IT issue.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ft.com/content/5f3a85ad-e621-4189-bada-989f41702ed9?syn-25a6b1a6=1">The secretive Iranian cyber unit behind Europe’s freezer hacks</a></li>
<li><a href="https://www.fdd.org/analysis/france-is-latest-victim-of-iranian-cyber-sabotage-first-unleashed-on-israel/">France Is Latest Victim of Iranian Cyber Sabotage First Unleashed on...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#critical infrastructure`, `#IoT security`, `#state-sponsored hacking`, `#Iran`

---

<a id="item-tech-news-9"></a>
### [Claude and ChatGPT Reported to Challenge AlphaFold in Protein Work](https://www.solidot.org/story?sid=85992) ⭐️ 7.0/10

Phylo researcher Xinming Tu reported that, in an overnight test early this month, the latest Claude model beat other large language models—and a specialized tool trained on protein sequences—at predicting little-known bacterial protein sequences, a finding he shared with Harvard Medical School&\#x27;s Leo Chen that stirred debate in computational biology. Separately, OpenAI said Tuesday that its latest model designed new proteins, some of which behaved as expected when synthesized and tested in the lab. Some scientists suggested general models such as Claude and ChatGPT could surpass specialized tools like AlphaFold for protein structure prediction and design, while skeptics argued the apparent abilities may be rote reproduction of training data; the report provides no primary sources or methodological details, so the claims remain preliminary.

rss · Solidot · Nov 25, 15:26

**「Background」** AlphaFold is Google DeepMind’s specialized protein-structure prediction system: its public database, developed with EMBL-EBI, contains more than 200 million structure predictions, while AlphaFold Server, powered by AlphaFold 3, predicts how proteins interact with molecules such as DNA and RNA. That dedicated protein-modeling baseline is the reference point against which the reported performance of general-purpose LLMs is being debated.

**「Validation burden」** For biotech teams, the practical consequence is that general-purpose model outputs remain design candidates requiring wet-lab synthesis and binding assays: OpenAI&\#x27;s reported GPT-6.2 protein-design run produced 35 binders from 322 minibinders tested. Teams should budget experimental validation rather than treating an LLM-generated protein as a validated result.

<details><summary>References</summary>
<ul>
<li><a href="https://alphafold.ebi.ac.uk/">AlphaFold Protein Structure Database</a></li>
<li><a href="https://alphafoldserver.com/welcome">AlphaFold Server</a></li>
<li><a href="https://www.techrepublic.com/article/news-gpt-6-2-protein-design-lab-binding-results/">GPT-6.2 Protein Design: What the Lab Binding Data Show</a></li>

</ul>
</details>

**Tags**: `#AI for science`, `#protein structure prediction`, `#protein design`, `#large language models`, `#AlphaFold`

---

<a id="item-tech-news-10"></a>
### [XPeng tech day: IRON robot speaks untethered, driverless robotaxi operations planned](https://www.ifanr.com/1695212?utm_source=rss&amp;utm_medium=rss&amp;utm_campaign) ⭐️ 7.0/10

At its 2026 technology day, XPeng said its IRON humanoid robot walked on stage and delivered an untethered Chinese-English speech with no remote control, and laid out a 2027 rollout: hardware mass production in January, store assistant trials in the first quarter, and a public launch in the second quarter. XPeng said driverless passenger trials for its Robotaxi are already underway, with driverless demonstration operations in some areas planned for the end of 2026, and a purpose-built model, YOYO-01, slated for 2027; it also plans to begin charging a subscription for its Turing AI driver assist on new vehicles globally from the second quarter of 2027, while buyers before then keep lifetime rights. The company said its second-generation VLA system has been tested in Germany, the Netherlands and France since July, that public urban assisted-driving test rides opened at its Paris store in November, and that it targets first global deliveries in the first half of 2027. It further announced an over-the-air update raising 5C charging to 6C \(10% to 80% in 10.7 minutes\) and a &quot;VLA adaptive deceleration&quot; feature arriving in December 2026 on the G9L and MONA L05.

rss · iFanr · Nov 26, 02:25

**「Background」** XPeng has used its technology day to present IRON, its humanoid robot. At the previous edition, IRON&\#x27;s highly humanlike gait triggered suspicions that a person was hidden inside, and XPeng cut open the robot&\#x27;s skin on stage to rebut them.

**「Owner billing and rollout timeline」** XPeng owners face a concrete software-cost and compatibility split: from Q2 2027, Turing AI assisted driving will move to subscription for new vehicle buyers, while customers who order before the service opens keep lifetime ADAS rights; XPeng did not disclose pricing. Dual Orin-X models will receive a distilled second-generation VLA build starting in December 2026, with remaining dual Orin-X vehicles covered by Q1 2027, so those owners are on a different software path from Turing-chip cars.

**Tags**: `#autonomous driving`, `#humanoid robots`, `#robotaxi`, `#VLA`, `#XPeng`

---

<a id="item-tech-news-11"></a>
### [Tencent open-sources Hy4 flash GGUF weights, smallest runs on 64 GB Mac mini](https://mp.weixin.qq.com/s/o0xxShVQX6g2UllrrEv1WQ) ⭐️ 7.0/10

Tencent Hunyuan has released GGUF quantized weights for its 224B-parameter Hy4 flash model through its AngelSlim compression and acceleration toolkit. The original weights are about 410.27 GiB; the smallest IQ2-AH build is 125.73 GiB, roughly 30% of the original, and Tencent says it can run on a 64 GB Mac mini using the Strata offload framework. Tencent-reported figures put generation at 89 tokens/s with 10K context on a 48 GB VRAM device and 47 tokens/s with 32K context for the Q3\_K version on a 128 GB M5 Max. The company also reports that Q3\_K scores within 0.4 points of the original model on evaluations including DeepSWE v1.1; these performance and quality figures have not been independently verified.

telegram · zaihuapd · Nov 25, 09:29

**「Background」** GGUF is the container format used by llama.cpp-family local runners, and the IQ2-AH build Tencent published is its smallest quantization, at 125.73 GiB against a 410.27 GiB original. That smallest build is still roughly twice the 64 GB of unified memory in a Mac mini, so running it depends on streaming weights from storage instead of holding them in RAM. Project materials for the Strata engine describe exactly that approach: a C++20/CUDA inference engine for models that fit in neither VRAM nor RAM, splitting one checkpoint across GPU VRAM, host RAM, and read-only NVMe.

**「Fit vs. fidelity trade-off」** The variant that actually fits a 64 GB machine is the IQ2-AH build, and Tencent&\#x27;s quality comparison only covers Q3\_K \(within 0.4 points of the original on DeepSWE v1.1\), so users picking the smallest quant to stay inside 64 GB are trading away accuracy that the release does not quantify. Teams needing the 47 tokens/sec at 32K context should note that figure was measured on a 128 GB M5 Max with Q3\_K, while the 89 tokens/sec result came from a 48 GB VRAM GPU at 10K context — offloaded Mac mini throughput is not stated. Independent quantizers are also publishing competing low-bit builds: one Hugging Face publisher reports lower KL divergence than the AngelSlim IQ2\_AH weights across the public Hy4 GGUF variants it measured, a self-reported claim worth checking against evaluation files before committing a deployment.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ro99/strata">GitHub - ro99/strata: C/C++ MoE inference engine for models ...</a></li>
<li><a href="https://huggingface.co/nace-ai/Hy4-flash-GGUF">nace-ai/Hy4-flash-GGUF · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#open-source AI`, `#model quantization`, `#local inference`, `#Tencent Hunyuan`, `#GGUF`

---

<a id="item-tech-news-12"></a>
### [Minecraft Java RCE via server resource-pack fonts affects 1.20.5–1.21.10](https://github.com/bikini/minecraft2shell) ⭐️ 7.0/10

A public disclosure named minecraft2shell on Nov. 22 showed a high-severity remote code execution flaw in Minecraft Java Edition: a crafted TrueType font in a server resource pack can trigger a native out-of-bounds write in FreeType 2.14.3 and earlier and execute arbitrary code on a Windows Java client. Java Edition 1.20.5 through 1.21.10 and snapshots 26.1 through 26.4 are affected; 1.20.4 and earlier and Bedrock Edition are not. Mojang has not issued an official patch, and the game still uses lwjgl-freetype 3.4.3. The community m2sfix 1.0.0, published Nov. 24, disables hinting through a Java agent or mod; until a fix, users should avoid adding resource packs, set multiplayer server resource-pack permissions to disabled, or install the temporary fix.

telegram · zaihuapd · Nov 25, 12:46

**「Background」** Minecraft Java Edition renders fonts through LWJGL&\#x27;s FreeType bindings, and server-supplied resource packs can include TrueType font files that the client processes. The reported flaw is in FreeType&\#x27;s native font-hinting path, so crafted font data can trigger an out-of-bounds write in native code.

**「Disable resource packs or install the fix」** Because the demonstrated attack is client-side and arrives through a server resource pack, players on affected Java versions can be exposed by joining a malicious server with resource packs enabled; the public proof targets the Windows Java 26.3 client. With no Mojang patch, the supplied guidance is to set multiplayer server resource-pack permissions to &quot;Disabled&quot; or install the community m2sfix 1.0.0 agent/mod, which disables hinting.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/bikini/minecraft2shell">GitHub - bikini/ minecraft 2 shell : Minecraft to native RCE · GitHub</a></li>

</ul>
</details>

**Tags**: `#Minecraft`, `#RCE`, `#security vulnerability`, `#FreeType`, `#open source`

---

<a id="item-tech-news-13"></a>
### [Samsung, SK Hynix reportedly to adopt YMTC Xtacking NAND tech](https://tech.ifeng.com/c/8yLRPKxQy4L) ⭐️ 7.0/10

Samsung Electronics and SK Hynix have reportedly agreed, through cross-license agreements, to use parts of Yangtze Memory Technologies&\#x27; Xtacking technology in 3D NAND flash. Xtacking fabricates the memory cells and CMOS control circuits on separate wafers and joins them by bonding, so each part can be produced and optimized independently. All three companies declined to comment, and the report did not disclose licensing terms, the specific Xtacking elements covered, or a timeline.

telegram · zaihuapd · Nov 25, 14:33

**「Background」** Xtacking separates a 3D NAND&\#x27;s memory array from its CMOS control logic, fabricating each on a separate wafer and then bonding the two — an approach YMTC first demonstrated in 2018. As Samsung and SK hynix push NAND toward hundreds of layers, they are running into the limits of conventional single-wafer fabrication, which makes a production-tested wafer-bonding process a lower-risk option to adopt.

**「Impact」** If the licenses take effect, the Korean manufacturers could separate NAND array and logic production, with the logic portion potentially made at a foundry on a more advanced process, according to an Omdia senior analyst cited in the report; the lack of company confirmation means the scope and timing remain unsettled.

<details><summary>References</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/samsung-and-sk-hynix-tap-ymtcs-xtacking-tech-in-cross-license">Samsung and SK Hynix cross-license YMTC&#x27;s Xtacking 3D NAND</a></li>
<li><a href="https://www.techpowerup.com/355199/samsung-and-sk-hynix-to-license-ymtcs-xtacking-technology">Samsung and SK hynix to License YMTC&#x27;s Xtacking ...</a></li>

</ul>
</details>

**Tags**: `#3D NAND`, `#Xtacking`, `#semiconductor manufacturing`, `#Samsung/SK Hynix`, `#cross-licensing`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [A 2-Meter Asteroid Briefly Became Earth’s Mini-Moon](http://www.dapenti.com/blog/more.asp?name=xilei&amp;id=196974) ⭐️ 5.0/10

rss · Dapenti Xilei · Nov 25, 23:52

**「Background」** Earth has one long-lived natural satellite, but the article explains that small near-Earth asteroids can be temporarily captured as “mini-moons,” using 2026 QQ8 as its example.

**「Solution」** According to the article, the roughly 2-meter-wide 2026 QQ8 was captured in April and will depart in early December; it is harmless, and Matthew Payne of the Minor Planet Center says an impact would at most produce a bright meteor and a small bang. Krisztián Sárneczky first spotted it in August at Hungary’s Konkoly Observatory as Sar2901, but its faint signal left astronomers unsure whether it was natural rock or space debris. Weeks of tracking—including solar-radiation-pressure effects and data from the Lowell Discovery Telescope and the University of Hawaii’s 2.2-meter Mauna Kea telescope—led the Minor Planet Center to confirm it as natural in late October and name it 2026 QQ8. Payne says such temporary companions are common, perhaps one at any time, though small size, distance, and fast apparent motion make them hard to find; earlier examples include 2006 RH120 \(~1 year\) and 2020 CD3 \(~3 years\). The article attributes most near-Earth objects to the main asteroid belt and describes capture as a gentle process in which an object approaching at a suitable speed and angle is perturbed by Earth’s and the Moon’s gravity; Payne calls the exact origin an active question. The piece relies on expert quotes rather than raw astrometry or methods.

**「Takeaway」** The article’s larger point is that 2026 QQ8 is a safe, short-lived example of a common gravitational process, and that the Rubin Observatory’s LSST—expected to raise the known catalog from about 1.5 million to 5 million objects—should expose many more hidden mini-moons.

**Tags**: `#迷你月亮`, `#近地小行星`, `#轨道捕获`, `#天文观测`, `#薇拉·鲁宾天文台`

---

<a id="item-tech-blog-2"></a>
### [Five Open-Source Chinese Input Methods: A Stability Check](https://www.appinn.com/open-source-ime-boom-and-stability/) ⭐️ 5.0/10

rss · Appinn · Nov 25, 09:40

**「Background」** Note: this summary may have been produced by third-party AI from an Appinn article and may deviate from the original; it does not represent Appinn’s views. Please &lt;a href=&quot;https://www.appinn.com/open-source-ime-boom-and-stability/&quot; target=&quot;\_blank&quot;&gt;read the original&lt;/a&gt; for verification. A wave of new open-source Chinese input methods prompted a hands-on comparison of five Windows options, all judged against Rime Weasel’s 万象base scheme with Xiaohe double pinyin.

**「Solution」** The author’s main finding is that the field is expanding faster than product quality: even the best alternatives feel like demos, with Weasel still the only mature choice at 9/10 despite its complex configuration. Qingjian \(7.5\) and Qingfeng \(8\) are feature-rich—Qingfeng the most so—but settings are numerous, poorly organized, and sometimes contradictory; both also import Rime dictionaries only partially, mishandling polyphonic entries such as those in the yuanshen dictionary. Double-pinyin support is especially uneven: Qingjian’s radical and stroke lookup and its “ask a character” feature fail or require full pinyin, while Qingfeng’s auxiliary-code trigger settings do not persist. Shuishan \(7\) adds broad model-correction options, but the author saw crashes, dropped input, and lost focus on a low-spec PC, while FreeType \(4.5, or 6.5 excluding its marketing\) lacks lookup features and has poor candidate ordering, though its settings search and organization are the best of the group.

**「Takeaway」** The comparison suggests that open-source IMEs need to prioritize stability and coherent, restrained configuration over feature count before they can be recommended for production use.

**Tags**: `#开源输入法`, `#Rime`, `#双拼`, `#稳定性评测`, `#Windows 输入法`

---

<a id="item-tech-blog-3"></a>
### [Ladybird Alpha: A Browser Built on an Independent Engine](https://www.appinn.com/ladybird-browser/) ⭐️ 4.0/10

rss · Appinn · Nov 25, 06:26

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图存在偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/ladybird-browser/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;Ladybird began in SerenityOS, became an independent project in 2022, and on November 23, 2026 released an Alpha for macOS and Linux after four years of development, aiming to build a browser rather than another skin over Chromium, WebKit, or Gecko.

**「Solution」** Ladybird has its own rendering engine, JavaScript engine, and WebAssembly implementation, uses no code from other browser engines, and in 2024 founder Andreas Kling and GitHub co-founder Chris Wanstrath formed a nonprofit to support it. Its stated goals are a fully independent engine, free and open-source code, privacy, no default-search revenue, and no monetization of user data; the project also said in February that it is gradually migrating from C++ to Rust with AI assistance. The Alpha adds bookmarks, history, private browsing, ad filtering, profiles, session restore, PDF viewing, video playback, and content blocking, with rolling updates and a roadmap of Beta in 2027 and a general release in 2028. The developers warn of failing sites, occasional crashes, and no security guarantee, and the author found common sites usable but hit many &quot;SSL verification failed&quot; errors on less common ones; the browser lacks AI features, extensions, and userscripts, borrows Firefox for DevTools via a local port, and in the author&\#x27;s brief, screenshot-based comparison used somewhat more memory than Edge. macOS requires Apple Silicon and macOS 14.4+, Linux supports x86-64 and ARM64 via Flatpak, Ubuntu, and Fedora packages, and Windows support is still pending.

**「Takeaway」** Ladybird&\#x27;s Alpha is less a polished Chrome replacement than a concrete test of whether a fully independent, nonprofit browser engine can be built and sustained without search or data revenue. Its significance is in opening that engine to real-world testing while being explicit about the compatibility and security gaps and early performance questions that remain.

**Tags**: `#Ladybird`, `#浏览器内核`, `#开源浏览器`, `#Alpha 发布`, `#上手体验`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Report: US Commerce Department Pressured Intel for 10% Stake](https://www.wired.com/story/inside-trumps-demands-to-another-chips-ceo/) ⭐️ 9.0/10

WIRED, citing court filings, reported that a US Commerce Department lawyer told Intel’s CFO in August 2025 that the government’s demand for a 10% stake was not a negotiation and warned of unpredictable consequences if the board refused. The report says Intel’s board handed over the shares days later, and that the government paid nothing for a stake it said was then worth about $11 billion.

telegram · zaihuapd · Nov 25, 13:25

**「Background」** A New York Times report in November 2025 said the Commerce Department held a 9.9% Intel stake valued at $8.9 billion, part of the Trump administration’s broader practice of taking ownership stakes in private companies.

**「Impact」** If confirmed, the no-payment 10% stake would dilute existing Intel shareholders by about a tenth of the company at no cost to the government, and it would mark a rare direct U.S. government equity holding in a private firm — a step described as highly controversial and previously used mainly during the 2008–2009 financial crisis.

<details><summary>References</summary>
<ul>
<li><a href="https://www.nytimes.com/2025/11/25/us/politics/trump-intel-steel-minerals-china.html">Trump Administration Is Taking Billions in Stakes in Firms Like Intel ...</a></li>
<li><a href="https://techcrunch.com/2025/08/22/u-s-government-plans-to-take-a-10-stake-in-intel/">US government plans to take a 10 % stake in Intel | TechCrunch</a></li>

</ul>
</details>

**Tags**: `#美国商务部`, `#英特尔`, `#政府持股`, `#半导体产业`, `#产业政策`

---

<a id="item-finance-news-2"></a>
### [US Proposes New Tariffs on 14 Trading Partners, Including China and EU](https://www.cnbc.com/2026/11/25/us-tariffs-trump-section-301.html) ⭐️ 8.0/10

The US government is reportedly planning new Section 301 tariffs on 14 trading partners including China, the EU, Japan, India and South Korea, with country-specific rates rather than one blanket level. For China, the proposed levy would add 20% on top of existing 25% tariffs and could rise to 40% if China does not comply with the October 2025 Busan trade truce, according to the report.

telegram · zaihuapd · Nov 25, 13:59

**「Background」** Section 301 of the Trade Act of 1974 gives the Office of the United States Trade Representative authority to investigate foreign trade practices and respond by imposing tariffs. The proposed levies follow separate tariffs of 10% or 12.5% that the Trump administration applied to 60 trading partners in July, which the new measures would not stack on top of.

<details><summary>References</summary>
<ul>
<li><a href="https://www.congress.gov/crs_external_products/IF/PDF/IF11346/IF11346.31.pdf">Section 301 of the Trade Act of 1974 - Congress.gov</a></li>

</ul>
</details>

**Tags**: `#US trade policy`, `#Section 301 tariffs`, `#China-US trade`, `#EU trade`, `#global supply chains`

---

<a id="item-finance-news-3"></a>
### [UK energy bills to rise 26% from January as gas costs surge](https://www.bbc.co.uk/news/articles/cm20qnq33e90o?at_medium=RSS&amp;at_campaign=rss) ⭐️ 7.0/10

UK energy regulator Ofgem says its new three-month price cap will raise a typical household&\#x27;s annual energy bill by 26% from January, from £1,723 to £2,166 if that level is sustained for a year, reflecting a surge in wholesale gas costs.

rss · BBC Business · Nov 25, 13:42

**「Background」** Ofgem sets a three-month cap on household energy prices in England, Scotland and Wales, and the January-to-March cap is based on wholesale gas prices in the preceding three months, which rose 33%.

**「Who is affected」** The increase will affect households not on fixed-rate energy tariffs—millions of customers—while those with fixed deals fall outside the immediate cap change.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>
<li><a href="https://www.independent.co.uk/news/uk/home-news/energy-price-cap-increase-cost-b3091156.html">Energy bills to soar to £ 2 , 166 a year as energy price cap rises again</a></li>
<li><a href="https://www.independent.co.uk/news/uk/home-news/energy-price-cap-increase-cost-b3091156.html">Energy bills to soar to £2,166 a year as energy price cap rises again</a></li>
<li><a href="https://www.bbc.co.uk/news/articles/cm20qnq33e90o">Energy bills to rise by 26 % from January after gas prices surge</a></li>

</ul>
</details>

**Tags**: `#energy prices`, `#household bills`, `#gas prices`, `#cost of living`, `#UK economy`

---

<a id="item-finance-news-4"></a>
### [Shein to pay $100mn to settle US customer-deception allegations](https://www.ft.com/content/0128d44e-8ca1-49b8-868b-b8fe0e4824c6?syn-25a6b1a6=1) ⭐️ 7.0/10

Shein has agreed to pay $100 million to resolve US allegations that it misled customers about the origin of its cotton fabrics and suppressed negative reviews, according to a Financial Times report that did not name the regulator involved or the date of the settlement.

rss · FT Markets · Nov 25, 11:18

**「Background」** The allegations were brought by the US Federal Trade Commission, the country&\#x27;s consumer-protection regulator, and the $100 million is designated under the settlement as consumer redress — money returned to affected shoppers.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ftc.gov/news-events/news/press-releases/2026/11/shein-pay-100-million-over-allegations-deceptive-unfair-practices">SHEIN to Pay $100 Million Over Allegations of Deceptive and ...</a></li>

</ul>
</details>

**Tags**: `#Shein`, `#US consumer protection`, `#regulatory settlement`, `#fast fashion`, `#cotton sourcing claims`

---

<a id="item-finance-news-5"></a>
### [Bank of Korea raises rates to 3.25%, expects inflation above target](https://news.rthk.hk/rthk/ch/component/k2/1879324-20261126.htm) ⭐️ 7.0/10

South Korea&\#x27;s central bank raised its benchmark interest rate by 0.25 percentage point to 3.25%, a two-year high, matching market expectations, and said inflation will remain above its target for a considerable period.

rss · RTHK Finance · Nov 26, 02:11

**「Background」** The Bank of Korea aims to keep consumer price inflation at 2% over the medium term, so its warning that inflation will remain above target means above that 2% goal. The latest increase follows rate rises in July and August and a pause in October, bringing this year’s total to three increases worth 0.75 percentage point.

**「Impact」** The higher benchmark rate is likely to raise borrowing costs for South Korean households and businesses with variable-rate loans.

<details><summary>References</summary>
<ul>
<li><a href="https://www.bok.or.kr/eng/main/contents.do?menuNo=400530">General Principles of Monetary Policy Operation</a></li>

</ul>
</details>

**Tags**: `#南韓央行`, `#利率`, `#通脹`, `#經濟預測`, `#貨幣政策`

---