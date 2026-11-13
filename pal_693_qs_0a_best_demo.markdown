---
layout: page
title: What this QS offers beginners
permalink: /pal_693_qs_0a_best_demo/
---

<br>



[↑ 3c Foundry QS](/pal_693_qs/) / [→ Short overview of all chapters (TOC)](/pal_693_qs_0a2_config_dias/)   


_26.1113 08:00 (converted from docx source file to markdown+PNGs by ChatGPT)_

<br>

<a id="section-why-this-is-the-best-qs-for-foundry"></a>


**TOC**

- **[You follow accurate step-by-step directions that keep you from getting stuck](#section-you-follow-accurate-step-by-step-directions-that-keep-you-from-getting-stuck)**
- **[You build a Foundry app from scratch that covers the core basics](#section-you-build-a-foundry-app-from-scratch-that-covers-the-core-basics)**
- **[All the screenshots in this demo are from the author's PC](#section-all-the-screenshots-in-this-demo-are-from-the-author-s-pc)**
- **[This demo will be updated constantly (AI converts docx source files to the required wepage files)](#section-this-demo-will-be-updated-constantly-ai-converts-docx-source-files-to-the-required-wepage-files)**
- **[There will be follow-on tutorials and Youtube videos](#section-there-will-be-follow-on-tutorials-and-youtube-videos)**

<br>

<a id="section-you-follow-accurate-step-by-step-directions-that-keep-you-from-getting-stuck"></a>

### **You follow accurate step-by-step directions that keep you from getting stuck**

Foundry is an application that takes a new approach to a new paradigm: Using "ontology" with AI as an add-on within the enterprise. You cant simply spend an hour on a demo and master the basic concepts. It takes training. And you need master those concepts before trying to tackle real world problems.

This QS will make that process as fast as possible. This QS is laser-focused on 2 things:

- **Detailed step by step directions.** Never getting stuck. You need to master how to navigate the Foundry dialogs, master the terminology, etc etc.
- **Using FDE** (Foundry's built-in AI assistant).  You will always be using FDE if you work with Foundry (or any other similar product) in the future.

<br>

<a id="section-you-build-a-foundry-app-from-scratch-that-covers-the-core-basics"></a>

### **You build a Foundry app from scratch that covers the core basics**

This QS shows how to build a "small" Foundry app that is laser-focused on 2 things:

- **Bare bones demos that help you understand exactly what you are doing (the mechanics) and why**.  The QS uses simple **Text** and **Integer** values so you can focus on Foundry’s mechanics rather than a business scenario.
- Demonstrating the **core configurations/workflows** (with minimal text and diagrams). The next chapter "**A short overview of all chapters**" provides overview diagrams for everything you will do in this QS.

The entire QS is based on the following basic data flow chain.

<img src="/assets/qs/0a/0a_01.png" alt="Foundry QS diagram" width="65%" style="border: 1px solid #999;">

**The main chain**

- **MockAPI:** holds the external records that Foundry will fetch.
- **Data connection:** gives the Python script approved access to MockAPI.
- **Python import script:** fetches the records and writes them into a dataset.
- **Dataset:** stores the imported rows inside Foundry.
- **Object type:** defines how those rows become **Capstone2Record objects**, with properties such as **Text** and **Integer**.
- **AIPL (AIP Logic workflow):** sends the selected object’s property values and your instructions to an LLM.
- **AIPLF (published function):** makes that AIPL workflow available for the UI or an Action to call.
- **UI (built in Workshop):** displays the objects and lets you select one, enter instructions, and request an LLM response.

**What we add afterward**

- **Actions:** commit the LLM response to the object’s **CheckResult** property.
- **Automations:** run the AI operation when objects are added or their monitored properties change.
- **Build schedule:** runs the Python import every two minutes.
- **Governance controls:** demonstrate who can see objects and submit Actions, and inspect execution history.

**By the end, you will have built and traced the complete path from an external record to a saved LLM response.**

<br>

<a id="section-all-the-screenshots-in-this-demo-are-from-the-author-s-pc"></a>

### **All the screenshots in this demo are from the author's PC**

I (the author of this QS) worked alone with FDE (Foundry's built-in AI) to build this QS. Without human assistance. At the time I started this QS, I had just a few months experience with Foundry. I had done several Foundry demos (you can find my versions of those demos on the website), and the more I understood what I was doing, the more I wanted to create Foundry docs that showed how to learn Foundry from a different perspective.

I documented all of my steps and the many chats with FDE along the way. I created the original QS content in MS.Word which  allowed me to focus on configuring Foundry and getting the details down "on paper" (not on creating webpages). I then used GPT to convert the docx to markdown and PNG image files for the webpages.

<br>

<a id="section-this-demo-will-be-updated-constantly-ai-converts-docx-source-files-to-the-required-wepage-files"></a>

### **This demo will be updated constantly (AI converts docx source files to the required wepage files)**

The source for this QS is a single MS.Word docx file.  Working in MS.Word makes it possible to focus on content and quickly update the QS. The docx is converted to webpages (markdown + pics) by ChatGPT using a single (large) prompt. The docx and the resulting webpages have very simple formatting in order to make the conversion reliable. This makes constant QS updates and maintenance possible.

<br>

<a id="section-there-will-be-follow-on-tutorials-and-youtube-videos"></a>

### **There will be follow-on tutorials and Youtube videos**

This QS is the first of a series of tutorials I plan to write over the next several months.

There will other demos and possibly Youtube video overviews of these demos. The videos will

- Have a limited lifetime. When the video is outdated, it will be redone.
- Focus on high level explanations of what webpage content.
