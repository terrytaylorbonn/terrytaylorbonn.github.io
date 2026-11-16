---
layout: page
title: pal_onto_rest_analogies
permalink: /pal_onto_rest_analogies/
---

<br>

_Main Foundry diagram (ZAI original diagram verified by FDE)_<br><img src="/assets/MAIN-03.png" alt="drones" width="73%" style="border: 1px solid #999;">

<br><br>
<br>

-----------------
-----------------
-----------------
-----------------

<br>


# **ME: attached is my diagram for Foundry ... the core of what it is.** 

I am trying to compare ontology operations with REST operations.

could you give me examples of ontology/REST pairs.

<br>

## GPT: Your diagram makes the comparison quite natural. Foundry Ontology operations are conceptually similar to REST API operations on business objects.

The main distinction is that Foundry provides a managed object model and controlled Actions, rather than requiring you to build all the REST endpoints yourself.

<br>

-----------------

<br>

## Ontology ↔ REST equivalents

Using your `693_Record` objects as an example:

| Operation          | Foundry Ontology                        | Conventional REST               |
| ------------------ | --------------------------------------- | ------------------------------- |
| Create object      | Create an object through an Action      | `POST /records`                 |
| Read object        | Query an Object Type                    | `GET /records/123`              |
| Read many objects  | Query an Object Set                     | `GET /records`                  |
| Filter objects     | Apply an Object Set filter              | `GET /records?status=FOUND`     |
| Update property    | Modify object through an Action         | `PATCH /records/123`            |
| Replace object     | Action that sets multiple properties    | `PUT /records/123`              |
| Delete object      | Delete object through an Action         | `DELETE /records/123`           |
| Link two objects   | Create or modify an object relationship | `POST /records/123/links`       |
| Run business logic | Execute a Foundry Action                | `POST /records/123/check`       |
| Trigger automation | Ontology event / automation trigger     | Webhook or event-driven handler |

These are conceptual equivalents, not necessarily the exact HTTP endpoints Foundry exposes.

<br>

-----------------

<br>

## Three concrete examples

### 1. Read an object

#### Foundry

Workshop Object Table reads a `693_Record` object.

Ontology → Object

#### REST

```
GET /records/123
```

Returns the record's properties.

### 2. Modify an object

#### Foundry

Workshop button submits `693_SaveCheckResult`, updating the object's `CheckResult` property.

#### REST

```
PATCH /records/123
```

```
{"CheckResult":"FOUND"}
```

### 3. Execute AI and save its result

#### Foundry

693_CheckAndSaveRecord` runs the AI check through AIPLF and saves the answer through an Action.

#### REST

```
POST /records/123/check
```

Server-side logic calls the LLM and updates the record.

<br>

-----------------

<br>

## One important architectural distinction

In conventional REST applications, the API usually handles both reads and writes.

In Foundry:

- Object Types / Object Sets provide the structured data and query model.
- Action Types provide controlled write operations and business logic.
- Workshop UI reads objects and submits Actions.
- AIP Logic / Functions can supply AI processing used by those workflows.

So the closest mapping for your diagram is:

#### Foundry

- Object Types + Object Sets + Actions

#### REST application

- Resources + GET/POST/PATCH/DELETE endpoints

#### Both expose controlled operations on persistent business data.

**One qualification for your diagram:** Foundry Actions are not simply REST endpoints. They are governed business operations with permissions, validation, and potentially more complex logic. But the REST analogy is very useful for explaining their practical role.



<br>

-----------------
-----------------
-----------------
-----------------

<br>


# **ME2: i am not trying to make them the same... i am just to explain**

the understood ontology with "analoguies" to REST endpoints (assume reader understands those). There is so much chatter about the "mystical" ontology... i am just trying to de-mystify it. the details are great to mention in anycase.

_(ME: question above is kind of sloppy on my part)_

<br>

## Exactly. Your objective is not to equate Ontology with REST, but to use familiar REST concepts to explain what Ontology actually does.

I think that's an effective teaching approach, especially for developers who already understand APIs.

For example:

| Foundry concept    | Familiar REST analogy                              |
| ------------------ | -------------------------------------------------- |
| Object Type        | Resource type, such as `/customers`                |
| Object instance    | Individual resource, such as `/customers/123`      |
| Property           | Resource field, such as `customer.name`            |
| Link Type          | Relationship between resources                     |
| Object Set         | Collection returned by a query                     |
| Action Type        | Controlled operation, analogous to an API endpoint |
| Action submission  | Calling an endpoint to perform an operation        |
| Action permissions | API authorization rules                            |

The central insight is that Ontology isn't some mysterious AI mechanism. It's a structured representation of business objects, their relationships, and the operations permitted on them.

The additional Foundry capabilities—governance, security, integration with datasets, AI, automation, and UI—are important, but they don't invalidate the analogy.

Your diagram also makes an important point: Ontology is only one part of Foundry's overall data-processing and application architecture. The data pipeline, AIP Logic, Functions, and UI have their own roles.

I'd use a sentence like this in your tutorial:

> If you're familiar with REST APIs, you already understand much of the basic idea behind Foundry Ontology: objects resemble API resources, properties resemble resource fields, links resemble relationships, and Actions resemble controlled API operations. The implementation and capabilities differ, but the analogy helps remove the mystery.

That gets your point across without suggesting the two technologies are identical.

<br>

-----------------
-----------------
-----------------
-----------------

<br>