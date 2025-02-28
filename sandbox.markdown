---
layout: page
title: AI API sandbox
permalink: /sandbox/
---
 
25.0225 [(Gdrive)](https://drive.google.com/drive/folders/1-Adawag9uA8_bq-hDF-nOuPYaRLz1eEO) 

# AI API Sandbox 

<br>

Work on the API sandbox ([video overview](https://www.youtube.com/watch?v=E9C912Omm7U)) started in Sep 2024, focusing on API/API-doc tech demos. I changed the name to "AI API sandbox" on 25.0203.
<!--  I never found a useful "AI drone getting started" (or even just a "drone GS"), and so I created the [AI drone wiki](https://github.com/terrytaylorbonn/auxdrone/wiki/AI-drones). For the same reason I created this AI API sandbox wiki. -->

<br>

![image](https://github.com/user-attachments/assets/187576ca-6ca9-41cc-9629-39a0db97581c)

<br>

[Sandbox concepts](https://github.com/terrytaylorbonn/auxdrone/wiki/4.0-AI-concepts) 

[AI concepts](AI-concepts)

[About the author](https://github.com/terrytaylorbonn/auxdrone/wiki/About-the-author)

<br>

### Deployments

The following 2 deployments are the main goal for mid 2025.

- [MAIN stack deployment](Main-deployment) ([Stack deployments](Deployments) lists all deployments active and past) includes
  - #2 Stack (FrontEnd (FE), Backend (BE), and database (DB))
  - #1 APIs / API-docs (code annotations)
  - #3 Deployment 
- [Doc deployments (MAIN)](Main-doc-deployments) include
  - #4.1 Sites + site docs
  - #4.2 API docs (json/yaml) / Postman
  - #4.3 AI generated doc content (from my lab note docx files on the Gdrive)
  - #4.4 AI chat (using local/remote models with RAG)
  - #4.5 RAG

<!-- [MAIN non-stack doc deployment](Concepts-(API-sandbox)-v2) -->

  ![image](https://github.com/user-attachments/assets/4f6c1990-ceae-483c-8534-bb9ce664ce22)


<!-- (AI dev tools) Copilot and ChatGPT have been indispensible for <!- in the 3 [dev phases](Concepts-(API-sandbox)-v2) of -> building these deployments. These binary-algorithm-based AI tools will never replace human intelligence (or replace programmers). But (as with high level languages, IDE's, code completion assistants, and search engines) they will 
- raise the level of abstraction and
- become a indispensible part of the dev toolset and product releases. -->

<br>

### Lab notes

The final 6 sections are basically my lab notes (*I hope to feed some version of these into an AI RAG to either generate docs or for chat*). 

![image](https://github.com/user-attachments/assets/d1b8bebd-ee54-4e4b-a3a0-b20f07a54d09)

- [2 Stacks/frameworks](2-Stacks-and-frameworks). The APIs/API-docs were created for the backend. Now need to be integrated into a complete stack. This part focuses on 
  - Base tech (HTML/JS/CSS).
  - Front ends (React, Vue, Angular, etc), what the end-user uses to access the backend.
  - Full stack (MERN).
  - Any other backend / server-side frameworks (Javascript, Python).
- [1 APIs/API-docs](1-APIs-and-API-docs) 
  - Creating APIs (REST, GraphQL) and API-docs on the local PC.
  - Tests with API tools (Swagger, Postman, etc).  
- [3 Deployment](3-Deployment). Deployment on remote hosts including
  - Dedicated hosting platforms (Netlify, Vercel, Render, etc).
  - AWS/GCP/Azure (also using Terraform).
  - CI/CD.
- [4 Doc/chat sites (WIP)](4-Doc-sites) (Non-MERN, non-code) 
- [5 API management](5-API-management) (AWS, Gravitee.io, Kong, Kubernetes Gateway, Apigee, Mulesoft, IBM).
- [6 Other](6-Other) (Git, other AWS, etc). 

