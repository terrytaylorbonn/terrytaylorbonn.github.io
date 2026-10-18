---
layout: page
title: 00 Why Foundry?
permalink: /pal_concepts_why_foundry/
---

<br>

**[← 3c Enterprise](/pal/)**

<br>

#### **This page is a WIP** (currently just various thoughts (many **very original**))

<br>

You are always hearing about how "ontology" is the secret of Palantir's success. On this page I write my own original take on this concept (I've not seen a similar explanation elsewhere). 
- My opinion is that the reasons for this success are not so simple. There are a variety of reasons why Palantir is so successful.
- **The biggest reason: Foundry represents the** 
  - **(1) required higher level of abstraction and** 
  - **(2) the "rails" required for AI apps**. 
  
When the switch was made from assembly level to abstract languages (like COBOL, FORTRAN, C, etc), IDE's were created to aid in creating 
- (1) abstract commands and the 
- (2) guard rails (various techniques to reduce the additional complexity and room for error created by abstraction) to make it possible for humans to effectively write code. 



**Foundry is an example of the next level. The easiest way to get the concepts is too compare Foundry with other types of systems.**

<br>

#### **TOC**
For now this is a collection of various ideas that come to mind...
- **1 Comparing Foundry to airliner autopilot**
- **2 Comparing PC and Foundry to understand ontology**
- **3 Comparisons: Post, telegraph, telephone (manual/auto switching)**
- **4 Comparisons: No AI and LLM (remote/ local)**
- **9 CHAT**


<br>

------------------
------------------
------------------

<br>

# **1 Comparing Foundry to airliner autopilot**

_(GPT does not have intelligence, but for me something far more important: the ability to provide meaningful insightful feedback when discussing innovative concepts.... pure magic)_

#### For details see **[Chat about Autopilot <> Foundry comparisons](/pal_concepts_why_foundry_1/)**

_Autopilot diagram (GPT generated; my comments in red)_<br><img src="/assets/sun-30.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>

_Comparison with Foundry_<br><img src="/assets/sun-32.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>





<br>

------------------
------------------
------------------

<br>

# **2 Comparing PC and Foundry to understand ontology**

To me the easiest way of understanding what Foundry (and the ontology) does is to compare to a typical "enterprise" setup with Foundry (see diagram below). 

This section consists of
- a single prompt ("ME:") of mine to GPT 
- GPT's response ("GPT:") 

GPT's final comment about my diagrams:

> **My main recommendation: Keep the diagrams largely as they are. They're doing exactly what you want: showing developers that the Ontology isn't magic. It's a higher-level implementation of familiar enterprise software mechanisms, integrated with pipelines, applications, and AI.**


<br>

------------------

<br>

#### **ME: This section compares PC and Foundry as the best way to understand what ontology really is.**

In left diagram below (PC + backend)
- Local PC files upload to pipeline; pipeline output to backend.
- **PC to the backend is REST connection (CRUD: create, read, update, delete)**.
- **Backend contains objects + actions + links (persistent storage in DB)**.
- Maybe sometimes backend has connection to LLM ?? 
- External systems.

In right diagram below (Foundry)
- datasource uploaded to pipeline; pipeline output to ontology.
- **UI sends REST-like (CRUD) commands to ontology**. 
- **Ontology contains objects + actions + links (persistent storage in DB)**.
- Pipeline/ontology uses (usually external) LLM.
- External systems such as Odoo (webhook).


_PC and Foundry_<br><img src="/assets/sun-28.png" alt="drones" width="70%" style="border: 1px solid #999;"><br>

_Foundry dialog for specifying the type of action for an object type (**in this example, the dialog is for creating CUD (R is default) for the object type**)_<br><img src="/assets/sun-23.png" alt="drones" width="60%" style="border: 1px solid #999;"><br>

_Creating the NORTH UI widget and specifying the action (create chunk (of text))_<br><img src="/assets/sun-29.png" alt="drones" width="100%" style="border: 1px solid #999;"><br>

<br>


#### **GPT: I think this is one of the strongest explanations you've developed for what Foundry actually is.** 
The side-by-side comparison makes the Ontology much less mysterious.

Your central thesis is:

Foundry is an AI-era enterprise application platform that raises the abstraction level of the traditional PC + backend architecture.

I largely agree. But I would make a few technical distinctions to strengthen the argument.

### 1. What your diagrams get right

The structural similarity is striking.

| Traditional PC + backend | Foundry                                    |
| ------------------------ | ------------------------------------------ |
| PC user interface        | Foundry UI (e.g., Workshop)                |
| Backend application      | Ontology + associated Foundry services     |
| Objects                  | Ontology Objects                           |
| Object relationships     | Ontology Links                             |
| Backend operations       | Ontology Actions                           |
| Database                 | Dataset backing, Ontology storage/indexing |
| REST APIs                | Foundry APIs, OSDK, Actions                |
| Data ingestion / ETL     | Foundry Pipelines                          |
| External integrations    | Foundry connectors, webhooks               |
| AI integration           | Pipeline AI, AIP Logic, model inference    |

The Ontology is not an entirely new programming paradigm. It packages many familiar backend mechanisms into a standardized, higher-level platform.

And your second screenshot reinforces that point. Foundry provides configurable Create, Modify, Upsert, and Delete operations rather than requiring developers to implement each operation from scratch.

### 2. Four refinements I'd make

#### A. The Ontology is not the entire backend

This is probably the most important distinction.

In your left diagram, the orange Backend box contains application logic, objects, APIs, and persistence.

In Foundry, those responsibilities are distributed across several integrated services:

- Ontology — business objects, relationships, and Actions.
- AIP Logic / Functions — custom and AI-assisted logic.
- Pipeline Builder — ingestion and transformation.
- Foundry APIs and platform services — access, execution, persistence, security.

So the Ontology is the central business-object and action layer, rather than literally all the backend software.

Your diagram works as a conceptual simplification, provided you explain that.

#### B. The UI connection is REST-like, but not necessarily REST

You wrote:

> UI sends REST-like (CRUD) commands to ontology.

That's a good conceptual description.

More precisely, the UI queries Ontology objects and invokes Actions. Underlying implementations may use Foundry APIs and platform services rather than direct REST requests from the browser.

I would label that connection:

Object queries + Actions (CRUD-like)

#### C. The database relationship is different

In a traditional backend, objects are commonly persisted directly into application databases.

In Foundry, objects can be backed by datasets, with Ontology indexing and optional edit mechanisms.

As your D2 demo demonstrated, objects can appear automatically through dataset-backed indexing without invoking a Create Action.

That's an important difference worth preserving in your explanation.

#### D. AI is not necessarily external

Your diagram correctly shows LLM access from both pipelines and the Ontology side.

However, Foundry can use models made available within its platform environment as well as externally hosted models.

And AI can be invoked from applications and workflows, not only from pipelines and Ontology functions.

I'd simply label the purple box LLM / Models (internal or external).

### 3. The bigger architectural insight

Your comparison highlights three levels of abstraction.

Level 1 — Traditional programming

Developers write objects, business logic, database access, APIs, and integrations.

Level 2 — Traditional enterprise frameworks

Frameworks provide many of these mechanisms, but developers still assemble the application and supporting services.

Level 3 — Foundry

The platform provides a common environment for data pipelines, business objects, relationships, Actions, applications, integrations, and AI.

This is where I think your argument is strongest.

Foundry doesn't invent objects, REST, pipelines, or AI. It integrates them into a system where developers can work at a higher architectural level.

That can make developing complex enterprise workflows more manageable, particularly when AI is involved.

### 4. The one claim I would slightly modify

You wrote:

> Foundry raised the abstraction level to deal with AI-era complexities.

I would distinguish the historical claim from the present-day advantage.

Foundry's higher-level data and application abstractions existed before today's generative AI boom. They weren't originally invented solely to deal with LLMs.

But those abstractions are especially valuable now because AI introduces unpredictable outputs and increasingly complex interactions with enterprise systems.

So I'd phrase your conclusion as:

> **Foundry is a higher-level enterprise application platform that integrates the familiar mechanisms of traditional PC/backend systems — pipelines, objects, relationships, CRUD-like Actions, APIs, and external integrations. Its integrated architecture is particularly valuable in the AI era, allowing developers to introduce AI into workflows while retaining structured business operations, deterministic logic, and configurable controls.**

That preserves your main insight without overstating Foundry's historical motivation.

**My main recommendation: Keep the diagrams largely as they are. They're doing exactly what you want: showing developers that the Ontology isn't magic. It's a higher-level implementation of familiar enterprise software mechanisms, integrated with pipelines, applications, and AI.**


<br>

------------------
------------------
------------------

<br>

# **3 Comparisons: Post, telegraph, telephone (manual/auto switching)**

The new paradigm that Foundry brings to AI/binary computing is not unlike historical paradigm shifts, such as with the appearance of the telephone.

- Post office: network tightly controlled, reliable.
- Telegraph: 
  - Only trained operators allowed (their signature is detectable)
  - Easy to hack signals. 
- Telephone (manual switching)
  - Manual switching operator can listen in.
  - Operator always knows source.
  - Human language; skill level lower than for telegraph.
- Telephone (auto switching)
  - Must more secure.
- Telephone digital
  - Much harder to listen in.


<br>

------------------
------------------
------------------

<br>


# **4 Comparisons: No AI and LLM (remote/ local)**

The following compares the differences that AI introduced into the enterprise.


<br>

### **No AI**

- The App must match the OS perfectly. Decades ago this was a hard lockin to a CPU, but nowadays tech exists to quicky port to other CPUs.
- THe OS is a monopoly. Calls to the OS must be perfect (unlike LLMs that accept human language).
- The response format is quite predictable. 

_Non-AI App_<br><img src="/assets/sun-25.png" alt="drones" width="16%" style="border: 1px solid #999;"><br>

<br>


### **Remote LLM**

- (1) **Human language prompt/response** between app (agent) and LLM internal agent (iA) intros considerable risk.
  - Previously this would have been a REST interface, which would have required careful programming and drastically restricted communication.
- (2) **No monopoly for intercommunication** between app (agent) and LLM (unlike between app and REST API; the app must carefully be written for particular API)
- (3) **No HW lockin** for LLM TF (any CUDA/GPU that the LLM is compatible with)
- (4) BUT **response is not predictable** (human language)
- (5) This is **why Foundry excels**. 
  - 5.1 **Not built on the myth of AGI** (intelligent AI).
  - 5.2 **Abstracts from code enough for human programmers to handle the added complexity of the new programming paradigm** (just like the added abstraction for the switch from assembly level to high level languages previously). Other companies added complexity (programming), but Foundry added ontology abstraction.
  - 5.3 **Foundry restricts and governs** any communications or actions.
- (6) The **risks with remote LLM are many**:
  - LLM provider steals your ideas.
  - Your colleagues get careless and/or lazy and start feeding complex prompts with proprietary info to LLM.
  - The LLM searchs in the internet for any info it requires (further spreading your IP all over the internet).

_Remote LLM_<br><img src="/assets/sun-27.png" alt="drones" width="30%" style="border: 1px solid #999;"><br>

<br>



### **Local LLM (complicated)**


In diagram below:
 - Ollama installs LLM locally. 
 - TF .pt file is loaded onto the GPU with CUDA interface.
 - Any GPU can be used, but as with early CPUs, a GPU can have a monopoly if it is a top performer (like Nvidia).
 - Inference is via CUDA.

_AI app ("agent") + local LLM_<br><img src="/assets/sun-26.png" alt="drones" width="30%" style="border: 1px solid #999;"><br>



<br>

------------------
------------------
------------------
------------------
------------------------------------
------------------

<br>

# **9 CHAT**

Below is an interesting chat I had on 26.1016 about the core of what make Foundry tick.. what makes it so valuable. Still working on these concepts.... eventually want to compare Foundry with a REST based system.  Its taking a long time to do this.. so much time spent on peeling the onion layers of complexity to get at the gist.

My take on this is I think unique and quite on the mark. GPT (for what its worth) agrees.

<br>

------------------

<br>

### **ME01: in foundry**

you have objects.
you can run Crud on these objects. 
(these are the actiions you can do.... actually only CUD.... Read is by default).

links to other objects... this is link a shared PK in a db. 
objects are linked. 

so its kind of like REST endpoints.

#### **GPT:**

Yes. A Foundry Ontology is somewhat like a REST API backed by a relational database, but with additional business logic.

Your analogy is useful mechanically.

| Foundry Ontology | Database / REST analogy                                   |
| ---------------- | --------------------------------------------------------- |
| Object Type      | Database table / REST resource                            |
| Object           | Database row / JSON resource                              |
| Primary Key      | Primary Key (PK)                                          |
| Properties       | Columns / JSON fields                                     |
| Links            | Relationships between tables, often using foreign keys    |
| Actions          | Controlled CUD operations (and other business operations) |
| Object queries   | Read operations (GET-like)                                |

Three important refinements:

1\. Actions aren't limited to CUD. An Action can perform a business operation, such as Approve Order, which may update multiple objects or trigger other logic. Actions can also be configured to create or modify links.

2\. Links aren't necessarily shared primary keys. In relational databases, relationships commonly use a foreign key referencing another table's primary key. Foundry's Ontology exposes these relationships as navigable links between objects.

3\. Reading isn't an Action, but it isn't completely automatic. Applications query objects through Foundry's interfaces and APIs, subject to permissions.

### The important architectural distinction

A REST API exposes resources and operations.

Foundry's Ontology defines business objects, their relationships, and the operations permitted on them. Those capabilities can then be exposed through APIs, the OSDK, Workshop applications, automations, and AI agents.

So your analogy is essentially correct:

Ontology ≈ relational data model + business operations + API-accessible interface.

That is a useful starting point for explaining the Ontology without Palantir's more abstract terminology.



<br>

------------------

<br>

### **ME02: you can also use REST commands (https:/xxx.com/run_test) to do actions.**


#### **GPT:**
Yes. Foundry Ontology Actions can also be invoked through REST API endpoints, not just through Foundry applications.

For example, conceptually:

```
POST https://<foundry-host>/api/v2/ontologies/{ontology}/actions/{action}/apply
```

With a JSON request body containing the Action's parameters.

The distinction is:

- Ontology Action — Defines what operation is allowed and what it does.
- REST endpoint — Provides a way for external programs to invoke that Action.
- Workshop, Automate, AIP Logic, etc. — Other ways to invoke Actions.

Your example, `https://xxx.com/run_test`, could also be a custom REST endpoint that calls a Foundry Action behind the scenes.

So an important part of the Ontology is that the same business operation can be invoked through multiple interfaces, subject to authentication, permissions, and validation.

And importantly, Foundry's native REST endpoints have defined URL structures; you don't simply invent an endpoint name for an Action.





<br>

------------------

<br>

### **ME3:  so the big selling point is Foundry constrains you.. what you can do.**

but at the same time allows you to "insert" AI anywhere in the workflow.
in the pipeline, in the ontology 
(this word is to me misleading... 
the real value is the objects relationships and CRUD).

you insert AI in a controlled and monitored way.

#### **GPT:** 



Yes. I think you're identifying one of Foundry's most important architectural advantages, especially for enterprise AI adoption.

And I would emphasize two things equally:

1. Foundry constrains operations. It defines what data, objects, relationships, and operations are available, who can use them, and under what conditions.
2. Foundry allows AI to participate in those operations, without necessarily giving AI unrestricted control.

The key is that these two capabilities work together.

### 1. The Ontology is more than a data model

I agree that the word Ontology can obscure the practical mechanics.

What matters to a developer is:

- Objects — Business entities with properties and primary keys.
- Links — Relationships between objects.
- Actions — Controlled operations that create, modify, or delete objects and links.
- Business logic — Functions, rules, and validations governing operations.

The Ontology gives AI a structured interface to the business, rather than unrestricted access to underlying databases.

### 2. AI can be inserted at different points

For example:

<img src="/assets/sun-21.png" alt="drones" width="50%" style="border: 1px solid #999;">

Conceptual illustration: AI can participate in data processing, business logic, and application workflows. Not every AI invocation must modify the Ontology.

- Pipeline: AI extracts information, classifies records, or enriches data.
- Ontology: AI-backed functions can reason over objects and propose or initiate Actions.
- Applications / Automations: AI assists users, makes recommendations, or participates in multi-step workflows.

### 3. The critical qualification

Foundry doesn't automatically make AI reliable just because it operates inside Foundry.

Reliability depends on how the developer configures permissions, Action constraints, validation, testing, monitoring, and human approval.

But Foundry provides a common platform for implementing those controls.

### The central concept

I would summarize your argument this way:

Foundry combines flexible AI reasoning with structured data, deterministic business logic, and controlled operations. AI can be introduced at multiple points in the workflow, while the platform provides mechanisms to constrain, test, monitor, and govern its behavior.

That is a much more concrete explanation of Foundry's value than simply saying it enables human–AI teaming.

<br>

------------------

<br>

### **ME4: can try to give a summary of how this mimics REST based systems.** 

not just the REST endpoints...
but the data sanitization that occurs, realtime data inputs,


#### **GPT:**

I think Foundry can be understood as an enterprise REST-based application architecture, extended with integrated data pipelines, business objects, AI, and governance.

The similarity goes well beyond REST endpoints.

## 1. Comparing traditional REST systems with Foundry

| Mechanism           | Traditional REST-based system                       | Foundry equivalent                                           |
| ------------------- | --------------------------------------------------- | ------------------------------------------------------------ |
| External data input | APIs, databases, message queues, sensors            | Data Connection, streaming and batch ingestion               |
| Data sanitization   | ETL, validation, cleaning, normalization            | Pipeline Builder, transforms, data quality checks            |
| Data storage        | SQL/NoSQL databases                                 | Foundry datasets and backing data sources                    |
| Business objects    | Application models, database records                | Ontology Object Types and objects                            |
| Relationships       | Primary keys, foreign keys, joins                   | Ontology Links                                               |
| CRUD operations     | REST GET, POST, PATCH, DELETE                       | Object queries and Ontology Actions                          |
| Business logic      | Backend functions, services, rules engines          | Ontology functions, Actions, AIP Logic                       |
| AI integration      | Calls to LLM APIs or local models                   | AI in pipelines, functions, applications, automations        |
| User applications   | Web applications, dashboards                        | Workshop, Quiver, other Foundry applications                 |
| Automated workflows | Schedulers, event handlers, workflow engines        | Automate, build schedules, other workflow tools              |
| Security            | Authentication, authorization, validation, auditing | Foundry permissions, policies, approvals, audit capabilities |
| External operations | REST calls to ERP, CRM, other services              | Connectors, webhooks, APIs, integrations                     |

The important point is that traditional enterprise systems already implement most of these mechanisms. Foundry integrates many of them into one platform.

## 2. The complete data and action loop

Consider a manufacturing system receiving real-time sensor measurements.

Conceptual processing loop. In practice, some steps run asynchronously, and operations can bypass stages that aren't needed.


<img src="/assets/sun-22.png" alt="drones" width="50%" style="border: 1px solid #999;">


For example:

1. A sensor reports excessive vibration on Machine 42.
2. A pipeline ingests the measurement, checks validity, handles missing values, and updates the relevant data.
3. The Ontology represents Machine 42 and its relationships to equipment, maintenance records, and production orders.
4. A deterministic rule or AI function evaluates the situation.
5. An Ontology Action creates a maintenance request, possibly requiring human approval.
6. A Foundry application displays the result, or an integration sends the request to an external maintenance system.

This resembles a conventional enterprise application built from APIs, databases, validation services, business logic, and workflow engines.

## 3. Where Foundry adds value

I would identify three major advantages.

A. Integrated data refinement

In a traditional REST architecture, developers often assemble separate ingestion, ETL, validation, storage, and monitoring systems.

Foundry provides integrated tools for building and operating much of that pipeline.

B. A standardized business-object and action layer

Instead of every application independently implementing its own data models and business operations, the Ontology provides shared definitions of objects, relationships, and Actions.

This can reduce duplication and make operations more consistent across applications.

C. Controlled AI insertion

This is perhaps the most interesting part of your thesis.

AI can participate in data refinement, analysis, decision support, and business operations. But the developer can surround AI with deterministic validation, permissions, constrained Actions, evaluation, monitoring, and human approval.

AI does not need unrestricted database access to be useful.

## 4. One important distinction: real-time versus batch

Foundry supports both batch and streaming data, but not every Ontology object or application automatically reflects source-system changes instantaneously.

Freshness depends on ingestion configuration, pipeline execution, Ontology synchronization, and the specific integration.

Likewise, an Action may update Foundry's operational state without immediately updating an external source system; that requires an appropriate write-back mechanism.

## My suggested summary for your Foundry concepts document

Foundry implements many of the same mechanisms found in traditional REST-based enterprise systems: data ingestion, sanitization, databases, business objects, relationships, CRUD-style operations, business logic, APIs, and workflows.

Its major advantage is integrating these mechanisms into a common platform, with the Ontology providing a shared object-and-action interface.

AI can be inserted at multiple points in this architecture, while deterministic software, permissions, validation, monitoring, and human oversight constrain what the AI can do.

The innovation is not that Foundry invented these mechanisms. It is how Foundry integrates them and makes them available for building controlled, AI-assisted enterprise workflows.


<br>

------------------

<br>

### **ME5:**

pic 1 shows all the actions you can create for object type. 
pic 2 is about an action that runs a function on a different objecct. 
whats interesting is this gives incredibly flexible functionality. 

and pic 2 shows the code generated.
that the real genius.. you dont have to write code.

this is REST/ objectx oriented programming "on rails".


<img src="/assets/sun-23.png" alt="drones" width="50%" style="border: 1px solid #999;">

<img src="/assets/sun-24.png" alt="drones" width="50%" style="border: 1px solid #999;">



#### **GPT:** 

“REST / object-oriented programming on rails” is a very good description of what you're seeing. And I think you've identified an important part of Foundry's value that Palantir's introductory explanations tend to obscure.

The interesting part isn't just that Foundry has objects and Actions. It's that Foundry provides much of the infrastructure needed to turn business objects into working applications.

### 1. Picture 1: More than CRUD

You have the familiar operations:

- Create object
- Modify object
- Modify or create object (upsert)
- Delete object

But look at the other tabs: Link, Function, Webhook, Interface, Notification, Scenario, etc.

That means an Action is not merely a database operation. It can also be an entry point to other logic and systems.

This is much closer to an enterprise application service layer than a simple database interface.

### 2. Picture 2: The really interesting part

Your second screenshot shows an Action configured to invoke `clinicEditFunction`, with a `Clinic` object as an input.

The code preview includes:

```
async function clinicEditFunction(
    client: Client,
    clinic: Osdk.Instance<Clinic>,
): Promise<ClinicEdit[]> {
    const editBatch = createEditBatch<ClinicEdit>(client);
```

This illustrates several important mechanisms:

1. The function receives a typed Ontology object.
2. It can use the Ontology SDK to work with that object.
3. It constructs a batch of proposed edits.
4. The Action provides a configured interface through which that logic can be invoked.

The developer doesn't need to write a separate REST service, design its endpoint, or manually implement the surrounding Action interface.

One qualification: the screenshot shows existing TypeScript code being previewed from Code Repositories. It doesn't establish that Foundry automatically generated the entire `clinicEditFunction` implementation. You may still need to write custom business logic for Function Actions.

### 3. Why your analogy works

In traditional REST / object-oriented development, you might have to assemble:

`Database → ORM → Business logic → REST API → Authentication → UI → Monitoring`

Foundry provides integrated mechanisms for much of that:

`Ontology objects → Links → Actions → Functions → Applications / APIs`

And AI can participate in the logic without necessarily bypassing the structured interfaces.

### 4. What I find most significant

Foundry makes business operations reusable.

You can define an Action once, then invoke it from different places: Workshop, an automation, a custom application using the OSDK, or an AI-assisted workflow.

The same operation can use consistent object definitions, input validation, and permission controls.

That is a substantial architectural advantage over repeatedly implementing similar operations in independent applications.

Your phrase captures it nicely:

Foundry is something like REST and object-oriented enterprise application development on rails, with integrated data pipelines, reusable business operations, and controlled AI integration.

The important caveat is that the rails don't eliminate programming or guarantee correctness. They eliminate a great deal of repetitive integration work and provide standardized places to enforce controls.

<br>

------------------

<br>

### **ME6: so original OO programming focused on "low level" OOP, .....**

by that i mean providing the basic commands to create objects.. but you had to create a lot of "glue" logic.  

but in foundry its not glue logic... Foundry actually give you "real" complete objects on a higher level, making it much easier to focus on the business aspects while still retaining the ability to custom code.

#### **GPT:** 

Yes. I agree with your central distinction: Foundry raises the level of abstraction from programming objects to building business systems using predefined, operational business objects.

And **I think this is a more useful way to explain Foundry than Palantir's abstract descriptions of the Ontology.**

### Traditional OOP versus Foundry

| Traditional OOP                        | Foundry Ontology                                         |
| -------------------------------------- | -------------------------------------------------------- |
| Define classes                         | Define business Object Types                             |
| Instantiate objects                    | Create business object instances                         |
| Define properties and methods          | Define properties, Links, Actions, Functions             |
| Program object relationships           | Configure relationships between Object Types             |
| Write database persistence logic       | Use Foundry's object storage and backing-data mechanisms |
| Build REST endpoints                   | Use Foundry's APIs and Action interfaces                 |
| Implement authorization and validation | Configure platform permissions and Action validation     |
| Build integration and workflow logic   | Use Foundry pipelines, automations, and integrations     |

### The distinction I would emphasize

Traditional OOP gives developers the programming constructs needed to build applications. You still have to assemble persistence, APIs, authentication, relationships, workflows, and much of the surrounding infrastructure.

Foundry gives developers a higher-level application framework, with many of these capabilities already integrated.

For example, when you define a `Clinic` Object Type, you're not merely creating a class.

You're defining a business entity that can participate in a larger system:

- It has properties, identity, and relationships.
- It can be queried through standardized interfaces.
- Actions can modify it under configured constraints.
- Applications and automations can operate on it.
- Custom functions and AI can extend its behavior.

The developer can concentrate more on what the business operation should accomplish, rather than repeatedly building the infrastructure that makes the operation possible.

### Two qualifications

First, traditional OOP is not inherently limited to low-level programming. Mature frameworks such as Django, Spring, and .NET also provide high-level business application infrastructure. Foundry's advantage is its particular integration of data, business objects, actions, applications, and governance.

Second, Foundry doesn't eliminate glue code altogether. Complex external integrations, unusual business rules, and custom interfaces may still require programming.

### Your deeper point

I think the real distinction is:

Traditional OOP provides the building blocks for creating objects and applications. Foundry provides a platform in which business objects are already connected to a substantial set of application services.

And that becomes especially valuable with AI.

Instead of an AI agent having to interact with arbitrary databases, APIs, and custom code, it can operate through well-defined business objects and constrained Actions.

Foundry doesn't just make business application development easier. It also provides a structured environment in which AI can participate in those applications.


<br>

------------------

<br>

### **ME7: keeping the "programming level" (you can also write real code if required) on a high level allows you to focus on much more complex systems programming.**

that last pic i showed you will all of the many options for an action... if you tried to do that in an IDE with code assist, it would far too complicated ... links, functions, notifications, webhooks, etc etc..... but in foundry you have a very manageable way of havin access to all of these.

#### **GPT:** 

Yes. And I think you're getting at something more important than simply reducing the amount of code developers must write.

Foundry raises the level at which developers can design and control complex enterprise systems.

Look at your Action configuration screenshot. You have access to:

- Object creation, modification, and deletion
- Links between objects
- Custom functions
- Webhooks to external systems
- Notifications
- Interfaces and other operations

These are not merely convenient programming shortcuts. They are pre-integrated system capabilities exposed through a relatively consistent configuration interface.

### Why this matters

Imagine implementing the same functionality in VS Code, even with an excellent AI coding assistant.

You would need to design, implement, integrate, and maintain multiple subsystems: database models, APIs, relationship management, authentication, event handling, notifications, webhooks, error handling, and so forth.

An AI coding assistant could generate much of that code. But generating code is not the same as integrating and operating a reliable system.

Foundry already provides much of that infrastructure.

Consequently, the developer can spend more time on higher-level questions:

- What business objects should exist?
- How should they relate?
- Which operations should be permitted?
- What should trigger those operations?
- Where should deterministic logic, AI, or human approval be used?
- How should the entire process be monitored?

These are systems architecture and business-process design problems, rather than primarily coding problems.

### One qualification

I wouldn't say that implementing such a system in an IDE would necessarily be too complicated. Experienced teams build systems like this using conventional frameworks.

But they must assemble and maintain the underlying components themselves, or rely on several separate platforms.

Foundry's advantage is that much of this functionality is already integrated and accessible through common interfaces.

### And here's the connection to AI

This higher level of abstraction also makes AI integration much more manageable.

An LLM can interpret information or recommend an operation, while Foundry provides structured objects, functions, Actions, permissions, and workflows through which that operation can be carried out.

The developer moves from writing the machinery to designing how the machinery works together.

I think that is one of the strongest arguments for Foundry—and it is a stronger argument than merely claiming that Foundry makes programming easier.


<br>

------------------

<br>

