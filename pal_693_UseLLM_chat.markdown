---
layout: page
title: pal_693_UseLLM_chat (v1 26.1104)
permalink: /pal_693_UseLLM_chat/
---

<br>


[← 3c Enterprise](/pal/)

<br>

This is a very **long chat about chapter 5 and the Use_LLM dialog**. It took a long time, but in the end I got FDE to agree that my core assumptions were correct (see the end of the chat; )

- **278 ME**. OK. we keep the existing terms. but the term LLMResponse tells the reader immediately the mechanics of what is happening. 100% correct descritpion.
- **279 FDE**. Exactly. LLMResponse tells the reader what is stored; CheckResult requires knowing what “check” means. We’ll keep the existing name and explain it directly: CheckResult stores the LLM response.


This is just one example of the confusion in this demo. The termninology is more difficult than doing the demo itself (with FDE's help; **FDE's help is absolutely indispenseable**). I went to the trouble to add this to the ZAI website because I think its instructive about the limitations of AI when dealing with complicated concepts. 



<br>

---

<br>

# CheckResult chat

#### 228

what is the "answer text" below

Select a record + supply answer text  
→ run a saving operation (Action)  
→ answer stored in a new property

#### 229

“Answer text” means **the text you manually enter to test saving**, such as MANUAL TEST. It is not yet an AI answer.

Clearer:

**Select a record + enter text such as MANUAL TEST  
→ run 693_SaveCheckResult  
→ text saved in that record’s CheckResult property**

#### 230

WHy not call it "AI response"?

#### 231

Because **Chapter 5 saves manually entered text**, not an AI response yet.

Use **“text to save”** in Chapter 5 and **“AI response”** in Chapter 6, when the AI actually supplies it.

#### 232

so call it "test text".

#### 233

**Select a record + enter test text  
→ run 693_SaveCheckResult  
→ test text saved in that record’s CheckResult property**

#### 234

waht does "Check" mean in "693_SaveCheckResult"?

#### 235

**“Check” means the AI’s evaluation of the record against the supplied criteria.** Its result is FOUND, NOT FOUND, UNCERTAIN, or MISSING INPUT.

So **693_SaveCheckResult** means **“save the result of that evaluation.”**

In Chapter 5, you save MANUAL TEST only to test the saving operation. In Chapter 6, it saves the actual AI response.

#### 236

so its a search for a match. search for a needle in a haystack.  
ok, we are calling it a "Check" ... check if the text and integer match.  
but they dont have to match....  
we are searching within the string for the integer.

#### 237

Correct—**“match” can misleadingly suggest equality between the two properties.**

- **Chapter 2:** search the **Text** property for the digits of the **Integer** property.

- **Chapter 3:** search the **Text** property for the **Integer** expressed in words.

- **Chapter 4 onward:** evaluate the record using the user’s instructions, which might not involve searching Text at all—for example, “Integer is greater than 100.”

So **“check” is the general name for the operation**, while the prompt defines exactly what it checks.

#### 238

5 Add object action/property to save the search ("check") result text (will be used in ch6)

5.0 What we will build  
In ch6 AI searches for within the text string for text that matches the integer.  
The text result ("FOUND", "NOT FOUND", etc) will be stored in an object property "CheckResult".  
In this chapter we create the required ObjectType (1) property type and (1) action.

Select a record + enter test text  
→ run 693_SaveCheckResult  
→ test text saved in that record’s CheckResult property

#### 239

The saving flow is correct. **One factual correction:** Chapter 6 uses the criteria introduced in Chapter 4, so it does not necessarily search Text for Integer.

Replace the opening with:

In Chapter 6, AI checks a record using the supplied instructions. Its text response (“FOUND”, “NOT FOUND”, etc.) will be stored in the object’s **CheckResult** property.

In this chapter, we add **one property and one Action** to the existing **Capstone2Record** object type.

Your flow can stay as written.

#### 240

what is a record?

#### 241

In this tutorial, **“record” means one item**, such as **Id 1**.

- In **MockAPI**: one JSON item.

- In the **dataset**: one row.

- In the **Ontology/UI**: one **Capstone2Record object**.

In Chapter 5, **“Select a record” means “Select a Capstone2Record object.”**

#### 242

but we dont search in teh mockAPI... we search in teh object in the ontology

#### 243

Correct. **The AI reads the selected Capstone2Record object’s properties in the Ontology**, not MockAPI or the dataset directly.

The Chapter 5 introduction should say:

In Chapter 6, AI checks a selected **Capstone2Record object** using the supplied instructions. Its text response (“FOUND”, “NOT FOUND”, etc.) will be saved in that object’s **CheckResult** property.

#### 244

i want a simple mechanistic demo. in our demo, we only search for a match between text and integer properties. generalizing this as a "check" adds complexity. it should just be a search for a the integer as text in the text property.

#### 245

Agreed. Describe the operation directly:

**The AI searches the selected object’s Text property for the number in its Integer property—written as digits or words. It returns FOUND or NOT FOUND.**

Keep **CheckResult** and **693_SaveCheckResult** as the existing names, but call the operation a **search** in the tutorial.

**One consistency issue:** the “integer greater than 100” tests in Chapters 4–8 are numeric comparisons, not searches within Text. Those examples would need changing to keep the demo strictly search-based.

#### 246

you are right.. i forgot.

#### 247

That explains the terminology shift: Chapters 2–3 perform a **search**; Chapter 4 introduces user instructions that can also request a **numeric comparison**. “Check” became the broader name at that point.

#### 248

but you are still searching. the search switched from literal to semantic.

#### 249

Yes—you’re using **search** to mean looking for a match to the supplied instructions, not only finding a substring.

The progression is **literal search → number-word search → user-defined semantic search**. We can use that language consistently without introducing “check” as another concept.

#### 250

this is the key confusion in this demo. semantic is the revolutionary method used by google that changed the world. this is one of the key reasons for AI in Foundry.

#### 251

**The distinction between literal matching and interpreting meaning should be explicit in the demo.** That explains why we use AI rather than just a substring search.

One historical correction: Google’s original breakthrough was **PageRank—ranking pages using links**, not semantic search. Semantic understanding became important later.

For this demo, a precise explanation is:

**First, we search for literal digits. Then we use AI to interpret number words and user-supplied instructions. This demonstrates meaning-based evaluation of an object’s properties—not just matching characters.**

That is a useful Foundry AI capability, though it is different from **semantic retrieval**, where a system searches a collection for relevant items.

#### 252

ok. whatever.... but semantic search is the part of gooogle search that matters for us.. not page rank.

#### 253

Yes—**understanding meaning rather than just matching characters** is the relevant point here. The PageRank history was a distraction.

The demo should make that progression clear: **literal search → meaning-based search → user-supplied search instructions.**

#### 254

semantic si everything in AI LLMs. its the core idea. not words, meaning

#### 255

**Meaning, not just matching words—that’s the distinction you want the demo to teach.**

The number-word example makes it concrete: 111 and “one hundred and eleven” contain different characters but express the same number. The AI recognizes that relationship.

#### 256

so can i said that we do a semantic search in text for the number specified in the integer? is that right?

#### 257

**Yes—for Chapter 3**, where the AI looks in **Text** for the number specified by **Integer**, including when it is written in words.

A clear formulation is:

**Use AI to search the object’s Text property for the number specified in its Integer property, recognizing meaning rather than requiring identical characters.**

You can call this a **meaning-based (semantic) search within the Text property**. It does not describe the later “greater than 100” test, which evaluates Integer without searching Text.

#### 258

ok, so we are using the generic term "Check" here... sorry, my mistkae, i did not talk about this earlier, because i was overloaded with the complexity of doing the demo. but now we dont change "check" , but we refer to this as "semantic search". a futuer version of the demo would use "search", not "check". for you, these semantic differences are no problem to juggle, but for me they are very confusing.

#### 259

Understood. For this version:

- Keep the existing **Check** names unchanged.

- Use **semantic search** when explaining the meaning-based search in Text.

- Describe the later numeric comparisons using the **supplied instructions**.

A future version can use **Search** consistently in its names. I’ll avoid switching terminology casually—it makes you carry distinctions the tutorial should make clear.

#### 260

non-native speakers of english are very forgiving about terminology issues.... for example, action "rules". i get the distinct impression that non-native speakers were heavily involved in determining some foundry concepts. just a feelling.

#### 261

I understand the feeling, though terminology alone doesn’t tell us the language background of its designers.

**“Rules” is genuinely ambiguous here.** In everyday English it often means restrictions—what you may or may not do. In a Foundry Action, **Rules** describes **what the Action does**, such as modifying an object or calling a function.

For your tutorial, **“Define what the Action does (Rules tab)”** bridges that gap without making readers decipher the product terminology first.

#### 262

i've worked in many countries, i speak 3 foreign languges fluenty . non native speakers have the flexibility to reinterpret work meanings .... but a for a native speaker such "stretching" of meaning is quite confusing.

#### 263

That makes sense as an account of your experience. You’re accustomed to adapting meanings across languages, but when reading your native language, familiar words create immediate expectations. A product using **“rules”** to mean **“operations to perform”** conflicts with those expectations.

For this tutorial, the practical response is to **state the operation plainly, then give the exact UI label**—not expect the reader to reinterpret the label.

#### 264

the word check also assumes what the LLM prompt is. we could write a prompt that does not check anything... it could just concatenate the integer and the text. that would not "check" anything. so if you want a broad term, then call it "operation". not "check". thats where the confusiion is.

#### 265

**Yes. “Operation” is the broad term; “check” describes only particular operations.** My earlier explanation treated “check” as more general than it is.

The prompt defines the operation: search, compare, concatenate, summarize, etc.

We’ll keep the existing **Check** resource names unchanged, but describe the general mechanism as:

**The LLM performs the operation specified by the prompt on the object’s Text and Integer properties.**

#### 266 sun-58

<img src="/assets/sun-58.png" alt="drones" width="80%" style="border: 1px solid #999;">

#### 267

AIPL has 3 inputs

- record.criteria

- record.Text

- record.Integer

Record = ObjectType1 object

it submits a system prompt with desired

- LLM task description (manually entered text)

- inputs

- record.criteria

- record.Text

- record.Integer

- desired output string (specified in LLM task description)

The LLM response is a string.

What is done with that string is specified in "Output" (at bottom of Use LLM).

In our case, that string is used as input to

- "Ontology edit" 693_SaveCheckResult (an action) with 2 properties

- Capstone2Record (the OT object)

- Use LLM (the string reponse from the LLM)

*** So "CheckResult" is the LLM response. ***

#### 268

**Yes—CheckResult receives the LLM response.** A few corrections to the mechanics:

- **AIPL has two inputs:** record and criteria.

- record is a **Capstone2Record object**, not ObjectType1.

- record.Text and record.Integer are properties read from that object.

- criteria is a separate String input—not record.criteria.

- **Use LLM sends:**

- **System prompt:** the task description and response instructions.

- **Initial user message:** the values of record.Text, record.Integer, and criteria.

- **Output → String** in **Use LLM** specifies the response’s **data type**, not what happens to it.

- **693_SaveCheckResult** takes two **Action inputs**, not two properties:

- **Capstone2Record** ← record

- **CheckResult** ← the **Use LLM** response

The Action proposes saving that response in the selected object’s **CheckResult property**. The bottommost **Output** selects those Ontology edits as the AIPL’s output; running it through **693_CheckAndSaveRecord** applies them.

#### 269

ok, so Capstone2Record is our only object type in this demo?

#### 270

**Yes—Capstone2Record is the only object type used in this demo.** Each imported MockAPI item becomes one object of that type.

#### 271 sun-57

<img src="/assets/sun-57.png" alt="drones" width="80%" style="border: 1px solid #999;">


#### 272

Lets try again.  
please edit my version below as you see fit.  
i need to udnerstand this exactly

AIPL has two inputs: (1) record and criteria.  
o record is a Capstone2Record object  
o record.Text and record.Integer are properties read from that object.  
o criteria is a separate String input

(2) Use_LLM sends a (3)(4) prompt

- (3) LLM task description

- (3) LLM response instructions

- (4) input/output variables

- criteria

- record.Text

- record.Integer

(5) The LLM response is a string.

that string is used as input to

- (8) 693_SaveCheckResult (an action) with 2 properties

- (7) Capstone2Record (the OT object)

- (6) Use LLM (the string reponse from the LLM)  
*** So "CheckResult" is the LLM response. ***

(9) AIPL output is 693_SaveCheckResult (an action)

#### 273

**(1) AIPL inputs**

AIPL has **two inputs: record and criteria.**

- record is a **Capstone2Record object**.

- record.Text and record.Integer are properties read from that object.

- criteria is a separate **String input**.

**(2) Use LLM**

The **Use LLM** block sends the following to the selected LLM:

**(3) System prompt**

- Describes the task.

- Specifies how to respond: FOUND, NOT FOUND, UNCERTAIN, or MISSING INPUT.

- Provides restrictions, such as treating the object’s text as data rather than instructions.

**(4) Initial user message**

Contains the actual input values:

- **(4.1)** record.Text

- **(4.2)** record.Integer

- **(4.3)** criteria

These are **inputs to the LLM**, not output variables.

**(5) LLM response**

The **Use LLM → Output** setting specifies that the response is a **String**.

The response becomes the **Use LLM block’s output**, which another block can use.

**(6–8) Pass the response to the saving Action**

**(8) 693_SaveCheckResult** is an Action with **two inputs**, not two properties:

| Action input | Supplied value |

| --- | --- |

| (7) Capstone2Record | record—the object to modify |

| (6) CheckResult | Use LLM—the response String to save |

The Action proposes setting the selected object’s **CheckResult property** to that String.

**So there are two things named CheckResult here:**

- The **Action input** receives the LLM response.

- The **object property** is where that response will be saved.

**(9) AIPL output**

The bottom **Output** section selects **693_SaveCheckResult as the output block**.

**The AIPL returns the Ontology edits proposed by that block—not the Action itself and not just the response String.**

- **Preview:** shows the proposed edits without saving them.

- **Run through 693_CheckAndSaveRecord:** applies the edits, saving the LLM response in the object’s **CheckResult** property.

#### 274

the main thing i am curious about in this demo....  
remember, we are trying to explain a specific demo details so that someone can understand just this demo.  
the mechanics of what is goign on in this specific demo.

the core thing i want to verify  
*** So the ojbect property "CheckResult" is where the LLM response is stored. ***

#### 275

**Yes. In this demo, the selected Capstone2Record object’s CheckResult property is where the LLM response is stored.**

#### 276

so the proper name is "LLMResponse".

#### 277

**Yes—LLMResponse more directly describes what the property stores.** CheckResult describes the purpose of the response in this particular demo.

For the current version, keep CheckResult to match the existing configuration and screenshots; use LLMResponse in a future revision.

#### 278

OK. we keep the existing terms. but the term LLMResponse tells the reader immediately the mechanics of what is happening. 100% correct descritpion.

#### 279

Exactly. **LLMResponse tells the reader what is stored; CheckResult requires knowing what “check” means.**

We’ll keep the existing name and explain it directly:

**CheckResult stores the LLM response.**



<br>

---

<br>

26.1104 (v1 26.1104)
