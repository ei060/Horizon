---
layout: default
title: "Horizon Summary: 2026-11-22 (EN)"
date: 2026-11-22
lang: en
---

> From 69 items, 9 important content pieces were selected

---

**Technology News**
1. [Lean formalization claims Riemann Hypothesis verification](#item-tech-news-1) ⭐️ 8.0/10
2. [Microsoft&\#x27;s RDMA over USB4 preview lets multiple Windows PCs share one local LLM](#item-tech-news-2) ⭐️ 8.0/10
3. [Zhejiang University reports first real-device QRAM on superconducting chip](#item-tech-news-3) ⭐️ 8.0/10
4. [GnuPG/GPGME flaw affects pre-2.3.0 software; RCE impact disputed](#item-tech-news-4) ⭐️ 7.0/10
5. [Dumpleton launches Muru, AI-assisted Rust ASGI/WSGI server](#item-tech-news-5) ⭐️ 7.0/10
6. [OpenRouter warns MiniMax model prompts may have been read by third parties](#item-tech-news-6) ⭐️ 7.0/10

**Technology Blog**
1. [Good Programming Is Mostly About Avoiding Blunders](#item-tech-blog-1) ⭐️ 6.0/10
2. [Dettato: Open-Source Multi-Instrument Audio-to-MIDI Transcription](#item-tech-blog-2) ⭐️ 4.0/10
3. [Synology DSM Patches Two Critical Flaws: OAuth API 9.8 and NGINX HTTP/2](#item-tech-blog-3) ⭐️ 4.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Lean formalization claims Riemann Hypothesis verification](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 8.0/10

A Lean formalization has been claimed to verify the Riemann Hypothesis, and the claim is under intensive discussion on Hacker News. The supplied material does not independently confirm the proof; the debate centers on whether a kernel bug could admit a false proof and on how much of the work was AI-assisted. Commenters also discussed whether the effort involved formalizing a large body of modern mathematics, with one saying Claude formalized a huge chunk of modern math.

hackernews · g-b-r · Nov 21, 14:36 · [Discussion](https://news.ycombinator.com/item?id=50589618)

**「Background」** The Riemann Hypothesis, posed in 1859, asserts that every non-trivial zero of the Riemann zeta function has real part 1/2. The Lean post follows Levent Alpöge&\#x27;s 20 November 2026 claim that he and Anthropic&\#x27;s Claude had found a proof and released it as Lean code; the blog reports that the exported proof was checked by Lean&\#x27;s official kernel, the con-leche and con-ron checkers bundled with Lean v4.36.0, and several third-party checkers implemented in different programming languages.

**「Impact」** The practical check is independent kernel verification: commenters note that separate implementations with their own consistency proofs make a shared kernel bug much less likely, but not impossible, so the claim should not be treated as established until that check is reported.

**「Community discussion」** Commenters disagreed over the strength of independent checking: one argued that a bug would now have to affect both the kernels&\#x27; consistency proofs and the RH proof, while another cited a past fake Collatz refutation that passed an independent checker and noted that human involvement was not part of the formal statement. Others credited the human guidance behind the AI-assisted effort and asked whether the result opens larger mathematical questions.

<details><summary>References</summary>
<ul>
<li><a href="https://www.clarin.com/us-news/who-is-levent-alpoge-the-anthropic-mathematician-who-claims-solved-the-riemann-hypothesis-with-claude_0_2WdGvYKBVM.html">Who is Levent Alpöge? The Anthropic mathematician who claims he...</a></li>
<li><a href="https://www.nacionale.com/en/articles/has-riemann-hypothesis-been-proved-levent-alpoge-claude-anthropic-claim-lean">Riemann hypothesis proof claimed with Claude , unverified</a></li>
<li><a href="https://leanprover-community.github.io/blog/posts/riemann-hypothesis/">Lean verification of the Riemann Hypothesis | Lean community blog</a></li>
<li><a href="https://math.mit.edu/~drew/grh/">RH Lean proof : verification files</a></li>

</ul>
</details>

**Tags**: `#formal verification`, `#Lean`, `#Riemann Hypothesis`, `#mathematics`, `#AI-assisted proof`

---

<a id="item-tech-news-2"></a>
### [Microsoft&\#x27;s RDMA over USB4 preview lets multiple Windows PCs share one local LLM](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 8.0/10

Microsoft released a developer preview of RDMA over USB4 for Windows that lets multiple PCs pool memory and GPU compute over ordinary USB4 cables, without a dedicated network card or switch, to run a single local AI model. In the demonstration, three AMD Ryzen AI Max+ 395 systems ran Qwen3-235B-A22B at 4-bit quantization at about 18.5 tokens per second. The capability is being distributed through Windows Insider. It remains a developer preview tied to specific hardware, so the demonstrated throughput is not a general guarantee.

telegram · zaihuapd · Nov 21, 06:13

**「What RDMA over USB4 changes」** RDMA \(Remote Direct Memory Access\) lets one computer read and write another machine&\#x27;s memory directly, bypassing the remote CPU, which is why it is normally associated with datacenter networking rather than consumer hardware. Microsoft&\#x27;s developer preview brings that capability to Windows 11 over ordinary USB4 cables, so two or more PCs can be joined into a single compute cluster without dedicated network adapters or switches.

**「Impact」** For local-AI users, the preview points to a way to run models too large for one machine&\#x27;s memory by linking commodity PCs rather than buying specialized networking gear. Anyone attempting it should expect USB4-equipped hardware and Windows Insider builds to be prerequisites, and should treat the three-machine Ryzen AI Max+ 395 result as a demo configuration rather than a baseline for other setups.

<details><summary>References</summary>
<ul>
<li><a href="https://habr.com/ru/articles/1110636/">Microsoft представила решение на базе USB 4 и RDMA для... / Хабр</a></li>
<li><a href="https://www.goha.ru/microsoft-dobavila-v-windows-11-tehnologiyu-rdma-po-usb4-dlya-obedineniya-neskolkih-pk-v-edinyj-lokalnyj-ii-klaster-lWoPRN">Microsoft добавила в Windows 11 технологию RDMA по USB 4 для...</a></li>

</ul>
</details>

**Tags**: `#RDMA`, `#USB4`, `#Windows`, `#local AI`, `#distributed inference`

---

<a id="item-tech-news-3"></a>
### [Zhejiang University reports first real-device QRAM on superconducting chip](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 8.0/10

Zhejiang University researchers report that they demonstrated quantum random-access memory \(QRAM\) on a superconducting quantum chip for the first time in a real device, using a home-built chip named Tianmu 2; the work was published in Nature Physics. The prototype retrieved 4-bit and 8-bit data with 80.9% and 60.4% accuracy, respectively. The team also reports that its circuit depth was more than 30% lower than an unoptimized approach and that the architecture showed local noise resistance. The researchers say the next step is scaling up QRAM.

telegram · zaihuapd · Nov 21, 08:31

**「Background」** QRAM is a proposed quantum memory architecture that lets an algorithm retrieve data at addresses held in superposition, a capability underlying many hoped-for quantum speedups but previously explored mainly in theoretical proposals and small proof-of-concept designs. The chip used in this experiment, Tianmu-2, is a 100-qubit superconducting processor jointly developed by Zhejiang University&\#x27;s superconducting quantum computing team and Hangzhou Logic Bit Technology, according to Baidu Baike.

**「Impact」** Because 8-bit retrieval reached only 60.4% accuracy \(and 4-bit 80.9%\), the prototype is not yet usable as a reliable memory for algorithms that assume clean, coherent data lookup — any QRAM-dependent routine run on it would inherit those error rates. The team has framed the next step as scaling the bucket-brigade architecture, which is the concrete prerequisite before developers could treat QRAM as a practical component rather than a hardware demonstration.

<details><summary>References</summary>
<ul>
<li><a href="https://baike.baidu.com/en/item/Tianmu-2/4929794">Tianmu-2_Baiduwiki - 百度百科</a></li>
<li><a href="https://producteast.com/china-demonstrates-the-worlds-first-quantum-random-access-memory-advancing-practical-quantum-computing/">China Demonstrates the World &#x27;s First Quantum... - Product East</a></li>
<li><a href="https://quantumnews.in/article/quantum-computing/zhejiang-university-achieves-breakthrough-worlds-first-superconducting-qram">Zhejiang University Achieves Breakthrough with World ’s First ...</a></li>
<li><a href="https://www.academia.edu/169067399/From_Experimental_Demonstration_to_Fault_Tolerant_Quantum_Interfaces_Bucket_Brigade_QRAM_Architectures_Surface_Code_Error_Correction_and_Neural_Decoding_Advances_in_2026">(PDF) From Experimental Demonstration to Fault-Tolerant Quantum...</a></li>

</ul>
</details>

**Tags**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#quantum memory`, `#research`

---

<a id="item-tech-news-4"></a>
### [GnuPG/GPGME flaw affects pre-2.3.0 software; RCE impact disputed](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 7.0/10

A GnuPG announcement describes a GPGME vulnerability whose remote-code-execution impact is disputed. A commenter says all software using GPGME versions before 2.3.0—whether as a shared library, DLL, or static link—is affected, citing Gpg4win, GnuPG Desktop, many mail and XMPP clients, Samba, and Flatpak as examples. A separate commenter said the flaw was disclosed on 2026-11-20 after an initial coordinated date of 2026-11-25 was moved up because GitLab had to update early amid the Ruby2Shell bug. Another commenter said Red Hat&\#x27;s packaging fixed the flaw five years ago but upstream missed it.

hackernews · gdgghhhhh · Nov 21, 08:32 · [Discussion](https://news.ycombinator.com/item?id=50587208)

**「Context」** GPGME is the GnuPG library that applications use to call GnuPG features such as signing and encryption. The advisory tracks the flaw as CVE-2026-129975 and says every application using GPGME before version 2.3.0 is affected, whether the library is shared, a Windows DLL, or statically linked; it also notes that 2.3.0 was never publicly available.

**「Patch requirement」** Applications that link GPGME before 2.3.0—whether as a shared library, a Windows DLL, or statically linked code—need to upgrade to 2.3.0 or later for CVE-2026-129975, including bundled copies that OS package updates may not cover. The advisory traces the fault to GPGME&\#x27;s internal status-line and key-listing parsers, so updating only the \`gpg\` binary is not the relevant fix.

**「Community discussion」** One commenter called it a double-free bug rather than an RCE chain and questioned whether vulnerability reports are intentionally overstated, while another said code execution via GitLab&\#x27;s signed-commit path would be serious. A further commenter argued that C/C++ development needs Rust-level tooling to prevent such memory-safety bugs.

<details><summary>References</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html">GnuPG Warns Critical GPGME Flaw Could Expose App Data via...</a></li>
<li><a href="https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html">[Announce] GnuPG Security Advisory for GPGME ...</a></li>
<li><a href="https://www.openwall.com/lists/oss-security/2026/11/20/13">oss-security - Fwd: GnuPG Security Advisory for GPGME ...</a></li>
<li><a href="https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html">GnuPG Warns Critical GPGME Flaw Could Expose App Data via...</a></li>

</ul>
</details>

**Tags**: `#security vulnerability`, `#GPGME`, `#GnuPG`, `#double-free`, `#coordinated disclosure`

---

<a id="item-tech-news-5"></a>
### [Dumpleton launches Muru, AI-assisted Rust ASGI/WSGI server](https://simonwillison.net/2026/Nov/21/muru/) ⭐️ 7.0/10

Graham Dumpleton, creator of mod\_wsgi, has launched Muru, an AI-assisted Rust server intended to run both ASGI and WSGI Python applications in development and production. The project is published at github.com/muruhq/muru and documented through an unusually detailed series of development posts published between November 4 and November 21, 2026, covering worker internals, combined WSGI/ASGI support, HTTPS in development, release-based restarts, canary deployments, Kubernetes integration, scaling to zero, and a tracing toolbar. Dumpleton frames the AI assistance as surface-level work while he judges readiness himself, drawing on two decades of mod\_wsgi experience; the supplied material includes no benchmarks, versioned release details, or evidence of adoption, so production readiness remains unverified.

rss · Simon Willison · Nov 21, 23:56

**「Background」** WSGI is Python&\#x27;s long-standing synchronous interface between web servers and applications, while ASGI extends that model to asynchronous apps. Graham Dumpleton&\#x27;s earlier mod\_wsgi, which he started 20 years ago, was built to host WSGI applications; Muru is a separate Rust server intended to support both ASGI and WSGI.

**「Migration consideration」** Teams with an existing WSGI application can evaluate Muru as a single server for both WSGI and ASGI, so adding WebSocket or async endpoints would not require maintaining a separate ASGI server alongside the WSGI deployment. Muru also advertises zero-downtime releases and traffic management, but the source provides no benchmarks or production-adoption evidence, so performance and operational maturity remain unverified.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/GrahamDumpleton/muru">GitHub - GrahamDumpleton/muru: Routing edge, control plane ...</a></li>
<li><a href="https://grahamdumpleton.me/posts/2026/11/muru-wsgi-and-asgi-together/">Muru: WSGI and ASGI together - Graham Dumpleton</a></li>

</ul>
</details>

**Tags**: `#Python`, `#ASGI/WSGI`, `#Rust`, `#Web servers`, `#mod\_wsgi`

---

<a id="item-tech-news-6"></a>
### [OpenRouter warns MiniMax model prompts may have been read by third parties](https://news.ycombinator.com/item?id=50585962) ⭐️ 7.0/10

OpenRouter emailed users warning that requests sent to MiniMax models may have been read by third parties, according to a report relayed secondhand through a Telegram channel and Hacker News. Security researchers who sent prompts containing test URLs to MiniMax models reportedly saw third parties access those URLs 40 to 130 hours later, with the report placing the tests between July and October 2026. OpenRouter attributed the issue to MiniMax and its forwarding providers AtlasCloud, Novita and StreamLake, removed the &quot;zero data retention&quot; labels from the affected endpoints, and advised users who had exposed sensitive credentials to rotate API keys and passwords. OpenRouter has not published anything about the incident on its own site, and the underlying details remain unverified.

telegram · zaihuapd · Nov 21, 06:53

**「What the ZDR label means」** OpenRouter&\#x27;s Zero Data Retention \(ZDR\) label refers to a policy under which prompts and responses are not routinely stored after processing, apart from a documented CSAM exception, and users can configure routing to use only endpoints with that policy, according to OpenRouter&\#x27;s documentation. Removing the label from the affected MiniMax endpoints therefore changes what those endpoints promise about retaining prompt data.

**「Impact」** Developers and organizations that routed prompts containing credentials, internal URLs or other sensitive data through MiniMax endpoints — including via AtlasCloud, Novita or StreamLake — should treat that traffic as potentially exposed and rotate the API keys and passwords referenced in those requests. Because the zero-data-retention label has been pulled from these endpoints, users can no longer rely on that designation when deciding where to send confidential data.

<details><summary>References</summary>
<ul>
<li><a href="https://openrouter.ai/docs/guides/features/zdr">Zero Data Retention - How OpenRouter gives you control over your...</a></li>

</ul>
</details>

**Tags**: `#ai-security`, `#data-privacy`, `#openrouter`, `#minimax`, `#api-security`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Good Programming Is Mostly About Avoiding Blunders](https://seangoedecke.com/to-code-well-avoid-blunders/) ⭐️ 6.0/10

rss · Sean Goedecke · Nov 22, 00:00

**「Background」** Sean Goedecke argues that in large commercial codebases with big teams—what he calls “impure engineering”—good programming depends less on brilliant insights than on avoiding catastrophic mistakes.

**「Solution」** He compares programming to chess and tennis: a player who never hangs a piece or miss-returns a ball can beat most opponents without producing brilliancies. Programming lacks a durable winning margin, he says, because one blunder—such as adding a parallel system, a second source of truth, an unnecessarily delicate async path, new subtle failure points, or a complicated interface—can turn an elegant codebase janky. The cardinal sins are inconsistency and unnecessary requirements: inconsistency destroys trust and forces engineers to hunt for surprises, while unnecessary requirements are sticky because later readers must assume they matter, and they interact combinatorially with every new feature. Goedecke therefore urges engineers to fit each task as normally as possible into the existing codebase and trim it to the smallest requirement set, treating thoughts of clever patterns or “extra credit” features as warning signs. He notes that coding agents match humans on consistency but are much worse at avoiding unnecessary requirements.

**「Takeaway」** The author’s larger point is that attention to detail and a laser focus on consistency and minimal requirements matter more than cleverness; indeed, cleverness can become a distraction.

**Tags**: `#software engineering`, `#code quality`, `#technical debt`, `#consistency`, `#requirements`

---

<a id="item-tech-blog-2"></a>
### [Dettato: Open-Source Multi-Instrument Audio-to-MIDI Transcription](https://www.appinn.com/dettato/) ⭐️ 4.0/10

rss · Appinn · Nov 21, 06:25

**「Background」** 你看到的内容可能由第三方 AI 基于小众软件文章提炼总结而成，可能与原文真实意图产生偏差。不代表小众软件观点和立场。请&lt;a href=&quot;https://www.appinn.com/dettato/&quot; target=&quot;\_blank&quot;&gt;点击链接阅读原文&lt;/a&gt;细致比对和校验。&lt;br /&gt;&lt;br /&gt;Dettato is an open-source music-transcription model from KobiMusic that runs locally on a CPU or GPU and converts recorded MP3 or WAV audio into editable MIDI. MIDI stores performance instructions—pitch, timing, duration, and velocity—rather than sampled sound, so musicians can inspect, slow down, correct, or re-voice a performance.

**「Solution」** Dettato separates transcription into four small models. A 15.3M-parameter annotator proposes note starts, ends, and pitches across 88 keys with two voices per key; a 4.9M evidence model removes wrong notes and repairs attacks, endings, and omissions; a 2.9M grouper assigns notes to instrument tracks and names them; and a 5.0M drums model maps percussion to General MIDI drum keys. Installation is one pip command from GitHub, and \`dettato song.mp3 -o out/\` produces \`song.mid\` plus a \`song.json\` recording track and note counts, downloading models from Hugging Face on first run; FFmpeg is suggested for unreadable MP3s. It requires Python 3.10+ and PyTorch 2.2+. The developer reports 87 seconds to transcribe 15 seconds of audio on a laptop CPU, including model loading, versus about 15 seconds for a four-minute song on an 8 GB RTX 5060 with peak VRAM under 4 GB; Apple Silicon Macs can run with \`--device cpu\`, but no Mac timing is given. The article does not explain the algorithm, accuracy, failure modes, or design tradeoffs, so those remain unverified.

**「Takeaway」** The author presents Dettato as a low-barrier, locally runnable route from mixed audio to per-instrument MIDI, including drums, using modest models. Its practical musical accuracy, however, remains untested in the article.

**Tags**: `#音频转MIDI`, `#Dettato`, `#音乐转录`, `#开源模型`, `#CPU/GPU性能`

---

<a id="item-tech-blog-3"></a>
### [Synology DSM Patches Two Critical Flaws: OAuth API 9.8 and NGINX HTTP/2](https://www.appinn.com/synology-dsm-critical-vulnerabilities-2026-11/) ⭐️ 4.0/10

rss · Appinn · Nov 21, 03:07

**「Background」** Note: this is a condensed retelling of the Appinn post and may diverge from the original, so verify against the source. On 19 November 2026 Synology published two critical advisories \(SA-26:21 and SA-26:20\) covering DSM and BeeStation OS — an unauthenticated OAuth API file read/write flaw and an NGINX HTTP/2 bug — leaving NAS administrators to work out how exposed they were and whether fixes were actually downloadable.

**「Solution」** According to the article, CVE-2026-120382 \(CVSS 3.1 9.8\) sits in how the DSM OAuth API handles command-parameter delimiters, letting a remote attacker read or write arbitrary files or knock services offline; the vector requires no privileges and no user interaction, so neither a DSM account nor a clicked link is needed. Apps relying on OAuth — the author cites Amazon Echo/Alexa playing music through Audio Station — may lose authorization or access, and Synology&\#x27;s stopgap is to stop the OAuth Service package. CVE-2026-123007 \(&quot;NGINX2Root&quot;, 8.1, rated Important inside a Critical notice\) affects NGINX with HTTP/2 enabled, crashing web services and, under specific conditions, enabling remote code execution; disabling HTTP/2 under Control Panel → Network → Connectivity is the interim measure, and third-party packages or Docker containers may also be exposed. Affected builds span DSM 7.4, 7.3, 7.2.2/7.2.1, 7.1 and BeeStation OS 1.5; the patch table marks 7.4.1-90080 Update 2 and 7.3.2-86009 Update 6 as released while older branches and BeeStation remain in progress — contradicting the headline&\#x27;s claim that updates are out, since a 20 November check found both advisories still &quot;Ongoing&quot; with the planned date unmet. Synology said no exploitation had been observed as of publication, and the author adds that QuickConnect itself was not confirmed vulnerable but recommends cutting public exposure via overlay networking \(Tailscale, ZeroTier\) and keeping offsite backups.

**「Takeaway」** The author&\#x27;s conclusion is that internet-exposed NAS storage stays high-risk regardless of vendor: patch when builds land, shrink the attack surface by disabling unneeded packages and public access, and remember that a platform with no disclosed flaws is not a platform without flaws.

**Tags**: `#Synology DSM`, `#OAuth API 漏洞`, `#NGINX HTTP/2`, `#安全公告`, `#NAS 安全`

---