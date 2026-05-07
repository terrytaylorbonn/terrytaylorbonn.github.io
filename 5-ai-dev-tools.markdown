---
layout: page
title: "(5) AI dev tools"
permalink: /AI-dev-tools/
description: Last edit 26.0501
---

<br>

The AI IDEs (Cursor, VSCode (+LLM)) are critical for AI app dev. This page will decribe primarily IDEs (and dev tools in general).

TOC
- 1 IDE overviews, intros, videos
- 2 IDE problems (errors I encountered, etc) (dealing with HL is risky)

<br>


## 1 IDE overviews, intros, videos 


- [(5.1) Cursor](/Cursor-overview/)
- [(5.2) GPT/Codex](/GPT-Codex-overview/)
- [(5.3) Claude](/Claude-dev-tools/) (not an IDE, but incluuded anyway)

<!-- <img src="/assets/ai_project_diagram_5.png" alt="drones" width="45%">  -->

<br> 

## 2 IDE Problems 26.0507 (taken from #606)



Add here: Claude source code leak.

<br> 

### demo #2: Security (Cur), email rabbit hole (Cur), data loss (Cla)

<br> 


#### ***See the demo details on page [(6) AI projects](/AI-projects/)***.

<br> 

#### **2.1 Security incident**
This little incident shows perfectly why you can't trust LLMs for secure apps. I am almost certain I made no error (I did not exposed secrets); in any case, Cursor pasted contents from .env to the chat window. those contents included an app password.  The following is a screenshot of the offending Cursor response:

<img src="/assets/cursor_secret_error.png" alt="drones" width="45%"> 


I remembered that when Cursor first posted. But I did not ask Cursor about it. I simply assumed the chat window was secure, otherwise Cursor would not have dont this. But I did notice what Cursor did.

Perhaps Cursor was not programmed to realize that the password in all letters and with spaces was a password (not misspelled text). password format was "abcd efgh ijkl mnop". Usually its pasted into the env as "abcdefghijklmnop", but I did not delete the spaces (works anyway). 

Later Cursor informed me that I (NOT CURSOR) pasted live secrets. 

 
<img src="/assets/cursor_secret_err_note.png" alt="drones" width="75%"> 


**Cursor could not tell me exactly what was compromised. ONLY the above statement.**

In docx #606 
- search for "first tell me more about the security note; (1) what exactly did i do, (2) how risky is it, and (3) how to fix"
- see ch "S7d CURSOR env var changes / test" for details about the fix. This required at least 4 hours to fix (including retesting and documentation; the fix worked the first time: Cursor told me it would only require 15 mins to fix).
- see ch S7c for details about the error and confusion. at the end of that chapter i wrote ">>> PS: never access the .env file. ask me to copy paste if required." CURSOR: "Understood. I will not read or access .env going forward. If I need any value, I’ll ask you to paste only what’s needed (redacted when possible)."

<br> 

#### 2.2 Claude unannounced restart (with no history)

what happened
•	Claude simply restarted (it apparently does that daily). 
•	After the restart the chat history was gone
•	THis happened right before i was going to generate the new text. the only thing that saved me was that I recorded the chats in this doc.
i am on free plan with api credits. maybe that is why. but i should have been warned and it should have kept the chat history.
for details see
"S6b CLAUDE CRASHED.. has NO MEMORY OF PAST !!! try to recover"
"S6c CLAUDE CHAOS... CURSOR FIXED"

<br> 


#### 2.3 cant send gmail emails from render 26.0505
Cursor did not warn about this at the start. cant do Resend either because cant verify google on Resend (use ziptieai.com ??? setup email? too much trouble .. at least for now)  in S7e. 
AI tools are reactive, not proactive. token generators, not intelligent. this is an example of that.  



<br> 


26.0507 (v1 26.0428)
