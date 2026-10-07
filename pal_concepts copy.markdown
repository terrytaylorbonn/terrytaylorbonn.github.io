---
layout: page
title: Enterprise AI Concepts (high level, Palantir Foundry) (26.0918, v1 0911)
permalink: /pal_conceptsadsfasfdsaadsf/
---

<br>

This page is the ZAI take on the core Palantir concept of "ALPHA sovereignty". Even if you won't be using Foundry, the techniques Foundry uses to solve this problem are of universal interest.

- **1 The problem with AI (LLMs) in the Enterprise**. Alpha = your company's business model, workflows, secrets. When you start using AI (**external Frontier models**) as assistants, then you have to take special precautions so that these Frontier labs can not
  - (1) steal your enterprise intelligence and
  - (2) integrate into their model or
  - (3) sell to others (in the form of tokens).
- **2 PAL exposes these problems and offers solutions (Alex Karp’s “Alpha” concept)**
  - PAL was the first to alert to the problem of ALPHA.
  - Foundry is a modern enterprise platform that is the best solution for avoiding ALPHA loss (and the perfect culmination of ZipteiAI's AI focus).
- **3 The Foundry business model** (currently a consultancy / not a monopoly, but a business model; future tool for the masses / public version?)

See also

- **[2.2x CONCEPTS (DEEP DIVE) -- ZAI Foundry demos](/3c.2_pal_demo_CONCEPTS/)** for more info (describes concepts for the 7/8 demos).

<!--  - **1.1b Losing alpha to... Foundry?** (no.. Foundry may extract intelligence, but Foundry is not in the AI model intellectual property repackaging business) -->

<br>

---

---

<br>

## **1 The problem with AI (LLMs) in the Enterprise**

- **1.1 Microsoft used Windows to extract ALPHA** (40 years ago)
  - **GOOGLE IT**.. google takes over
- **1.2 The (ext)Agent/LLM is the new app/OS paradigm**
- **1.3 They (1) promise AGI, but (2) deliver pattern recognition (tokens)**
  - we understand context: QKV makes meaning pattern matching possible. classification becomes next token.
  - FSD: many inputs, get "QKV", objRecog meaning: classification = action to take.
- **1.3b Pattern recognition / tokens WANT vibe coding (YOU HAVE NO ALPHA; YOU WILL OWN NOTHING AND BE HAPPY)**
  - You dont pay google by the number of answers you get.
  - Its like a movie generated with just a few prompts.
- **1.4 How they (real life frontier models, not AGI) steal alpha**
- **1.5 Examples** (of stealing alpha). Humanonoid FSD / TokenLink.
- **1.6 End goal: Monopolies (Gates, Musk).** They want to be ALPHA. Their shareholders and government collaborators are your worst enemy. (Musk less so; but he did give DaLu robots and FSD; he wants NASA to be his feeding trough).

<br>

#### **1.1 Microsoft used Windows to extract ALPHA (40 years ago)**

40 years ago when DOS and then Windows appeared, developers of core business logic (ALPHA) had a new platform that provided the complex computational foundation required for app dev.

One I (vaguely) remember was WordPerfect. They came out with an excellent word processor for Windows (DOS?). This was an excellent product who core functionality and workflows were quite easily extracted by those who build the OS that the app was dependent on.

Soon MS came out with their own WordPerfect: Microsoft Word. Word was a mess, some chaotic implementation that MS bought from someone else, but MS added an extra layer with a WorkPerfect style UI and workflows.

When MS changed their OS, MS.Word was already ready to go. Others like WordPerfect had to play catch up. Because the OS was the "HOME" of consumer. It was a business that made Gates very wealthy.

Now the tech has changed but the game is the same. Now the AI titans want their LLM to be the HOME of the consumer. 40 years ago the platform was the IBM PC that provided the worldwide standard. Musk (and the PayPal 3.0 mafia) are hoping that in the future it will be the "Star" link constellation.

**GOOGLE IT**

Eric Schmidt recently started making attack drones. "Dont be evil" :). Google collaborated with Fauci who was running a bioweapons lab in Wuhan. Google faithfully blocked anything it was told to block.

Google has a whole ecosystem built around those that use its search engines. In a way, AI is just a souped-up version of a search engine (google hit the jackpot by basing its search not on keywords, but on the AI-version of the real meaning of words and sentences; the core of AI is the LLM that converts keyword (token) input into real "machine" language QKV representations of meaning for effective pattern matching).

- ASK **OS: CAN YOU RUN THIS?**,
- ask **GOOGLE: Do you have a tool for this?** (just use google account for access),
- ASK **LLM: can you do this?** (see pics, create table, generate images, buy ticket, etc etc etc...)

<br>

---

<br>

**How Microsoft did it back then**

_NOTE: I am in China 26.0916 when writing this... I need AI to help me do this section, diagrams, etc. These diagrams are not correct... will fix after return to USA._

MS controlled the operating system. For some reason IBM when they came out with the PC they thought the OS was not important, and licensed it from MS. That made Gates the richest man in the world. The OS was the LLM of that time. That incredibly complex piece of binary logic HW/SW (HW was from Intel, the Nvidia of the day) that everyone was dependent upon as the basis for running their apps.

The OS had a Kernel (compare roughly to an LLM transformer) and a bunch of SW surrounding the Kernel that controlled the kernel and interfaced with the external world. Comparable to the LLM internal agent.

_OS (=> LLM)_<br><img src="/assets/wuxi-30.png" alt="xxx" width="25%" style="border: 1px solid #999;">

The apps back then were the equivalent of the (external) agents of today. They contained the core business logic that defined a product.

It wasn't really possible to take the app code and reverse engineer, but MS did not have to. They knew the OS inside and outside (like the Frontier labs know their LLMs), so all they had to do was scan what the app was sending/receiving to/from the OS and the reverse engineering was easy.

_App (=> "extAgent")_<br><img src="/assets/wuxi-31.png" alt="xxx" width="25%" style="border: 1px solid #999;">

<br>

#### **1.2 The (ext)Agent/LLM is the new app/OS paradigm**

<!-- C2b) What is LLM / agent -->

**LLM = equivalent of OS**. The diagram below shows the internal stucture of an LLM. The part of the LLM that makes it able to generate token sequences that mimic intelligent resonses is the **transformer (TF)**. The TF is a GPU-based computing engine. The **"internal" agent (iA)** is a procedural program (like Python, TypeScript) that (1) controls the TF and (2) interfaces with the external world (you). Note the following

- iA/TF are very complicated and designed to closely work together (iA must be totally customized to the TF)
- need language and "thinking" patterns to simulate (fake) human thinking. **this is far less reliable than procedural code**.

_LLM_<br><img src="/assets/wuxi-28.png" alt="xxx" width="45%" style="border: 1px solid #999;">

**(External) Agent = equivalent of the application (business logic)**. (ext)Agentic = non-human using AI (LLM). Note that your procedural logic (extAgent) is

- far more intelligent and reliable than the simulated "thinking" of LLMs (that is based on pattern recognition and training) because
- the intelligence of a human was used to program a procedural spec in the extAgent.

extAgent can have following variations:

- **Chat, action, auto (reaction), action/auto**
- **Single shot / loop**

_AI agent_<br><img src="/assets/wuxi-29.png" alt="xxx" width="25%" style="border: 1px solid #999;">

<br>

#### **1.3 They (1) promise AGI, but (2) deliver pattern recognition (tokens)**

**(See "HACK" page) AI has nothing, absolutely nothing, to do with real intelligence:**

- AI = clocked state machine. a snapshot in time means something.
- real intelligence (human, mouse, bird, etc): time based. like a flame. it has no fixed state.

- we understand context: QKV makes meaning pattern matching possible. classification becomes next token.
  - spits out nearest classification... - > next token.
- **FSD: many inputs, get "QKV", objRecog meaning: classification = action to take.**

<br>

#### **1.3b Pattern recognition / tokens WANT vibe coding (YOU HAVE NO ALPHA; YOU WILL OWN NOTHING AND BE HAPPY)**

you dont pay google by the number of answers you get.

**Its like a movie generated with just a few prompts..**

- you no longer are alpha, and you have little value.
- this is what "vibe" coding means. the viral initial popularity of vibe coding reflected a total lack of understand of what AI (the ZAI website goes into detail about what it really is.... see the "Hack" page)
- what is generated depends on what someone initial human input designed.. and then was basically stolen into the AI training.

_Losing alpha_<br><img src="/assets/wuxi-02.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>

<br>

#### **1.4 How they (real life frontier models, not AGI) steal alpha**

Its similar to when countries that have no IP (intellecutual property) laws allow their own to steal someone else's ideas, then those that put so much investment into creating something new lose it all. thats losing alpha. Thats what LLM's do.

LLM's steal alpha not by understanding, but by

- (1) LLMs designed to capture any unique intelligence
- (2) that intelligence used immediately to offer to other customers (as RAG)
- (3) that intel used for "insider training" of the next model

You might have started out not planning to give the LLM insider info, but by doing "prompt engineering" instead of "data engineering", you expose what is unique about your business model to the LLM (something I have done regularly when discussing in depth in long chats the core concepts of ZAI with GPT).

_How an LLM "plagiarizes" (steals) your alpha_<br><img src="/assets/wuxi-03.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>

<br>

#### **1.5 Examples of "stealing ALPHA" (Humanonoid FSD / TokenLink)**

MS was able to install programs locally then run them and sniff out what happened. But Inside your enterprise, the **AI apps (external agents) are not running locally on the Frontier LLMs, so the Frontier labs are dependent on you providing the intelligence** they require to copycat your workflows. The following are 2 examples.

<br>

**Example 1: Humanoid AI taxi driver**

Imagine you hire a humanoid AI robot as a taxi driver. And that humanoid sends AI requests to an external AI lab (the humanoid is basically an external agent to an LLM; let assume for the simplcity of this demo that the humanoin does all visual object recognition (etc) locally).

You use this taxi driver to run some kind of specialized delivery business. And business is good. You found a niche market that is scalable and profitable. The driver gets commands from you, but has to access the remote LLM to "understand" these commands.

You dont realize it, but the LLM quickly learns everything about your business. And its only natural that the Frontier lab starts wondering about offering such an intelligent taxi driver as an integral part of its model.

You think that Frontier labs are too "virtuous" for such dirty dealings? Remember that Musk has been promising FSD for a decade, and still has not delivered. In fact, Tesla has an army of human service engineers to help any Tesla that gets "stuck" in some kind "does not compute!" situation. FSD is still a pie-in-the-sky wish.

_If you use an external frontier model for too much of your alpha, then the frontier lab will steal "your" product (you dont have product actually). This is vibe coding (at its worst)._<br><img src="/assets/wuxi-18.png" alt="xxx" width="85%" style="border: 1px solid #999;">

<br>

**Example 2: Musk's "PlagiarizeLink"**

I saw a great video of Peter Thiel from about 10 years ago where he was letting the cat out of the bag about his approach to business: Monopolies. Thats what Starlink is all about. Whereas the IBM PC (the open architecture) for a long time had a near monopoly on personal PC's, and Windows ruled the OS, seems like the plan for Starlink to become in the AI era what the PC was.

The idea is for StarGrok to become the new omnipresent AI in the sky. Being able to listen in to all the chats about business processes .. would be interesting if Musk (actually, its not just him but a whole group behind him) could pull off what MS did 40 years ago.

<br>

#### **1.6 End goal: Monopolies (Gates, Musk).**

They want to be ALPHA. Their shareholders and government collaborators are your worst enemy. (Musk less so; but he did give DaLu robots and FSD; he wants NASA to be his feeding trough).

<br>

---

---

<br>

## **2 PAL exposes these problems and offers solutions (Alex Karp’s “Alpha” concept)**

<!-- 1b (C5)) (2) ALPHA (sovereignty) (AI external) [4] -->

IMPORT =================================================

- **Foundry core concept "ALPHA"/sovereignty** (that Alex Karp has been talking about a lot recently).
- **Other Foundry concepts** (data protection, etc; my own take)
- **Maximize ALPHA/sovereignty / Data protection** (within performance/cost/complexity limitations)

The value of Foundry is

- **Foundry forces compliance with safe AI practices**. Foundry makes you think about the requirements for enterprise AI.
- **Palantir leadership (such as Alex Karp) are very verbal about some very real problems with AI in the enterprise**. They are the only ones exposing the real issues, the hype (while minimizing their own marketing hype).

Note that you could implement these same concepts without using Foundry. Foundry simply makes it easier to do.

<br>

ZAI is about AI. So AI for sure has something to do with it.

- **2.0a CLIENT/SERVER (saved ALPHA 40 years ago)**
- **2.0 ALPHA: The Alex Karp ALARM about ALPHA sovereignty (encoded version)**
- **1.3c (2.3) DECODED 3: Your most valueable core logic is "OUTSIDE THE MODEL SPECTRUM"**. You can do silly vibe coding demos, but real world apps, unique, with specialized biz processes, can not be created using pattern matching LLMs. **I THINK WHAT THIS MEANS IS IF YOU ARE CAREFUL ABOUT LEAKAGE, LLMs CAN NOT STEAL YOUR IDEAS**.
  - **### BECAUSE YOUR CORE IDEAS (ALPHA) ARE NOT PATTERNS, BUT HARD LOGIC ###**
- **2.2 DECODED 2: ALPHA leakage to external LLMs**
- **2.1 DECODED 1: An unrealistic solution: Foundry + Create your own internal model (with PAL)**. models are difficult to create.
- **2.2b DECODED 4: SOVEREIGNTY (HOW PAL STOPS THE STEAL)**. minimize LLM usage. maintain control.
  - **### DONT SHARE ALPHA WITH LLMS ###**
  - share only non-alpha stuff
  - carefully quanitify and control ALPHA

<!-- - **3.4 WHY and HOW THEY STEAL ALPHA: MINING DEMO D5** -->

<br>

#### **2.0a CLIENT/SERVER (saved ALPHA 40 years ago), BROWSER 30 years ago?**

OS app ALPHA was saved by client/server architecture.
app no long needed to be installed on device.  
ALPHA was not on device.

Browser becomes a mini-OS itself, client server.
API's safely restrict what data gets sent to external systems.

PAL does this with AI.
THIS IS JUST THE START OF THIS NEW PARADIGM.

<br>

#### **2.0 ALPHA: The Alex Karp ALARM (encoded version)**

<!-- **1.5 how PAL raised the alarm**. how PAL (Karp) alerts to the problem. -->

- BELOW: Alex Karp sounding the alarm about sovereignty in the enterprise (it took me a while to understand that I think he meant... I am still not 100% sure what he meant, but I am pretty sure about my take on "alpha".
- NOTE the sign behind Alex: Own your own outcomes, Own your models, Own your destiny. ??

<img src="/assets/alex222.png" alt="xxx" width="60%" style="border: 1px solid #999;">

<br>

#### **1.3c (2.3) DECODED 3: Your most valueable core logic is "OUTSIDE THE MODEL SPECTRUM"**

<img src="/assets/wuxi-22-3.png" alt="xxx" width="50%" style="border: 1px solid #999;">

- Note what I wrote above: **"Farming out your ALPHA is like hiring a taxi driver".**
- Thats not exactly right. **A frontier lab LLM has no intelligence; it will fake the required skills**. And possible cause a lot of trouble. Something like FSD without the human caretakers.
- LLMs are dumb binary computational algorithms (token generators) with absolutely no intelligence. **[LLMs ARE A HACK](/0-demo/)** that simulates intelligent conversations by generating response words based on input_word_sequence patterns.
- You will be competing against
  - (1) others like yourself and
  - (2) amateurs who are putting an AGI humanoid robot in the drivers seat and calling this their FSD product (Musk does this to some extent with his army of human operators who are 24/7 ready to save any Tesla that is in a situation that FSD was not programmed to handle).

**NOTE: from section "C2b-2) ExtAgent"**. Note that your procedural logic (extAgent) is

- far more intelligent and reliable than the simulated “thinking” of LLMs (that is based on pattern recognition and training) because
- the intelligence of a human was used to program a procedural spec in the extAgent.

**1.3b WHY and HOW THEY STEAL ALPHA: MINING DEMO D5**

- If you give **frontier models** ("frontier" = the most advanced major models) access to your business logic, then
  - they **will steal your company secrets**
  - **there is nothing legal you can do to stop them**
  - They will be doing do to you what they have already done to countless authors of original material used to "train" (program) their frontier models.

**NOTE HOWEVER THE STEAL MAY NOT BE AS GOOD:** If ALPHA is leaked to the LLM, then I would guess that something like the following would occur:

- At first the leader ALPHA would be stored as RAG.
- Perhaps then if the FLab (Frontier lab) wanted make the ALPHA part of its knowledge store (token generation), then the FLab would train ALPHA into the next model.
- However, this would not have the accurate of the biz processes as the original?

**Would the ALPHA be mined from plagiarized records, with a process something like in the mining demo D5?**

_Mining demo D5_<br><img src="/assets/wuxi-27.png" alt="xxx" width="54%" style="border: 1px solid #999;">

<br>

#### **2.2 DECODED 2: ALPHA leakage to external LLMs**

<!--
3.2 DECODED: Loosing alpha = From "your company" to "vibe coding"
Loosing alpha = From "your company" to "vibe coding" -->

- **[Sovereignty (ALPHA)](/3c.2_pal_2.0_sovereignty/)** = Who ultimately controls the data, models, application, workflows, decisions, and operational future?
- "ALPHA" = Alex Karp's term for your core biz logic.
- **The core logic for your business is not in the AI, but in your business processes**.
- **1 "getting sovereignty right" = no vibe coding**. The core procedural code (pipeline, ontology, analysis) is your secret... you may use external LLMs as assistants, but you never give them enough to steal your ideas.

<!-- - These demos compare external, internally controlled, and hybrid AI architectures to determine what the organization actually controls. The focus is not only data protection, but also model replaceability, application ownership, operational continuity, and control of decisions and outcomes. -->

_Your company (with the intro of AI and automation... and no ALPHA guardrails)_<br><img src="/assets/wuxi-22-1.png" alt="xxx" width="68%" style="border: 1px solid #999;">

_The result of ALPHA leakage is loss of ALPHA (1) Alpha moves to model (your product is now "vibe"code), (2) model is now the alpha product, (3) your customers migrate_<br><img src="/assets/wuxi-22-2.png" alt="xxx" width="50%" style="border: 1px solid #999;">

<!--
**EXAMPLE:** Farming out your ALPHA is like hiring a taxi driver who can take customer requests, and you call this your FSD productd. If you use an external frontier model for too much of your alpha, then the frontier lab will steal "your" product (you dont have product actually). This is vibe coding (at its worst).<br><img src="/assets/wuxi-18.png" alt="xxx" width="54%" style="border: 1px solid #999;">
-->

<br>

#### **2.1 DECODED 1: An unrealistic solution: Foundry + Create your own internal model (with PAL)**

You could compare this to 40 years ago actually working on a mainframe (not a PC), and access to workflows was tightly controlled. This is what Foundry basically offers. A controlled environment.

THe problem with this solution: But that locally trained and deployed model? Thats a lot of work. And for a lot requirements for AI in an enterprise it would be overkill. The solution: Using Foundry to maintain the sovereignty of your system, of your ALPHA.

_The ideal solution to ALPHA sovereignty._<br><img src="/assets/wuxi-32.png" alt="xxx" width="40%" style="border: 1px solid #999;">

<br>

#### **2.2b DECODED 4: SOVEREIGNTY (HOW PAL STOPS THE STEAL)**

with tthe external AI (thats different from MS; you can avoid or limit exposure)

PAL gives LLM independence like app run on different OS's inside browser.

- **Ontology defines actions, etc that never go to an LLM**. Thus they can not be used to reverse engineer your alpha.<br>_Ontology stays in your Foundry system: it does not leak out_<br><img src="/assets/wuxi-22-2b.png" alt="xxx" width="54%" style="border: 1px solid #999;">
- Security that closely controls what employees can do with AI.

<br>

#### **Keeping alpha using Foundry (example) #########################**

In D2

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

<br>

## **3 Foundry is a consultancy tool (NOT A MONOPOLY) (FUTURE CONSUMER VERSIONS?)**

- **Overly complicated demos** that dont stay laser-focused on the topics Alex talks about or on the main point of the demo.
- **UI, terminology, and docs that leave you in confusion**.
- **Limited geographical availability, cost, etc.**
- Foundry sometimes seems like a tool for a consulting business, not a consumer product, dev tool.

<!--
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

**My focus (for now) is on Palantir (Foundry)** because (*this list is WIP...*)
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

---

---

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

<br>

26.0917 (v1 26.0804)
