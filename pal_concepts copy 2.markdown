---
layout: page
title: ALPHA and sovereignty (core Foundry high level Enterprise AI Concepts) (26.0922)
permalink: /pal_concepts222222222222222222222222/
---

<br>

This page is the ZAI take on the core ALPHA/SOV problems and Foundry solutions. From a tech/historical perspective.

**Short on time (TL;DR)? Skip to section C.**

The DoD has resources to use local models for their Palantir systems. Your enterprise may not have such resources -- you probably need to use external (not under your control) LLMs. thats a problem. A very big ALPHA/SOVereignty problem. PAL Foundry solves (or manages) those ALPHA/SOV problems.

<br>

#### **TOC**

- **Z. What is ALPHA/SOV**
- **V. Why LLMs want your ALPHA/SOVereignty**
- **W. What they are willing to do to get your ALPHA/SOVereignty**
- PAST, PRESENT, FUTURE of ALPHA/SOV
  - **B. (PAST) ALPHA/SOV Before LLMs**. a quick overview of the history of MS-DOS/WIN, Client Server, Google Search (they also focused on ALPHA/SOV, but without the sophisticated tools that AI LLMs have).
  - **C. (PRESENT) ALPHA/SOV after LLMs**. how Palantir (Alex Karp) alerted to the ALPHA/SOV problems and substantially mitigates the risks (**for the enterprise; protection for the PC?**).
  - **D. (FUTURE) ALPHA/SOV for the PC?**. Do you deserve Foundry protection? Foundry = NEW OS?

<!--    - C.0 NOTHING, NO PROTECTION??? #####################
    - C.1 Enterprise + LLMs = (BIG) PROBLEMS (AI API v3)
    - C.2 Foundry_Enterprise + LLMs = SOLUTIONS (AI API v4) -->

<br>

See also

- **[2.2x CONCEPTS (DEEP DIVE) -- ZAI Foundry demos](/3c.2_pal_demo_CONCEPTS/)** for more info (describes concepts for the 7/8 demos).

<br>

---

---

---

<br>

# **Z. What is ALPHA/SOV**

- Alpha = your company's business model, workflows, secrets<br>_A chinese official leaked ALPHA (this would not happen had they been using Founddry)._<br><img src="/assets/wuxi-42.png" alt="xxx" width="50%" style="border: 1px solid #999;"><br><br>
- SOV = your independence from a specific AI LLM provider.<br>_Palantir AIP provides total sovereignty from any specific model (@600)._<br><img src="/assets/wuxi-41.png" alt="xxx" width="60%" style="border: 1px solid #999;"><br><br>

<br>

---

---

---

<br>

# **V. Why LLMs want your ALPHA/SOVereignty**

Because a pattern matching algorithm needs the patterns of others to survive. Like a vampire wants blood, or a search engine wants to crawl the universe.

- **V.1 Real intelligence (human sensory organs and brain based)**
- **V.2 AI (LLM-based) core components**
- **V.3 AI simulated intelligence (clocked state machine HACK)**
- **V.4 The Hack MUST (to survive) steal training (pattern matching) materials (and your ALPHA)**
- **V.5 SOV: If you stored some of your UNIQUE ALPHA in LLM1, then switching to LLM2 wont work**

<!--
- **V.6 AGI is a STING, a distraction, a fraud** (used to get ALPHA/SOV)
- **A.1 The sting**. AGI is a distraction. LLM shops want you to believe that LLMs are intelligent (and that you can trust them and tell them all your technical secrets)
- **A.2 AI (LLM-based) core components**. External agent and the LLM (internal agent + transformer).
- **A.3 AI HACK**. The human brain (real intelligence). AI is simulated intelligence (a hack).
- **A.4 The Hack relies totally on stealing ALPHA/SOV** (plagiarizing intelligent content / locking in token subscribers) -->

See also the "[HACK](/0-demo/)" webpage.

<br>

### **V.1 Real intelligence (human sensory organs and brain based)**

The human

- (1) sees (or hears, touches (Braille)) words
- (2) generates thoughts from those words (thoughts exist only in time)
- (3) generates answer thoughts
- (4) converts those thoughts to words.

Its pretty simple, because the real magic is in the intelligent brain.

_(53)_<br><img src="/assets/wuxi-53.png" alt="xxx" width="60%" style="border: 1px solid #999;"><br>

<br>

### **V.2 AI (LLM-based) core components**

LLMs are, on the other hands, exceedingly complicated.

The **core components of (LLM-based) AI** (see diagram below)

- **external agent (CPU)**
  - procedural (CPU) code that your write that uses the LLM.
  - eAgent contains the end user central logic (business logic)

- **internal agent (CPU)**
  - procedural (CPU) code that runs the main loop and controls LLM input/output.
  - Very closely customized to TF.
  - feeds required prompts into TF and process responses.
  - responds to eAgent

- **TF (GPU)** (NEEDS TRAINING INPUT)
  - 1 (main) **pattern matching** in "machine language" space
  - 2 **"thinking"** (and other **simulations** of intelligent thought)... these are also pattern matching.
  - 3 **language models** (Transformers; they convert inexact human representation of meaning (words) into massive amounts of numbers that are used to compute the exact "machine language" meaning)

<!-- _(52)_<br><img src="/assets/wuxi-52.png" alt="xxx" width="36%" style="border: 1px solid #999;"><br> -->

_(left) eAgent on the PC (47) and (right) in the enterprise (46)_<br><img src="/assets/wuxi-47.png" alt="xxx" width="36%" style="border: 1px solid #999;"> <img src="/assets/wuxi-46.png" alt="xxx" width="46%" style="border: 1px solid #999;">

<br>

### **V.3 AI simulated intelligence (clocked state machine HACK)**

**AI (TF is the core, the source of the "AI")**

- (1) sees, hears, touches NOTHING.
- (2) binary data (representing prompt) is converted into numerical representations. For each token in GPT-3 that means 12K FP numbers (this is complex encoding/representation of the computed meaning, including context, vastly more info than just a few letters).
- (3) TF performs pattern match on all the machine language numbers (KEY CAPABILITY OF TF: vastly different letter inputs can end up with very closely matched machine language results)
- (4a) after many iterations the output is a CLASSIFICATION -- a set of probabilities for all tokens. Usually the token with highest probability is chosen as the output token (which is then appended to the input and then the cycle repeats) (the most probable token is not chosen when the LLM is programmed to trick the user with random output to give the impression of real intelligence rather than deterministic programming; LLMs are 100% deterministic in their computations)
- (4b) the cycle repeats until the the iAgent/TF determine that the answer is complete

_(hack-01) TF algorithm (GPT-3)_<br><img src="/assets/hack-01.png" alt="xxx" width="41%" style="border: 1px solid #999;"><br>

**NOTE: AI (4a) Classification possibilities:**

- ONLY about 50K (50K vocab tokens).
- this means determining next token based on machine_language_space pattern matching (many patterns match a single token... there are google's of patterns, but only 50K total classifications; so many patterns match a single classification).

<br>

### **V.4 The Hack MUST (to survive) steal training (pattern matching) materials (and your ALPHA)**

For training the LLM (training = programming the patterns into the LLM, not giving the LLM human style skills or intelligence). stealing instructions, book material, concepts, secrets, etc, thats all quite common. THe LLM gets the info from somewhere, and the model is trained on it. And like magic, the author's rights are null and void, and the knowledge/intelligence is available to the world for the cost of the tokens.

but what about your enterprise ALPHA? The workflows that provide the core value to your product? THe LLM Steals your intelligence to create patterns for their LLMs and then offers your intelligence to the world for the cost of generating tokens.

_(55-111)_<br><img src="/assets/wuxi-55-111.png" alt="xxx" width="25%" style="border: 1px solid #999;"><br>

_(55-333)_<br><img src="/assets/wuxi-55-333.png" alt="xxx" width="25%" style="border: 1px solid #999;"><br>

<br>

### **V.5 SOV: If you stored some of your UNIQUE ALPHA in LLM1, then switching to LLM2 wont work**

**In diagram 111 in previous section "prompt engineering... vibe coding.."** this means that your enterprise is defining increasingly higher level prompts that are interpreted in a specific way by LLM1. INevitably you start to adjust your enterprise side to the specifics of LLM1. Switching to LLM2 will probably results in unexpected responses.

- The more your enterprise sends your ALPHA to an LLM, the more you are risking not only having ALPHA stolen, but **loosing SOVereignty**.
- From the very beginning their goal is to lock you into their LLMs

- **NOTE: PayPal's Musk's might be taking a unique tactic to deny SOV**. His (the PayPal mafia's) favorite tactic is a monopoly; he undoubted plans to try to lock in customers to his Grok by controlling their options for AI LLMs, by getting them to depend on "Star"Link...this will be a unique way to deny SOV (only Musk will have such a monopoly).

<!-- >
- ALSO the more you move your ALPHA into the LLM (with prompts that slowly change your product into a vibe coding product), the more the LLM can replicate (and offer to the world for the price of a token) your core ALPHA. -->

_(55-222)_<br><img src="/assets/wuxi-55-222.png" alt="xxx" width="25%" style="border: 1px solid #999;"><br>

<!--_(51) The Sting_<br><img src="/assets/wuxi-51.png" alt="xxx" width="40%" style="border: 1px solid #999;"><br>

 #### **extAgent** (needs business logic)

- eAgent contains the end user central logic (business logic)

 _(49)_<br><img src="/assets/wuxi-49.png" alt="xxx" width="37%" style="border: 1px solid #999;"><br><br> -->

<!--#### **iAgent**

- iAgent (very closely customized to TF) uses
  - proc code to feed required prompts into TF and process responses.
  - central loop
  - responds to eAgent

 _(49)_<br><img src="/assets/wuxi-49.png" alt="xxx" width="37%" style="border: 1px solid #999;"><br><br> -->

<!--#### **GPU space details (TF)**

 _(48)_<br><img src="/assets/wuxi-48.png" alt="xxx" width="10%" style="border: 1px solid #999;"><br><br> -->

<!-- ### **A.3 Why LLMs must steal (like a vampire)**

- LLMs must steal the patterns to match against. **THEY WANT YOUR ALPHA**. the LLM house that can steal the most high quality patterns wins the war.<br>_A chinese official leaked ALPHA._<br><img src="/assets/wuxi-42.png" alt="xxx" width="50%" style="border: 1px solid #999;"><br><br>
- They want to do this with Musk-style monopolies, convincing you that they are your friend. **THEY WANT TO TAKE AWAY YOUR SOVEREIGNTY**.<br>_Sovereignty means independence from AI models (@6mins)._<br><img src="/assets/wuxi-41.png" alt="xxx" width="60%" style="border: 1px solid #999;"><br><br>

<br> -->

<br>

---

---

---

<br>

# **W. What they are willing to do to get your ALPHA/SOVereignty**

<br>

### **W.1 AGI is a STING, a distraction, a fraud (used to get ALPHA/SOV)**

Many gurus are walking back their predictions about AGI. Musk recently said he expected AGI in a few years (thats ridiculous statement). The focus on **AGI is a distraction**. LLM shops want you to believe that LLMs are intelligent so that you

- Become totally dependent on their wares (why bother thinking about anything if a super-duper AGI is going to be doing all the thinking for us all?). **(ADD LINK TO BESTPARTNER \_c376_2026.0316_best_partner_agi_andrew_ng.mp4 WHERE SAID THAT CEO'S ACTUALLY STARTED STOPPING INVESTING BECAUSE AGI WAS GOING TO TAKE OVER)**
- NO NEED FOR PAL TYPE SYSTEMS, or FOR ALPHA/SOV. you just take one LLM (whoever is promising AGI) and it will do everything for you.
- the sooner or later phenomenon
  - Musk promised FSD a decade ago; he has not delivered, but he has sold a lot of "FSD" cars, and no Tesla owners seem to hold it against him (I guess Musk did his best)
  - its natural human behavior for his fans to forgive the real life Tony Stark for not delivering, focusing instead on what he has delivered, in the belief that all great achievements dont always occur on time.
  - this is similar to how the Gates discovered that people were very forgiving of the shortcomings of his OS if they believed he'd eventually get it right.

Andrew Ng warned about this... he said that **if AI made too many promises and did not deliver, then they might lose their funding**. Ng is my favorite Guru, but even he is in the end focused 100% on the health of the AI sting, not those getting stung.

Andrew says below "Will this be the year 2026 of AGI?". He then talks about a computer will pass the AGI test if it can carry out the work task as well as a skilled human. Am I missing something, because this whole topic of AGI being achieved by some test reminds me of my classmates and I remarking in Junior High school (50 years ago) that calculators were already smarter than humans because they could do complex math so well. So now 50 years later AGI is achieved if some binary calculator can pass some test? Do these people have even the slightest idea of what is of intelligence?

_(50)_<br><img src="/assets/wuxi-50.png" alt="xxx" width="80%" style="border: 1px solid #999;"><br>

<br>

---

---

---

<br>

<!-- # **X PAST, PRESENT, FUTURE of ALPHA/SOV**

**(B) (PAST) ALPHA/SOV before LLMs**. Section B is a quick overview of the history of MS-DOS/WIN, Client Server, Google Search (they also focused on ALPHA/SOV, but without the sophisticated tools that AI LLMs have).

_PC (the eAgent is on the PC) (47)_<br><img src="/assets/wuxi-47.png" alt="xxx" width="36%" style="border: 1px solid #999;">

**(C) (PRESENT) ALPHA/SOV with LLMs (the problems and the Foundry solutions)**. Section C focuses on how Palantir (Alex Karp) alerted to the ALPHA/SOV problems and substantially mitigates the risks.

_Enterprise (the eAgent is in Foundry) (46)_<br><img src="/assets/wuxi-46.png" alt="xxx" width="48%" style="border: 1px solid #999;">

**(D) (FUTURE) ALPHA/SOV for the PC?**

<!-- - (currently a consultancy / not a monopoly, but a business model; future tool for the masses? / public version?)
- **Overly complicated demos** that dont stay laser-focused on the topics Alex talks about or on the main point of the demo.
- **UI, terminology, and docs that leave you in confusion**.
- **Limited geographical availability, cost, etc.**
- Foundry sometimes seems like a tool for a consulting business, not a consumer product, dev tool. --

_(56) Do you deserve Foundry protection? Foundry = NEW OS?_<br><img src="/assets/wuxi-56.png" alt="xxx" width="50%" style="border: 1px solid #999;">


<br>

---

---

---

<br> -->

# **B. (PAST) ALPHA/SOV Before LLMs**

#### **TOC**

- B.0 Mainframes (60ya)
- B.1 Microsoft used Windows to extract ALPHA (40 years ago). Microsoft did all it could do to steal your alpha and sovereignty. The goal was a monopoly (the same for AI shops now).
- B.2 Browser + URLs.
- B.3a/b Client/Server (browser/non-browser agents/apps). REST APIs (20ya). The basis of networking and remote access. Data security becomes a real problem.
- B.4a/b Google Search (AI API v1/v2) (browser/non-browser agents/apps) (server becomes risk). AI APIs for AI search engines (20ya). The Google search revolution based on language models. AI started tracking you and stealing your data in real time.

<br>

---

<br>

### **B.0 Mainframes (60ya)**

<br>

---

<br>

### **B.1 Microsoft used Windows to extract ALPHA (40ya)**

no safe alpha for app/agent in consumer PC market. anyone could (1) buy the app, (2) install on OS, and (3) (especially Microsoft) reverse engineer the workflows with the help of OS calls.

_Agent (app) on Win OS on PC; the red line is where ALPHA is lost._<br><img src="/assets/wuxi-33.png" alt="xxx" width="19%" style="border: 1px solid #999;"><br><br>

40 years ago when DOS and then Windows appeared, developers of core business logic (ALPHA) had a new platform that provided the complex computational foundation required for app dev.

One I (vaguely) remember was WordPerfect. They came out with an excellent word processor for Windows (DOS?). This was an excellent product who core functionality and workflows were quite easily extracted by those who build the OS that the app was dependent on.

Soon MS came out with their own WordPerfect: Microsoft Word. Word was a mess, some chaotic implementation that MS bought from someone else, but MS added an extra layer with a WorkPerfect style UI and workflows.

When MS changed their OS, MS.Word was already ready to go. Others like WordPerfect had to play catch up. Because the OS was the "HOME" of consumer. It was a business that made Gates very wealthy.

Now the tech has changed but the game is the same. Now the AI titans want their LLM to be the HOME of the consumer. 40 years ago the platform was the IBM PC that provided the worldwide standard. Musk (and the PayPal 3.0 mafia) are hoping that in the future it will be the "Star" link constellation.

**How Microsoft did it back then**

MS controlled the operating system. For some reason IBM when they came out with the PC they thought the OS was not important, and licensed it from MS. That made Gates the richest man in the world. The OS was the LLM of that time. That incredibly complex piece of binary logic HW/SW (HW was from Intel, the Nvidia of the day) that everyone was dependent upon as the basis for running their apps.

The OS had a Kernel (compare roughly to an LLM transformer) and a bunch of SW surrounding the Kernel that controlled the kernel and interfaced with the external world. Comparable to the LLM internal agent.

_OS (=> LLM)_<br><img src="/assets/wuxi-30.png" alt="xxx" width="25%" style="border: 1px solid #999;">

The apps back then were the equivalent of the (external) agents of today. They contained the core business logic that defined a product.

It wasn't really possible to take the app code and reverse engineer, but MS did not have to. They knew the OS inside and outside (like the Frontier labs know their LLMs), so all they had to do was scan what the app was sending/receiving to/from the OS and the reverse engineering was easy.

_App (=> "extAgent")_<br><img src="/assets/wuxi-31.png" alt="xxx" width="25%" style="border: 1px solid #999;">

<br>

---

<br>

### **B.2 Browser + URLs [REST API v1]**

- browser is the agent. stateless. very little "ALPHA" on the app/agent (browser).
- **the revolutionary part: the plumbing used to connect browser/server.** that "plumbing would form the basis of client/server tech (next bullet).

_The REST API (with URL and DNS) was a revolutionaryly simple way to connect 2 computers._<br><img src="/assets/wuxi-34.png" alt="xxx" width="25%" style="border: 1px solid #999;"><br><br>

<br>

---

<br>

### **B.3 Client/Server [REST API v2/v3]** (browser/non-browser agents/apps)

**3a [REST API v2] Client/Server browser-based apps/agents**

- USE THE BROWSER AS A PLATFORM.
- NOTE: The agent is a webapp that is downloaded from the SERVER. Interacts with the server. The real ALPHA is on the server. Your client ALPHA is probably quite limited.<br>_The server contains the ALPHA (ALPHA is safe if the server is secure (likely))._<br><img src="/assets/wuxi-35.png" alt="xxx" width="50%" style="border: 1px solid #999;"><br><br>

**3b [REST API v3] Client/Server (REST apps/agents)**

- THE APP/AGENT REPLACES THE BROWSER. Interacts with the server. REAL ALPHA appears on the client.<br>_The client contains the ALPHA (ALPHA is at risk if the client is not secure (quite likely))._<br><img src="/assets/wuxi-36.png" alt="xxx" width="40%" style="border: 1px solid #999;"><br><br>

<br>

---

<br>

### **B.4 Google Search (AI API v1/v2) (browser/non-browser agents/apps) (server becomes risk)**

**4a [AI API v1] Google search (AI server becomes risk)**.

- First time the agent (in the browser) connects to an AI API. The output is unpredictable. But usually just used as info response... so no real danger. <br>_Client side agent inside browser; limited risk of ALPHA leakage in chats._<br><img src="/assets/wuxi-37.png" alt="xxx" width="46%" style="border: 1px solid #999;"><br><br>

**4b [AI API v2] Google search**.

- writing agents that use the Google API.THe agent ALPHA can all be picked up by Google (they already pick up all of your history to create personalize ads).<br>_Client side agent running in OS; high risk of ALPHA leakage._<br><img src="/assets/wuxi-38.png" alt="xxx" width="40%" style="border: 1px solid #999;"><br><br>

- ASK **OS: CAN YOU RUN THIS?**,
- ask **GOOGLE: Do you have a tool for this?** (just use google account for access),

- client/server not so safe anymore... but answer is still not an action
- prompt becomes alpha

**GOOGLE IT**

Eric Schmidt recently started making attack drones. "Dont be evil" :). Google collaborated with Fauci who was running a bioweapons lab in Wuhan. Google faithfully blocked anything it was told to block.

Google has a whole ecosystem built around those that use its search engines. In a way, AI is just a souped-up version of a search engine (google hit the jackpot by basing its search not on keywords, but on the AI-version of the real meaning of words and sentences; the core of AI is the LLM that converts keyword (token) input into real "machine" language QKV representations of meaning for effective pattern matching).

<br>

---

---

---

<br>

# **C. (PRESENT) ALPHA/SOV after LLMs**

AI APIs LLMs and Foundry (5ya). AI is tracking far more than your clicks and your searches. You even start using it for business processes and intel. But you are not appreciating what the token sellers are up to

#### **TOC**

- **C.0 PC + LLMs = (BIG) PROBLEMS (AI API v3a)**
- **C.1 Enterprise + LLMs = (REALLY BIG) PROBLEMS (AI API v3b)**
- **C.2 Foundry_Enterprise + LLMs = SOLUTIONS (AI API v4)**

<br>

---

<br>

### **C.0 PC + LLMs = (BIG) PROBLEMS (AI API v3a)**

<br>

---

<br>

### **C.1 Enterprise + LLMs = (BIG) PROBLEMS (AI API v3)**

- PAL was the first to alert to the problem of ALPHA when using external LLMs in enterprise (Alex Karp’s “Alpha” concept discussions)
- When you start using external AI (**external Frontier models**) as assistants, then you have to take special precautions so that these Frontier labs can not
  - (1) steal your enterprise intelligence and
  - (2) integrate into their model or
  - (3) sell to others (in the form of tokens).<br>_Access to external means severe risks for ALPHA leakage._<br><img src="/assets/wuxi-44.png" alt="xxx" width="63%" style="border: 1px solid #999;"><br><br>

<!-- - When you ask
  - OS to run something: OS gives answer or error code,
  - GOOGLE (search) for info: GSearch gives (1) what it finds and (2) what its overlords determine is the "truth" you should have access to.
  - LLM for help:

The LLM will give the best token sequence that matches your prompt. The LLM provider's business is for you to pay for generated tokens.-->

#### **TOC:**

- **C.1.1 (ext)Agent/LLM is the new app/OS paradigm**
- **C.1.2 LLM (TF) delivers pattern recognition (and empty AGI promises)**
- **C.1.3 (3/4) The "steal" is a natural result (of patttern recognition)**
- **C.1.4 (5/6/7) How the "steal" is done**
- **C.1.5 (8) End goal: $100 trillion monopolies**. Your yourself will own nothing (no ALPHA) and be happy.

<!-- - **C.1.1 The (ext)Agent/LLM is the new app/OS paradigm**
- **C.1.2 AI (1) promise AGI, but (2) deliver pattern recognition (tokens)**
- **C.1.3 Your most valueable core logic is “OUTSIDE THE MODEL SPECTRUM”**. Because your core ideas (ALPHA) are not patterns, but hard logic.
- **C.1.4 Why LLMs steal ALPHA?**
- **C.1.5 How LLMs steal ALPHA**
- **C.1.6 THE STEAL WONT BE AS GOOD AS THE ORIGINAL ALPHA**
- **C.1.7 Examples of “stealing ALPHA” (Humanonoid FSD)**
- **C.1.8 End goal: AI titan monopolies (You will own nothing (no ALPHA) and be happy)**. -->

<br>

#### **C.1.1 The (ext)Agent/LLM is the new app/OS paradigm**

<!-- C2b) What is LLM / agent -->

**LLM = equivalent of OS**. The diagram below shows the internal stucture of an LLM. The part of the LLM that makes it able to generate token sequences that mimic intelligent resonses is the **transformer (TF)**. The TF is a GPU-based computing engine. The **"internal" agent (iAgent)** is a procedural program (like Python, TypeScript) that (1) controls the TF and (2) interfaces with the external world (you). Note that the iAgent/TF

- are very complicated and designed to work closely work together (iAgent must be totally customized to the TF; iAgent will contain vast amounts of "glue" logic)
- need language and "thinking" patterns to simulate (fake) human thinking.

**this is far less reliable than procedural code**.

_LLM_<br><img src="/assets/wuxi-28.png" alt="xxx" width="45%" style="border: 1px solid #999;">

**(External) Agent = equivalent of the application (business logic)**. (ext)Agentic = the non-human user of the AI (LLM) API. extAgent can use AI in various modes:

- **Chat, action, auto (reaction), action/auto**
- **Single shot / loop**

_AI agent_<br><img src="/assets/wuxi-29.png" alt="xxx" width="25%" style="border: 1px solid #999;">

<br>

#### **C.1.2 LLM (TF) delivers pattern recognition (and empty AGI promises)**

You can compare LLMs to search engines on steroids. But the LLM does far more than just return search results.

- The LLM transformer (TF) computes the classification of the current prompt/response, and
- that classification is used to select the next token to add
- (this process is repeated until the TF or internal agent decide to stop).
- The LLM internal Agent orchestrates TF input to construct complex final responses.

There is no intelligence. Only pattern matching to classifications (tokens) that were "imprinted" on the LLM during "training" that used massive amounts of (often plagiarized) input token sequences (training text).

Therefore its only logical that the frontier models have the following main business goals:

- (1) You are dependent on (no sovereignty from) their model(s)
- (2) Their models can "steal" any intelligent business data (your ALPHA). And that is only logical, since the model sells you other people intelligence for a price.

<br>

---

<br>

AI has nothing, absolutely nothing, to do with real intelligence (See the page **[HACK](/0-demo/)**).

- AI = clocked state machine. a snapshot in time means something.
- real intelligence (human, mouse, bird, etc): time based. like a flame. it has no fixed state.
- we understand context: QKV makes meaning pattern matching possible. classification becomes next token.
- LLM spits out best classification which becomes the next token.
- The classification concept of AI can be used in many areas. For example
  - FSD (full self driving) has many inputs which are used to select a set of outputs (used to drive the car)
  - Object Recognition classification (dog or cat)

<br>

#### **C.1.3 (3/4) The "steal" is a natural result (of patttern recognition)**

**(C.1.4) Why LLMs steal ALPHA?**

- they **will steal your company secrets**. - (2) that intelligence used immediately to offer to other customers (as RAG) or (3) that intel used for "insider training" of the next model

- LLMs are built on pattern matching, that gives the illusion of intelligence.
- Therefore, it only natural that they must steal any intelligent patterns they can.
- They learn nothing, understand nothing. Only patterns.

- **A frontier lab LLM has no intelligence; it will fake the required skills**. And possibly cause a lot of trouble. Something like FSD without the human caretakers.
- LLMs are dumb binary computational algorithms (token generators) with absolutely no intelligence. LLMs ARE A **[HACK](/0-demo/)** that simulates intelligent conversations by generating response words based on input_word_sequence patterns.
- You will be competing against
  - (1) others like yourself and
  - (2) amateurs who are putting an AGI humanoid robot in the drivers seat and calling this their FSD product (Musk does this to some extent with his army of human operators who are 24/7 ready to save any Tesla that is in a situation that FSD was not programmed to handle).

<br>

**You can not stop them**

If you give **frontier models** ("frontier" = the most advanced major models) access to your business logic, then

- **there is nothing legal you can do to stop them**. Its similar to when countries that have no IP (intellecutual property) laws allow their own to steal someone else's ideas, then those that put so much investment into creating something new lose it all. thats losing alpha. Thats what LLM's do.
- They will be doing do to you what they have already done to countless authors of original material used to "train" (program) their frontier models. You might have started out not planning to give the LLM insider info, but by doing "prompt engineering" instead of "data engineering", you expose what is unique about your business model to the LLM (something I have done regularly when discussing in depth in long chats the core concepts of ZAI with GPT).

<br>

**(C.1.3) Your ALPHA is "OUTSIDE THE MODEL SPECTRUM"? Then just fake it in the LLM or add to the iAgent**

- "ALPHA" = Alex Karp's term for your core biz logic.
- **The core logic for your business is not in the AI, but in your business processes**.
- The core procedural code (pipeline, ontology, analysis) is your secret... you may use external LLMs as assistants, but you never give them enough to steal your ideas.

Your core business logic/ideas are intelligently encoded hard logic, not patters "learned" by an LLM during automated "training". your procedural logic (extAgent) is

- far more intelligent and reliable than the simulated “thinking” of LLMs (that is based on pattern recognition and training) because
- the intelligence of a human was used to program a procedural spec in the extAgent.

<img src="/assets/wuxi-22-3.png" alt="xxx" width="50%" style="border: 1px solid #999;">

<br>

#### **C.1.4 (5/6/7) How the “steal” is done**

(C.1.5) How LLMs steal ALPHA

<!--**2 ALPHA leakage to external LLMs**
3.2 DECODED: Loosing alpha = From "your company" to "vibe coding"
Loosing alpha = From "your company" to "vibe coding" -->

<!-- - These demos compare external, internally controlled, and hybrid AI architectures to determine what the organization actually controls. The focus is not only data protection, but also model replaceability, application ownership, operational continuity, and control of decisions and outcomes.

_How an LLM "plagiarizes" (steals) your alpha_<br><img src="/assets/wuxi-03.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>  -->

MS was able to install programs locally then run them and sniff out what happened. But Inside your enterprise, the **AI apps (external agents) are not running locally on the Frontier LLMs, so the Frontier labs are dependent on you providing the intelligence** they require to copycat your workflows. The following is an examples.

_Your company (with the intro of AI and automation... and no ALPHA guardrails)_<br><img src="/assets/wuxi-22-1.png" alt="xxx" width="68%" style="border: 1px solid #999;">

_The result of ALPHA leakage is loss of ALPHA (1) Alpha moves to model (your product is now "vibe"code), (2) model is now the alpha product, (3) your customers migrate_<br><img src="/assets/wuxi-22-2.png" alt="xxx" width="50%" style="border: 1px solid #999;">

<br>

**(C.1.6) THE STEAL WONT BE AS GOOD AS THE ORIGINAL ALPHA**

If ALPHA is leaked to the LLM, then something like the following would occur:

- At first the ALPHA would be stored as RAG.
- The ALPHA is trained into the next model.
- NOTE: This would not 100% replicate the original business practices.

_ALPHA mined from plagiarized prompt submissions? (screenshot from Mining demo D5)_<br><img src="/assets/wuxi-27.png" alt="xxx" width="54%" style="border: 1px solid #999;">

<br>

**(C.1.7) Examples of "stealing ALPHA" (Humanoid FSD)**

Imagine you hire a humanoid AI robot as a taxi driver. And that humanoid sends AI requests to an external AI lab (the humanoid is basically an external agent to an LLM; let assume for the simplcity of this demo that the humanoin does all visual object recognition (etc) locally).

You use this taxi driver to run some kind of specialized delivery business. And business is good. You found a niche market that is scalable and profitable. The driver gets commands from you, but has to access the remote LLM to "understand" these commands.

You dont realize it, but the LLM quickly learns everything about your business. And its only natural that the Frontier lab starts wondering about offering such an intelligent taxi driver as an integral part of its model.

_You humanoid was a Trojan horse who gave you business ALPHA to an AI titan (vibe coding at its worst)._<br><img src="/assets/wuxi-18.png" alt="xxx" width="85%" style="border: 1px solid #999;">

<br>

#### **C.1.5 (8) End goal: $100 trillion monopolies**

Your yourself will own nothing (no ALPHA) and be happy.
End goal: AI titan monopolies (You will own nothing (no ALPHA) and be happy)\*\*

_**[Sovereignty (ALPHA)](/3c.2_pal_2.0_sovereignty/)** = Who ultimately controls the data, models, application, workflows, decisions, and operational future?_

The AI titans also want to be the ALPHA AI providers. Their shareholders and government collaborators allso want the same. Musk has been promising FSD for a decade, and still has not delivered. Tesla has an army of human service engineers to help any Tesla that gets "stuck" in some kind "does not compute!" situation. FSD is still a pie-in-the-sky wish. **StarLink** (note the word "star") **is probably also a Trojan Horse whose real goal is some kind of monopoly and ensuring extraction (and resale) of ALPHA.** A better name might be "PlagiarizeLink".

I saw a great video of Peter Thiel from about 10 years ago where he was letting the cat out of the bag about his approach to business: Monopolies. Thats what Starlink is all about. The idea is for StarGrok to become the new omnipresent AI in the sky. Being able to listen in to all the chats about business processes. It would be interesting if Musk (actually, its not just him but a whole group behind him) could pull off what MS did 40 years ago.

**FINAL RESULT: You will own nothing (no ALPHA) and be happy (doing vibe coding and paying for output tokens)**

<!--

_Losing alpha_<br><img src="/assets/wuxi-02.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>

- You dont pay google by the number of answers you get.
- Its like a movie generated with just a few prompts.

- you no longer are alpha, and you have little value.
- this is what "vibe" coding means. the viral initial popularity of vibe coding reflected a total lack of understand of what AI (the ZAI website goes into detail about what it really is.... see the "Hack" page)
- what is generated depends on what someone initial human input designed.. and then was basically stolen into the AI training. -->

<br>

---

<br>

### **C.2 Foundry_Enterprise + LLMs = SOLUTIONS (AI API v4)**

PAL Foundry offers solutions (on RAILS, similar to REST API CONTROLS)\*\*. Foundry is a modern enterprise platform that is the best solution for avoiding ALPHA loss (and the perfect culmination of ZipteiAI's AI focus).

_Foundry adds governance to the enterprise that puts access to external LLMs "on rails"._<br><img src="/assets/wuxi-40.png" alt="xxx" width="71%" style="border: 1px solid #999;"><br><br>

The solutions are primarily
(1) ALPHA governance and
(2) LLM sovereignty

<!-- OS app ALPHA was saved by client/server architecture.
app no long needed to be installed on device.
ALPHA was not on device.

Browser becomes a mini-OS itself, client server.
API's safely restrict what data gets sent to external systems.

PAL does this with AI.
THIS IS JUST THE START OF THIS NEW PARADIGM. -->

<!--
**PAL exposes these problems and offers solutions (Alex Karp’s “Alpha” concept)**
1b (C5)) (2) ALPHA (sovereignty) (AI external) [4]

IMPORT =================================================

- **Foundry core concept "ALPHA"/sovereignty** (that Alex Karp has been talking about a lot recently).
- **Other Foundry concepts** (data protection, etc; my own take)
- **Maximize ALPHA/sovereignty / Data protection** (within performance/cost/complexity limitations)

The value of Foundry is

- **Foundry forces compliance with safe AI practices**. Foundry makes you think about the requirements for enterprise AI.
- **Palantir leadership (such as Alex Karp) are very verbal about some very real problems with AI in the enterprise**. They are the only ones exposing the real issues, the hype (while minimizing their own marketing hype).

Note that you could implement these same concepts without using Foundry. Foundry simply makes it easier to do.

-->

#### **TOC**

- **C.2.1 Foundry + Create your own internal model (with Foundry)**. The perfect solution, except that models are difficult to create.
- **C.2.2 Foundry provides (1) ALPHA governance and (2) LLM sovereignty**. Foundry stops the steal.

<!--
  - **### DONT SHARE ALPHA WITH LLMS ###**
  - share only non-alpha stuff
  - carefully quanitify and control ALPHA
- **B.6.3 -1.3c (2.3) DECODED 3: Your most valueable core logic is "OUTSIDE THE MODEL SPECTRUM"**. You can do silly vibe coding demos, but real world apps, unique, with specialized biz processes, can not be created using pattern matching LLMs. **I THINK WHAT THIS MEANS IS IF YOU ARE CAREFUL ABOUT LEAKAGE, LLMs CAN NOT STEAL YOUR IDEAS**.
- **3.4 WHY and HOW THEY STEAL ALPHA: MINING DEMO D5**
<
#### **B.6.2 (-2.0) ALPHA: The Alex Karp ALARM (encoded version)**
<!-- **1.5 how PAL raised the alarm**. how PAL (Karp) alerts to the problem.
- BELOW: Alex Karp sounding the alarm about sovereignty in the enterprise (it took me a while to understand that I think he meant... I am still not 100% sure what he meant, but I am pretty sure about my take on "alpha".
- NOTE the sign behind Alex: Own your own outcomes, Own your models, Own your destiny. ??
<img src="/assets/alex222.png" alt="xxx" width="60%" style="border: 1px solid #999;">
-->
<!--
**EXAMPLE:** Farming out your ALPHA is like hiring a taxi driver who can take customer requests, and you call this your FSD productd. If you use an external frontier model for too much of your alpha, then the frontier lab will steal "your" product (you dont have product actually). This is vibe coding (at its worst).<br><img src="/assets/wuxi-18.png" alt="xxx" width="54%" style="border: 1px solid #999;">
-->

<br>

#### **C.2.1 Foundry + Create your own internal model (with Foundry)**

You could compare this to 40 years ago actually working on a mainframe (not a PC), and access to workflows was tightly controlled. Foundry provides the tools to create your own models.

THe problem with this solution: locally trained and deployed model is a lot of work. And for a lot requirements for AI in an enterprise it would be overkill.

_The "ideal" solution to ALPHA/SOV is the local model._<br><img src="/assets/wuxi-32.png" alt="xxx" width="40%" style="border: 1px solid #999;">

<br>

#### **C.2.2 Foundry provides (1) ALPHA governance and (2) LLM sovereignty**

- on RAILS, similar to REST API CONTROLS
- governance that secures ALPHA
- SOV that provides hot-switching of LLMs

_Foundry adds governance to the enterprise that puts access to external LLMs "on rails"._<br><img src="/assets/wuxi-40.png" alt="xxx" width="71%" style="border: 1px solid #999;"><br><br>

_Ontology defines actions, etc that never go to an LLM ... Thus they can not be used to reverse engineer your alpha._<br><img src="/assets/wuxi-22-2b.png" alt="xxx" width="50%" style="border: 1px solid #999;">

<br>

- **EXAMPLE: Keeping alpha using Foundry (D2 example)**. In D2
  - AI usage:
    - 3 difference models are used.
    - 2 models in the pipeline to prepare the dataset.
    - 1 model in the AIP logic in the UI to call the LLM that answers a question based on pipeline data.
  - No model gets the whole picture.
  - Models only get the grunt work (doing what transformers do best: pattern recognition)
  - The "thinking" is real in such an algorithm, becuase a human specifically wrote the logic
    - This is the opposite of how "thinking" is simulated in LLM's.

<!-- _Alpha_<br><img src="/assets/alex222.png" alt="xxx" width="55%" style="border: 1px solid #999;"> -->

<!-- - **3 The frontier model is a token generator** (nothing more). But **your core procedural code** ("agent" that has been customized to work with your AI models) **= proprietary knowledge that never gets sent to an LLM so can't be stolen (at least by an LLM)**. -->

<br>

---

---

---

<br>

# **D. (FUTURE) ALPHA/SOV for the PC?**

MAIN

- the bikker jacket dude wants PCs built that host his HW.
- need open HW.
- Need some kind of PAL system to protect ALPHA/SOV.
  - **Do you deserve Foundry protection?**
  - **Foundry = NEW OS?**

OTHER

- (currently a consultancy / not a monopoly, but a business model; future tool for the masses? / public version?)
- **Overly complicated demos** that dont stay laser-focused on the topics Alex talks about or on the main point of the demo.
- **UI, terminology, and docs that leave you in confusion**.
- **Limited geographical availability, cost, etc.**
- Foundry sometimes seems like a tool for a consulting business, not a consumer product, dev tool.

_(56)_<br><img src="/assets/wuxi-56.png" alt="xxx" width="50%" style="border: 1px solid #999;">

<br>

26.0922 (v1 26.0804)

<!-- ===============================================================================================

# ===============================================================================================

# ===============================================================================================

### **1.0 Why Foundry**

Foundry is a modern enterprise platform for

- data integration,
- ontology,
- analytics,
- applications,
- **AI assistance**, and
- governance.

_Foundry enterprise platform functionality"_<br><img src="/assets/wuxi-01.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>

My focus (for now) is on Palantir Foundry because:

- Foundry takes a **very practical no-nonsense approach to AI in the enterprise** (see the 2 images below). Foundry was a market leader over 20 years ago (long before AI).
- Foundry represents the **logical culmination of ZiptieAI: (2) neural networks → (2b) models → (3) agents → (3b) workflows** (and finally) **→ (3c) enterprise platforms**.
- Palantir offers a **generous Foundry free trial**.
- Foundry's **built-in AI assistant (FDE) makes hands-on self-study practical**.

_Palantir provides proven engineering (the crystal ball is just a metaphor, marketing genius); those selling AGI are selling a fantasy that can cause big problems in an enterprise._<br><img src="/assets/pal_9_06.png" alt="drones" width="25%" style="border: 1px solid #999;"> <img src="/assets/777_02.png" alt="drones" width="30%" style="border: 1px solid #999;"><br>

- Foundry makes the enterprise visible and governable by bringing data from many systems into a common operational model that can be analyzed, monitored, and updated. AI is used as a helpful engineering tool, not a replacement for human judgment. Because LLMs are probabilistic, their access and actions must be controlled, verified, approved, and logged.
  - _ME: Those 3 sentences were obviously AI-generated. I simply asked GPT to write a good summary, because I was short on time and just need a few blurbs. An example of losing "alpha". That basically means let an intelligenct meanial laborer (GPT) take over an executive position._

**My focus (for now) is on Palantir (Foundry)** because (_this list is WIP..._)

- Palantir is a market leader.
- Palantir offers a generous free trial account for Foundry.
- **Palantir enterprise systems utilize AI as a helpful assistant** (not as a replacement for human intelligence).
- **Palantir's built-in AI help (FDE) makes it possible to complete the demos** (without human assistance).
- Palantir Foundry makes the enterprise visible and governable.
- Data from many systems is transformed into a common operational model that can be analyzed, queried, monitored, and updated.
- LLMs play the role of helpful assistants, but their very presence makes parts of the system probabilistic. As a result, AI actions must be sandboxed, verified, approved, and logged.
- **Palantir Foundry represents the logical culmination of ZiptieAI:** (see header on this webpage) (2) neural networks, (2b) models, (3) agents, (3b) workflows, and finally **(3c) enterprise platforms** brought together in a single system.
- Finally: Palantir's approach appealing is that **AI is used as a powerful engineering tool within a governed enterprise platform**, rather than as a replacement for human judgment. -->

<!--
<br>

#### **1.2 Why all the fuss about AI in the enterprise** (and how Foundry can mitigate these problems)

For the diagram below:

- **My original title:** _The fantasy world -- (left) a crystal ball (called a "palantir" ("seeing stone") in The Lord of the Rings) and (right) **AGI (a myth that digital circuits can host intelligence). Palantir Foundry** represents the real world -- An enterprise system that **provides the infrastructure and safeguards so that AI can be a practical "helpful assistant"** (not super-human intelligence)._
- **GPT's strongly suggested "professional" title:** _The trusted wizard (left) using a crystal ball ("palantir" or "seeing stone" in The Lord of the Rings) and (right) modern AI running on digital hardware. Both promise enhanced visibility and insight, although one belongs to fantasy and the other **(AGI) belongs to engineering**._

<br>

### **1.1 Keeping "alpha"** (away from token generators that want to steal/resell your IP)

LLMs get paid to generate tokens.. that is their business model; this will inevitably conflict with your desire to keep your enterprise secrets secret.

**TOC**

- There is another, perhaps the most important, reason to use Foundry: "Keeping alpha".
- Its like a movie generated with just a few prompts..
- How they (real life frontier models, not AGI) steal alpha
- Keeping alpha using Foundry (example)
- Loosing alpha ... to Foundry?

-->

<!--
#### **Loosing alpha ... to Foundry?**

In D5 (biz process mining) I get the impression that you give Foundry your alpha? In any case, this is not losing it to an LLM that will share with anyone willing to pay.

_Biz process mining ... giving alpha to Foundry?? The following has an eery resemblance to a vibe pipeline..._<br><img src="/assets/biz_process_mining.png" alt="drones" width="65%" style="border: 1px solid #999;">

<br>

# **OLD**

I am still working on **my own take on the core conceptual gist of Palantir-SW**, but basically its

- Palantir makes the enterprise visible and governable.
- LLMs make parts of that visibility probabilistic, so they must be sandboxed, verified, and logged.

See also **[Concept CHATS](/pal_chats/)**.

In the diagram below

- LEFT: Before LLMs, the Palantir-SW had just wizards/magic-balls (the analyzers and the watchers of the analyzers) that were implemented in procedural programming. Trustd, reliable and safe (not human, but programmed by a trusted human programmer-employee). Like the old wizard in Lord of the Rings.
- RIGHT: With LLMs, the Palantir-SW now has new AI wizards/magic-balls embedded inside the old wizards/magic-balls. AI has no intelligence (and can not be trusted). An LLM is programmed on training data that you did not control (and you can not determine the training data from analyzing the model, even if you knew the NN weights/biases). And the model is often remote. This requires extra security that Palantir-SW provides. **You need Palantir-type systems now more than ever.**

_The trusted wizard (left) with his crystal ball (called a "palantir" ("seeing stone") in The Lord of the Rings) and (right) an LLM (AGI = super human intelligence hosted on digital circuits; this is more of a myth than "Lord of the Rings"; LLMs have no intelligence and therefore can not be trusted)_ <br><img src="/assets/pal_9_06.png" alt="drones" width="25%" style="border: 1px solid #999;"> <img src="/assets/777_02.png" alt="drones" width="30%" style="border: 1px solid #999;"><br>

<br>

# **CORE DIAGRAMS**

<br>

### **1 palantir.com/docs/foundry**

_(numbers added)_<br><img src="/assets/777_08.png" alt="drones" width="64%" style="border: 1px solid #999;">

-->
<!-- <br>

*before AI*<br><img src="/assets/777_07.png" alt="drones" width="74%" > -->

<!-- **AI CREATION DETAILS NEEDED**
- NO DIRECT LLM ACTIONS ("usually not directly")
- deterministic/human-approved

*with AI helpful assistant (**3b WRITE = 3b ACTION**)*<br><img src="/assets/777_09.png" alt="drones" width="74%" > -->

<!--
### **2 Main diagrams for example/demo/deep-dive** (26.0806)

<br>

#### **2.1 The initial workflow diagrams**

For the demos I wanted a more mechanistic conceptual overview (I am more interested in the mechanics of the PAL tools used than the business cases). At first I wanted something like the simple Foundry workflow diagram below with text to summarize what parts an example/demo covered.

_Basic PAL diagram_<br><img src="/assets/777_07.png" alt="drones" width="74%" >

For example, for Code Repo demo D19, this is what is covered

```
1 Data source          ✓ raw CSV datasets
1b Pipeline            ✓ code-based PySpark transforms
3 Ontology read        —
3b Actions/writeback   —
4 Analysis             —
5 UI/app               —
6 Security/governance  ✓ branching, commits, checks, build
AI                     xxAI, except optional AIP Assist
```

<br> -->

<!--

But I prefer the more detailed diagram below. The idea is to show
- All possible workflow
  - steps
  - functionality (as text below the diagram)
- Highlight all those aspects used in
  - ORANGE for examples (which install everything for you)
  - RED for demos/deep-dives (which required you to build everything)

For example the main diagram for **[E11](/3c.1b_pal_examples/)** (example 11).

*(MAIN_E11.png)*<br><img src="/assets/MAIN_E11.png" alt="drones" width="74%" >

<br>
-->

<!--
#### **2.2 Current workflow diagrams**

**[E11](/3c.1b_pal_examples/)**. Example main diagram for E11 (example 11): shows the main workflow; orange squares highlight those items included in example install.

_(MAIN_E11.png)_<br><img src="/assets/MAIN_E11.png" alt="drones" width="74%" >

**[D19](/3c.2_pal_initial_demos/)**. Example main diagram for D19 (demo 19): shows the main workflow; red squares highlight those items implemented for demo D19 (this is a a very rought first draft that will change greatly as I figure out the details).

_Numbers 1-6 (1a,1b) correspond to the numbers I added to the main diagram above (from palantir.com/docs/foundry) (MAIN_D19.png)_<br><img src="/assets/MAIN_D19.png" alt="drones" width="74%" >

<br>

#### **2.3 Future diagrams**

At some point I will start to "weed out" the things that dont belong in each main diagram. I dont want all that useless verbiage (I might have a master main diagram that has all the text, for not for each example/demos). But for now I want to keep a lot of the verbiage as my own notes (until I get to understanding all the details better).

_(MAIN_E17.png)_<br><img src="/assets/MAIN_E17.png" alt="drones" width="74%" >

-->

<!--

<br><br>

---

---

---

---

<br><br>

# **A. Executive summary**

- A.1 The AI hack (kind of a short version of the "Hack" webpage). **This explains why the vampires need your blood (ALPHA/SOV).**
- A.2 A historical review of ALPHA/SOV
  - 1 Mainframes and PCs (40ya). Microsoft did all it could do to steal your alpha and sovereignty. The goal was a monopoly (the same for AI shops now).
  - 2 REST APIs (20ya). The basis of networking and remote access. Data security becomes a real problem.
  - 3 AI APIs for AI search engines (20ya). The Google search revolution based on language models. AI started tracking you and stealing your data in real time.
  - 4 AI APIs LLMs and Foundry (5ya). AI is tracking far more than your clicks and your searches. You even start using it for business processes and intel. But you are not appreciating what the token sellers are up to

<br>

## A.1 The AI hack (kind of a short version of the "Hack" webpage)

- why the focus on AGI? the LLM shops want you to trust them... they are lieing.
- the core functions of LLMs
  - 1 (main) pattern matching
  - 2 "thinking" (and other **simulations** of intelligent thought)... these are also pattern matching.
  - 3 language models (Transformers, etc)

for 1 and 2 above,

- LLMs must steal the patterns to match against. **THEY WANT YOUR ALPHA**.
- the LLM house that can steal the most high quality patterns wins the war
- They want to do this with Musk-style monopolies, convincing you that they are your friend. **THEY WANT YOUR SOVEREIGNTY**.

They can do this automatic (MS DOS/win also focused on ALPHA/SOV, but did not have the sophisticated tools).

<br>

## A.2 A historical review of ALPHA/sovereignty

<br>

### 1 Mainframes and PCs

- **0 Mainframes**

- **1 Microsoft used Windows to extract ALPHA (40 years ago)**.
  - no safe alpha for app/agent in consumer PC market. anyone could (1) buy the app, (2) install on OS, and (3) (especially Microsoft) reverse engineer the workflows with the help of OS calls.<br>_Agent (app) on Win OS on PC; the red line is where ALPHA is lost._<br><img src="/assets/wuxi-33.png" alt="xxx" width="19%" style="border: 1px solid #999;"><br><br>

### 2 REST APIs

- **2 [REST API v1] Browser + URLs**.
  - browser is the agent. stateless. very little "ALPHA" on the app/agent (browser).
  - **the revolutionary part: the plumbing used to connect browser/server.** that "plumbing would form the basis of client/server tech (next bullet).<br>
    _The REST API (with URL and DNS) was a revolutionaryly simple way to connect 2 computers._<br><img src="/assets/wuxi-34.png" alt="xxx" width="25%" style="border: 1px solid #999;"><br><br>

- **3a [REST API v2] Client/Server browser-based apps/agents**.
  - USE THE BROWSER AS A PLATFORM.
  - NOTE: The agent is a webapp that is downloaded from the SERVER. Interacts with the server. The real ALPHA is on the server. Your client ALPHA is probably quite limited.<br>_The server contains the ALPHA (ALPHA is safe if the server is secure (likely))._<br><img src="/assets/wuxi-35.png" alt="xxx" width="50%" style="border: 1px solid #999;"><br><br>

- **3b [REST API v3] Client/Server (REST apps/agents)**.
  - THE APP/AGENT REPLACES THE BROWSER. Interacts with the server. REAL ALPHA appears on the client.<br>_The client contains the ALPHA (ALPHA is at risk if the client is not secure (quite likely))._<br><img src="/assets/wuxi-36.png" alt="xxx" width="40%" style="border: 1px solid #999;"><br><br>

### 3 AI APIs for AI search engines

- **4a [AI API v1] Google search (AI server becomes risk)**.
  - First time the agent (in the browser) connects to an AI API. The output is unpredictable. But usually just used as info response... so no real danger. <br>_Client side agent inside browser; limited risk of ALPHA leakage in chats._<br><img src="/assets/wuxi-37.png" alt="xxx" width="46%" style="border: 1px solid #999;"><br><br>

- **4b [AI API v2] Google search**.
  - writing agents that use the Google API.THe agent ALPHA can all be picked up by Google (they already pick up all of your history to create personalize ads).<br>_Client side agent running in OS; high risk of ALPHA leakage._<br><img src="/assets/wuxi-38.png" alt="xxx" width="40%" style="border: 1px solid #999;"><br><br>

### 4 AI APIs for LLMs and Foundry

- **5 [AI API v3] External LLMs in the Enterprise (AI API v2 ; server = LLMs)**.
  - PAL was the first to alert to the problem of ALPHA when using external LLMs in enterprise (Alex Karp’s “Alpha” concept discussions)
  - When you start using external AI (**external Frontier models**) as assistants, then you have to take special precautions so that these Frontier labs can not
    - (1) steal your enterprise intelligence and
    - (2) integrate into their model or
    - (3) sell to others (in the form of tokens).<br>_Access to external means severe risks for ALPHA leakage._<br><img src="/assets/wuxi-44.png" alt="xxx" width="63%" style="border: 1px solid #999;"><br><br>

- **6 [AI API v4] PAL Foundry offers solutions (on RAILS, similar to REST API CONTROLS)**
  - Foundry is a modern enterprise platform that is the best solution for avoiding ALPHA loss (and the perfect culmination of ZipteiAI's AI focus).<br>_Foundry adds governance to the enterprise that puts access to external LLMs "on rails"._<br><img src="/assets/wuxi-40.png" alt="xxx" width="71%" style="border: 1px solid #999;"><br><br>

- **7 The Foundry business model**
  - (currently a consultancy / not a monopoly, but a business model; future tool for the masses? / public version?)

<!--  - **1.1b Losing alpha to... Foundry?** (no.. Foundry may extract intelligence, but Foundry is not in the AI model intellectual property repackaging business) --

<br><br>

---

---

---

--- -->
