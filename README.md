[日本語](README_JP.md)

# CV

This is the resume and skill sheet of [tetratensor](https://github.com/tetratensor) (Kazuma Mori).

## Basic Information

| key      | value                                         |
| :------- | :-------------------------------------------- |
| Name     | Kazuma Mori                                   |
| Location | Tsushima, Nikasaki, Japan                     |
| Mail     | momotaro-tech@proton.me                       |
| GitHub   | [tetratensor](https://github.com/tetratensor) |

# Strengths

- Understand product problem domains and select technologies aligned with business context
- Build maintainable and extensible systems through testing and sound design
- Rapidly learn unfamiliar technologies
- Team building using Agile (Scrum)
- Full-stack web development across frontend, backend, and infrastructure
- Cross‑platform mobile development with React Native (Expo)
- Clear, scalable asynchronous communication and process design
- Applied AI: LLM apps, RAG, AI agents, tool use/function calling, structured outputs
- Real‑time and multimodal UX: streaming UI, TTS/STT, low‑latency pipelines, edge inference

I have led many greenfield and large-scale replacement projects to solve issues in existing systems.

I propose and execute optimal system architectures based on current constraints and goals.

I highly value psychological safety for teams/organizations, aiming for consistently respectful and flat communication.

Recently, I call myself a Product Engineer: I prioritize the product first and choose the technologies and approaches that best serve it.

# Areas I'm less strong in

- Web design (I can write CSS, but I am not a UI/UX designer)
- Development where the background/objectives are unclear and the work is just “do as told”

# Engineering Principles I Emphasize

Below is what I focus on across frontend, backend, and cloud (infrastructure).

### As a Frontend Engineer

My recent stack centers around Next.js, React, and React Native (Expo).

- Real‑time/multimodal UI for AI: WebRTC, SSE/streaming responses, audio capture/playback, transcript rendering
- Safety/guardrails surfaced in UX (disclaimers, PII redaction prompts, feedback loops)
- Separate pure, props-only components from those with side effects
- Invest mainly in two forms of testing:
  - Storybook-driven tests
  - E2E tests (essential to ensure frontend behavior)
- Use snapshot and unit tests for functions where appropriate

With Storybook, I strive to represent all component behaviors there, and deploy static Storybook outputs for easy review. Recently, I have been using Chromatic:

https://github.com/tetratensor/commew

This significantly improves UI review efficiency. Though it takes time, it consistently streamlines UI communication.

I design for portability to non-Node.js runtimes such as Cloudflare Workers or Vercel Edge Runtime.

With React Server Components (via Next.js), I carefully balance Server Components and Client Components.
I also design for streaming-first UIs for AI inference (progressive rendering, optimistic UI).

### As a Backend Engineer

Recently, due to my focus on Generative AI, I primarily write Python. I prefer starting small with lightweight frameworks like FastAPI. I usually adopt a layered architecture with DDD-inspired design to keep code testable and evolvable.

- Always test the application/use-case layer
- For database tests, I prefer using a real test database rather than heavy mocking (while keeping the code mockable). Verifying actual data persistence is a critical factor for backend APIs.
- Because DB-backed tests can be slow, I also apply performance improvements for test execution.

The largest scale I have handled in performance work:

- ~20 million members
- Throughput goal: 5,000 rps
- Target: <150 ms response for read APIs under the above load

I mostly run on cloud/serverless. In performance testing, I verify that scaling out improves performance accordingly.

AI backend focus:

- RAG pipelines (chunking, embeddings, hybrid/semantic search, reranking)
- Tool use/function calling, JSON/JSON Schema structured outputs
- Agent patterns (routing, planning, state persistence)
- Async streaming (Server‑Sent Events), WebRTC relays, low‑latency audio TTS/STT

Reference personal project using Generative AI (Python + FastAPI):

https://github.com/tetratensor/nekochans

### As a Cloud Engineer

While not a dedicated SRE, I have designed AWS networking from scratch for a ~1M-user service replacement project.

For startups, I often prefer high-performance serverless platforms like Cloudflare Workers or simple container platforms like Fly.io to minimize infra maintenance and focus on application development. For databases, I favor DBaaS such as PlanetScale; features like branching and safe migrations significantly improve DX.
For AI workloads, I also leverage serverless GPU (Modal) and managed inference (Cloud Run) with streaming endpoints.

For larger-scale systems, AWS often remains the best option in terms of cost and available knowledge.

I manage AWS resources with Terraform to capture who changed what/when and to codify environment setup.

I follow AWS best practices such as the [AWS Well-Architected Framework](https://wa.aws.amazon.com/wellarchitected/2020-07-02T19-33-23/index.ja.html) with strong attention to security.

## Skill Levels

Self-assessed proficiency scale:

- `S`: Understand current best practices and can implement them
- `A`: Solid, production-level development experience
- `B`: Some production experience, limited depth
- `C`: Studied/used in learning contexts

### Languages

| Language   | Level | Notes                                                    |
| ---------- | ----- | -------------------------------------------------------- |
| HTML       | A     | Comfortable from prior frontend work                     |
| CSS        | A     | Comfortable from prior frontend work                     |
| JavaScript | S     | Experience in browser and Node.js; up-to-date with specs |
| TypeScript | S     | Experience in browser and Node.js; up-to-date with specs |
| Python     | S     | LLM apps, RAG, agents, tool calling; FastAPI streaming   |
| Go         | A     | Built REST and gRPC apps without heavy frameworks        |
| PHP        | A     | First career language; not used recently                 |
| Ruby       | A     | Used around 2.2–2.3 era; not used recently               |
| Java       | B     | Minor maintenance with Java 8 + Spring                   |
| Scala      | C     | Light maintenance with Play 2.4; wrote Gatling tests     |

My longest experience is with JavaScript/TypeScript, and I keep up with the latest standards.

PHP: used for ~5 years early in my career; knowledge is dated (around 7.3).

Recently, I most often write TypeScript and Go for frontend with React/Next.js and infra code for AWS Lambda. Ruby proficiency is decent but outdated. Java/Scala experience is limited.

I am frequently involved in development for LLM-backed applications. Python is mainly used on the backend.

Please see my GitHub for a practical view of my skills:

https://github.com/tetratensor

### Frameworks (Backend)

| Name             | Level | Notes                                               |
| ---------------- | ----- | --------------------------------------------------- |
| Laravel          | A     | Introduced from scratch; last PHP project used this |
| Express          | S     | Frequently used from 2015 for Node.js on server     |
| NestJS           | A     | Frequently used from 2022 for Node.js on server     |
| Ruby on Rails    | B     | Built from scratch for Web APIs (v4 at the time)    |
| Django           | A     | Built from scratch                                  |
| FastAPI          | S     | LLM backends, SSE streaming, async APIs             |
| Spring Framework | B     | Light maintenance exposure                          |
| Play Framework   | B     | Light maintenance exposure (2.4)                    |
| Hono             | A     | Used in personal projects                           |

### AI/ML SDKs & Services

| Name                   | Level | Notes                                 |
| ---------------------- | ----- | ------------------------------------- |
| OpenAI API/SDK         | S     | Chat, tools, Realtime API, embeddings |
| Anthropic (Claude) API | A     | Tools, reasoning, safety              |
| Google Gemini API      | A     | Multimodal Live, images/audio/video   |
| Modal (serverless GPU) | A     | Batch/streaming inference jobs        |
| Milvus (Zilliz Cloud)  | B     | Vector search for RAG                 |
| Pinecone               | B     | Evaluating serverless                 |

Current thinking: rather than full-stack monolith frameworks, I often favor thin frameworks like [Hono](https://hono.dev/) with Cloudflare Workers to build small, loosely coupled systems, because:

- Next.js shifts more application logic into the frontend (LLM apps aside)
- Cloud services and libraries have reduced backend code amounts

Of course, monoliths can be the faster path in many cases; it depends.

With Go, I typically avoid frameworks and build small container apps with the standard library.

For TypeScript, I consider Edge runtimes like Cloudflare Workers first, and even on Node.js I aim for designs portable to non-Node runtimes.

### Frameworks/Libraries (Frontend)

| Name         | Level | Notes                                                     |
| ------------ | ----- | --------------------------------------------------------- |
| jQuery       | A     | Used early in career; no longer used recently             |
| React        | S     | Using since ~2015; track best practices                   |
| React Native | A     | Cross‑platform apps with Expo; native modules when needed |
| Vue.js       | B     | Built SPA incl. Vuex; less proficient than React          |
| Next.js      | S     | Used for multiple greenfield apps                         |
| Nuxt.js      | A     | Used for multiple greenfield apps                         |
| Angular      | C     | Studied v1 era; not used recently                         |

Comfortable with npm-based frontend tooling. Recently, my main is Next.js (React). I used Redux often before but now also use SWR and React Context, and like simple state libs such as [valtio](https://github.com/pmndrs/valtio).

Newer frameworks like Svelte/Solid/Qwik are interesting, but I currently prefer React for its ecosystem maturity, stability, and wealth of information. Many innovations (e.g., Server Components) emerge from the React ecosystem.

### RDB

| Name      | Level | Notes                                       |
| --------- | ----- | ------------------------------------------- |
| MySQL     | A     | Heavily used from 5.1 to 5.7                |
| Redis     | A     | Built Redis Sentinel-based failover on-prem |
| memcached | A     | Used as cache in early career               |
| MongoDB   | B     | Used once for internal system               |
| DynamoDB  | B     | Used for auth in a serverless API           |

I handled introduction-to-tuning for all the above. MongoDB usage was limited and not under high load. I care deeply about MySQL schema and performance. Recently I prefer DBaaS like PlanetScale for cost and DX (branching, safe migrations).

### Vector DB

| Name                  | Level | Notes                            |
| --------------------- | ----- | -------------------------------- |
| Milvus (Zilliz Cloud) | B     | First Vector DB used in LLM work |
| Pinecone              | B     | Planning to try serverless       |

I have production experience only with Milvus (Zilliz Cloud). Provisioning was handled by another member; I have not yet introduced a Vector DB from scratch myself.

### DevOps (including IaC)

| Name           | Level | Notes                                  |
| -------------- | ----- | -------------------------------------- |
| Terraform      | S     | Frequently used for AWS infrastructure |
| GitHub Actions | S     | Often used for CI/CD                   |

AI ops focus: dataset/versioning, prompt/version control, cost/latency monitoring, evaluation harnesses (offline/online), safety checks.

With public clouds like AWS, I commonly manage infra using Terraform. I have used Kubernetes for microservices efforts. For CI/CD, I currently prefer GitHub Actions to increase deploy frequency and shorten time-to-value.

### Public Cloud (AWS)

AWS services I have used:

| Service               | Level | Notes                                                               |
| --------------------- | ----- | ------------------------------------------------------------------- |
| EC2                   | S     | Used as web servers                                                 |
| ECS                   | A     | Recently using Fargate more                                         |
| ELB, ALB              | S     | Primarily ALB now                                                   |
| AWS Lambda            | S     | Frequently used for REST and infra tasks                            |
| S3                    | A     | Used for various purposes                                           |
| CloudFront            | A     | Used as CDN                                                         |
| Route 53              | A     | Used for DNS and domains                                            |
| API Gateway           | A     | Built many APIs with Lambda                                         |
| RDS                   | A     | Built Multi-AZ-aware setups                                         |
| DynamoDB              | A     | Used as DB for Lambda-based APIs                                    |
| ElastiCache           | A     | Used Redis for Laravel app caching                                  |
| Cognito               | A     | Built auth with User Pools for internal and external users          |
| CloudFormation        | B     | Prefer Terraform for faster feature support                         |
| X-Ray                 | B     | Used for serverless monitoring/analysis                             |
| CodeDeploy            | A     | Built blue/green deploys for EC2                                    |
| CodeBuild             | A     | Used for ECR pushes and more                                        |
| Kinesis Data Firehose | A     | Shipped logs to S3                                                  |
| Athena                | A     | Queried logs via SQL                                                |
| EKS                   | C     | Used for microservices platform (not complex setup)                 |
| Rekognition           | A     | Used to detect inappropriate images; also used in personal projects |

I omit basics like VPC/CloudWatch. I have built entire infrastructures from scratch (incl. web apps) with AWS since around 2015.

# Technologies I'm Currently Interested In

## LLM

I actively use search AIs like Perplexity and AI-assisted IDEs like Cursor to improve productivity. I have a strong interest in LLM-backed app development; I began taking on such projects around July 2022.

I’m particularly interested in real-time APIs like OpenAI Realtime API and Gemini 2.0 Multimodal Live API. The latter enables pseudo video-calls with AI and feels very promising.

https://github.com/tetratensor/realtime-api-web-console

## Next.js

I first used Next.js around 2017, and became especially interested with ISR (Incremental Static Regeneration). ISR can significantly improve response times for many services I work on.

Since Next.js 13, App Router with React Server Components is stable, making it even more important.

When Vercel is not an option, infra and ops costs rise, so I consider simpler frameworks like [Remix](https://remix.run).

## Edge Computing

With [Next.js Middleware](https://nextjs.org/docs/middleware) and [Remix](https://remix.run/), edge computing enables faster frontends and scenarios like A/B testing. I see code portability to non-Node runtimes (e.g., Vercel Edge Runtime) as increasingly necessary. Thus I watch lightweight frameworks like [Hono](https://hono.dev/).

## Cloudflare

Cloudflare now offers not only CDN/DDoS protection but also high-performance serverless (Workers) and a production DB (D1). I expect usage as an AWS alternative to increase.

An article I watch closely:

https://blog.cloudflare.com/python-workers

Python is officially supported on Cloudflare Workers, further improving synergy with AI apps. With WASI gaining traction as a post-container trend, Cloudflare’s support there is also interesting.

## React Server Components

With Next.js 13.4, App Router became stable and React Server Components are available:

https://nextjs.org/blog/next-13-4

In practice, shipped JS sizes are much smaller, opening opportunities to drastically improve page speed even for dynamic content. I am actively incorporating RSC into app design.

## Supabase

An affordable auth foundation with PostgreSQL and a Tokyo region, making it practical latency-wise.

Rapid auth plus PostgreSQL makes it my first-choice auth platform in many cases.

# Selected Work Experience

## Algomatic, [Niji Voice](https://nijivoice.com/) Text-to-Speech Service (Oct 2024 – Apr 2025)

### Overview

Development of Niji Voice, a TTS service that converts input text into speech.
Keywords: TTS, multimodal audio, low‑latency streaming, WebRTC/SSE, Realtime AI, Stripe metering

### Tech Stack

- Next.js 15
- Vercel
- [HeroUI](https://www.heroui.com/)
- ESLint
- Supabase (auth)
- Hono (application layer on backend)
- Python 3.13
- uv (Python package manager)
- FastAPI 0.115
- Custom-built TTS
- Cloud Run (API server)
- Stripe (payments)

### Team Size

1 (me) + 2 developers + 1 business owner + 1 creator + 1 designer = 6 total

### My Role

- Frontend architecture selection
- β version overall architecture selection
- Auth platform selection
- Frontend development
- Backend development

I also promoted the product and interacted directly with users on the official Discord to drive improvements.

### Outcomes

- Launched a login-free β version solo within two weeks; achieved rapid PMF (about 10 million characters generated in the first week)
- After two talented engineers joined, we collaboratively:
  - Monetized Niji Voice by adding login and payments
  - Released the Niji Voice API
- With a strong team and focused scope, we shipped high-quality features quickly.

## Video Translation App using LLMs (Mar 2024 – Sep 2024)

### Overview

Greenfield app that uploads a video, generates translated subtitles from the audio, and outputs a subtitled video.
Keywords: STT/ASR, translation, multimodal, batching, serverless GPU, RAG (domain prompts)

### Tech Stack

- Next.js 14, Vercel, [NextUI](https://nextui.org/)
- Biome, Prettier
- Python 3.12, Rye (pkg manager), FastAPI 0.112
- OpenAI API, Anthropic API, Gemini API
- Cloud Run (API server), Google Cloud Workflows
- [Modal](https://modal.com/) (serverless GPU)
- Stripe (payments)

### Team Size

1 (me) + 3 developers + 1 product manager

### My Role

- Frontend architecture selection
- Frontend and backend development
- Developer documentation
- Project facilitation (Scrum Master-like)

### Outcomes

- Productionized an existing LLM transcription/translation prototype into a user-facing app
- Balanced speed and quality: Next.js (App Router) + Vercel + NextUI on frontend; Cloud Run on backend
- Used Anthropic (Claude 3.5 Sonnet) and Gemini in addition to OpenAI as needed
- Results:
  - Delivered β in 3 weeks on a part-time schedule (2 days/week); released final on time in Sep
  - Designed the UI using a component library when no designer was assigned (later replaced by official design)
  - Clarified prioritization and visibility to ship within limited time

## Owned Media + AI Agent for an AI-focused Company (Jan 2024 – May 2024)

### Overview

Marketing site plus an AI agent that answers inquiries about contract development and can contact sales.
Keywords: AI agent, tools/function calling, lead qualification, retrieval, i18n

### Tech Stack

- Next.js 14, Vercel, ESLint, Prettier
- Python 3.12, Rye, FastAPI 0.100
- OpenAI API, Fly.io (API server), Milvus (Zilliz Cloud)

### Team Size

1 (me) + 1 developer + 1 external designer + 1 PM

### My Role

- Overall architecture/design/development
- Developer documentation
- Project facilitation

### Outcomes

- Designed with OpenAI tools to make the AI agent easily extensible; currently emails sales when a conversation is deemed a qualified lead
- Implemented frontend i18n

## Support Chatbot for a Major Credit Card Company (Dec 2023 – Jan 2024)

### Overview

Chatbot answering FAQs about credit cards.
Keywords: RAG, embeddings, PII redaction, content moderation, latency SLAs, Milvus

### Tech Stack

- Python 3.12, Rye, FastAPI 0.100
- OpenAI API
- AWS (ECS Fargate)
- Milvus (Zilliz Cloud)
- LINE Messaging API

### Team Size

1 (me) + 5 developers + 2 PMs

### My Role

- Backend infra design/build
- Backend architecture selection/design/development

### Outcomes

- Reduced communication overhead by documenting thoroughly to avoid repeated questions across many stakeholders
- Set up CI/CD early to increase deploy frequency and shorten feedback loops

## InnovativeAI, [Resume-No](https://resume-no.ai/en), AI Recruiting / Hiring Platform (May 2023 – Dec 2024)

### Overview

Worked on integrating or enhancing Resume-No(レジュメノー), an AI recruitment tool aimed at automating resume sourcing, screening, and candidate management for HR teams.

### Tech Stack

- React 18, Next.js 13, Jest, ESLint, Prettier, Vercel
- Upstash, Auth.js
- Python 3.11, Poetry, FastAPI 0.100, OpenAI API
- Milvus (Zilliz Cloud), PlanetScale, Fly.io (API server)

### Team Size

1 (me) + 2 developers + 1 designer + 1 PM

### My Role

- Auth platform selection/design/implementation
- Backend architecture selection/design/development
- Developer documentation
- Project facilitation

### Outcomes

- Operated under tight budgets/deadlines typical for startups; focused on essential value
- All members were part-time; emphasized async communication and visibility (Slack, GitHub Issues, GitHub Projects)
- Constantly reviewed scope and proposed changes based on customer value
- Balanced speed and quality by leveraging AI for routine coding and learning new tech (Python, FastAPI, App Router) quickly

## Large-Scale Auth Platform Replacement (Aug 2022 – Mar 2023)

### Overview

A client operating many services had slowed development due to poor maintainability and outdated dependencies with no tests. Goal: restore maintainability and speed.

### Tech Stack

- React 18, Next.js 13, Storybook, Jest, ESLint, Prettier, Vercel
- Authlete, Upstash

### Team Size

3 total: 1 (me) + 1 developer + 1 designer

### My Role

- Project manager
- Architecture selection/design/development
- Developer documentation
- Developer support and code reviews

### Outcomes

- SSR-heavy due to real-time account data and auth; used Edge Middleware and Edge API Routes to reduce latency
- Achieved ~80 PageSpeed Insights score consistently via Upstash + Edge BFF
- Clarified auth domain knowledge to improve maintainability significantly
- Improved deploy frequency from ~2/week to ~7/week, enabling faster experimentation (A/B tests) and growth

## Medical Media Frontend Replacement with Next.js (2021 – 2022)

### Overview

Major redesign to improve response speed and establish a robust frontend foundation that could be reused across services.

### Tech Stack

- React 18, Next.js 12, Storybook, Jest, ESLint, Prettier, Vercel

### Team Size

4 total: PM (1), me (1), developer (1), designer (1)

### My Role

- Architecture selection/design/development
- Documentation for other service teams
- Developer support and code reviews

### Outcomes

- Selected Next.js for ISR benefits to media services
- Chose Vercel to maximize Next.js advantages
- Collaborated with designers to package shared UI (via GitHub Packages) for reuse
- Results:
  - Large response-time improvements (PageSpeed +40% range)
  - Established frontend foundation and development rules

## Email Sending API (2021)

### Overview

Unified email sending across multiple apps to avoid duplicated logic and scattered templates.

### Tech Stack

- Go, AWS Lambda, [SendGrid Web API v3](https://sendgrid.kke.co.jp/docs/API_Reference/Web_API_v3/index.html)
- Serverless Framework, GitHub Actions, Terraform

### Team Size

2 total: PM (1) + me (1)

### Outcomes

- Centralized email logic; improved deliverability vs. SES
- Easier bounce management with SendGrid
- Performed IP warmup and configured custom-domain sending
- Later migrated to App Runner when Lambda concurrency limits approached

## Postal Code to Address Lookup API (2021)

### Overview

Provided a shared API for address lookup (postal code to address) used across many services.

### Tech Stack

- Go, AWS Lambda, [KENALL](https://kenall.jp/docs/)
- Serverless Framework, GitHub Actions

### Team Size

2 total: PM (1) + me (1)

### Role & Outcomes

- Implemented Go + AWS Lambda to call KENALL API and return address data
- Unified disparate implementations and eliminated address master maintenance
- Considered migrating from Lambda to App Runner due to potential concurrency/cold start concerns

## Mass Messaging Improvements for a [Crowdfunding Service](https://fundinno.com/) (2021)

### Overview

Fixed timeouts when project creators sent messages to all supporters for large projects.

### Tech Stack

- Ruby on Rails (5), Amazon Aurora (MySQL 5.7), SendGrid

### Team Size

2 total: PM (1) + me (1)

### Role & Outcomes

- Introduced related tables to avoid heavy changes to legacy schema
- Used SendGrid’s batch sends (1,000 addresses) and Delayed Job for async processing
- Results: handled >20,000 recipients reliably; removed user wait times

## Auth Platform Migration for [Crowdfunding Service](https://fundinno.com/) (2020 – 2021)

### Overview

Replace a devise-based auth with an IDaaS approach, adding future flexibility for social logins and non-password auth.

### Tech Stack

- Go (Cognito User Pool custom Lambdas and APIs operating on user data)
- React (16), OpenAPI v3, Terraform

### Team Size

Initially 2 (lead + me), later +2 developers and +1 advisor

### My Role & Outcomes

- Designed/implemented zero-downtime data migration from old to new auth
- Designed session persistence
- Rebuilt registration/login UIs in React (from ERB)
- Chose Cognito User Pool (budget vs. Auth0), overcame rate limits and migration complexities via careful PoCs
- Outcomes:
  - Avoided long downtime and opportunity loss
  - Enabled low-effort addition of new social logins (when OIDC-compliant)

## Comment Retrieval API for [Crowdfunding Service](https://fundinno.com/) (2020)

### Overview

Solve delayed comment rendering for projects with massive numbers of comments by introducing an API and SPA.

### Tech Stack

- React (16), Ruby on Rails (5), Amazon Aurora (MySQL 5.7), OpenAPI v3

### Team Size

2 total: PM (1) + me (1), plus ~3 reviewers

### Role & Outcomes

- Designed OpenAPI schema, implemented Rails API with paging, SPA-ified comment view with infinite scroll
- Tuned queries to avoid slow queries; optimized render performance with React DevTools
- Results: eliminated delays and allowed viewing of all comments (previously capped)

## Notification Service on EKS (2020)

### Overview

Microservice that sends notifications for various user actions (e.g., comments and replies).

### Tech Stack

- AWS (EKS), Go, gRPC, Terraform

### Team Size

2 total: me + 1 developer

### Role & Outcomes

- Chose overall architecture; developed gRPC services in Go
- Established a Go-on-EKS foundation; shared knowledge in a PHP-centric org; documented Go patterns and differences vs. PHP
- Project later ran at smaller scale due to budget; wished for more time on EKS/CI/CD polish

## AWS Infra Foundation for Ad Tool (2019)

### Overview

Built new cloud environment for an ad operations tool.

### Tech Stack

- AWS (various), Terraform

### Team Size

2 total: me + CTO

### Role & Outcomes

- Designed overall architecture; built multi-region infra with Terraform
- Result: infra moved from unmanaged to codified; enabled easy international expansion

## Migration from EC2 to AWS Fargate (2018)

### Overview

Containerized existing EC2 apps and migrated to Fargate.

### Tech Stack

- AWS Fargate, AWS CodeBuild, ECR, Docker Hub, Terraform, CircleCI, Gatling

### Team Size

2 total: me + 1 developer

### Role & Outcomes

- Led direction; built log analysis pipeline; authored Dockerfiles per app
- Outcomes: reduced environment drift, faster deployments, optimized costs; aligned some apps with the Twelve-Factor App

## Full Replacement of a Nursing Community Site (2017)

### Overview

Full replacement including DB for a community site for nurses.

### Tech Stack

- PHP 7.2 (Laravel 5.5), TypeScript, Next.js (React), Nuxt.js (Vue.js)
- AWS (various), JIRA, Confluence, GitHub, CircleCI

### Team Size

Lead (me) + 5 developers + 1 PM

### My Role

- Determined overall system architecture
- Scrum Master to improve team efficiency
- Built AWS infra (Terraform, deploy pipelines, log analysis)
- Built OIDC-compliant auth with AWS Lambda + TypeScript
- Built Web APIs in PHP (Laravel)
- Built frontends in Next.js and Nuxt.js
- Built auth with Cognito User Pool for admin site

### Outcomes

- Moved from monolith to loosely coupled microservices
- Introduced Atlassian, ZenHub, AWS to modernize dev process and boost efficiency
- Created a self-sufficient dev team; improved both velocity and quality
- Smooth data migration and project execution vs. prior replacement effort

## Full Replacement of Major EC Site Member Platform (2016)

### Overview

Replaced an aging member platform including DB redesign for a site with ~20M members.

### Tech Stack

- Java 8 (API server), Spring 4
- Ruby on Rails 4 (admin)
- MySQL 5.6, Couchbase 3 (backend cache), Redis (messaging)
- AWS (staging and performance environments)
- Vagrant, Ansible, Docker
- JIRA, Confluence, Bitbucket, Jenkins

### Team Size

Lead (me), technical advisor (1), developers (7), directors (2), PM (1)

### My Role

- Development lead
- Planned data migration from old to new DB; automated migration tests
- Decided overall system architecture
- Designed new member API and admin requirements/design
- Managed server configuration with Ansible; implemented APIs

### Outcomes

- Achieved major performance improvements to handle rapid member growth

- Built performance testing on AWS to easily test middleware

Key lessons:

- In replacements, data migration is the hardest part
- Small, elite teams beat large headcount for speed
- Early, thorough technical validation is crucial

## Internal Authorization Platform (2015)

### Overview

Internal OAuth 2.0-based authorization platform to manage internal APIs (a simplified Amazon API Gateway-like system).

### Tech Stack

- Node.js (Express), Redis (API Gateway cache)
- PHP 5.4 (FuelPHP) for admin site managing client IDs, etc.
- MySQL 5.5, Jenkins, JMeter

### Team Size

PM + 6 engineers (including me)

### My Role & Outcomes

- Requirements to development for the admin site
- Implemented Node.js APIs, unit tests, and performance tests
- Unified bespoke auth flows into standards-based OAuth; clarified API access management; enabled CI to reduce post-release defects
- Implemented OAuth Provider by mapping the OpenID Connect spec into code, reinforcing the importance of reading primary sources (RFCs, official docs)

## Internal Common Deploy Tool Replacement (2014)

### Overview

Replaced an in-house deploy tool (no tests, no reproducible env) with standard tools.

### Tech Stack

- Jenkins, Capistrano (Ruby)

### Team Size

2 total: me + PM

### Outcomes

- Replaced “tribal-knowledge” deploy tool, making maintenance accessible to anyone

## Social Login for Major EC Site (2013)

### Overview

Implemented social login for a major EC site (Facebook and Google for initial release).

### Tech Stack

- PHP 5.3, Zend Framework, Facebook API, Google API

### Team Size

3 total: me (lead) + 1 developer + 1 director

### Outcomes

- +500,000 registered users in the first month post-release
- Researched and implemented secure OAuth client flows; learned OAuth/OIDC fundamentals

## Personal Info API Performance Improvements (2013)

### Overview

Improved performance of an API that returns user personal information.

### Tech Stack

- PHP 5.3, Laravel, MySQL 5.1/5.5

### Team Size

1 (me), with 1 senior reviewer

### Outcomes

- Achieved major improvements via query design under legacy schema constraints
- Reduced average response from ~400 ms to ~150 ms; API became production-viable

## Personal Info API Development (2013)

### Overview

Separated user data access into a Web API.

### Tech Stack

- PHP 5.3, Laravel, MySQL 5.1

### Team Size

3 engineers (incl. me) + 1 director

### My Role & Outcomes

- Implemented API and unit tests; internal design (external by senior engineer)
- Added tests to previously untested classes; improved automation; learned change-friendly design and Git workflows via code reviews

# Personal Projects

## [AI Cat API](https://github.com/tetratensor/nekochans)

### Overview

AI-powered cat personality chatbot service backend API. A Japanese service that allows users to chat with AI that has cat personalities.

### Tech Stack

- Python 3.12+ (FastAPI, asyncio, aiomysql)
- OpenAI API, LangSmith, PlanetScale MySQL
- Docker, Docker Compose, uv
- Uvicorn, httpx, tiktoken

### Outcomes

- Full-stack development of AI chatbot backend
- Implemented SSE (Server-Sent Events) for real-time streaming responses
- Built comprehensive testing suite with parallel execution
- Integrated multiple AI providers and database systems
- Achieved 90% validation accuracy on emotion detection model
- Implemented Docker containerization for easy deployment

## [Amazon Wishlist Point Getter](https://github.com/tetratensor/Amazon-Wishlist-Point-Visualization)

### Overview

Chrome extension that automatically displays Amazon.co.jp reward points on wishlist pages, eliminating the need to visit individual product pages.

### Tech Stack

- TypeScript 5.7+, Webpack 5.99+
- Chrome Extension Manifest V3
- pnpm package manager, ES2022 target

### Outcomes

- Developed Chrome extension with 1.5k+ users on Chrome Web Store
- Implemented real-time DOM manipulation and point extraction
- Built efficient CSS selector system for various Amazon product types
- Optimized performance with IntersectionObserver and MutationObserver
- Created automated deployment pipeline with version synchronization

## [Chatbot Sentiment Analyzer](https://github.com/tetratensor/chatbot-sentiment-analyzer)

### Overview

LSTM-based neural network for sentiment analysis in chatbot conversations, with CLI interface and pre-trained model for immediate inference.

### Tech Stack

- Python 3.8+, TensorFlow/Keras
- LSTM neural network, Embedding layers
- NumPy, pandas for data processing
- Jupyter notebooks for model development

### Outcomes

- Developed LSTM model achieving 88.8% training accuracy, 76.1% test accuracy
- Implemented real-time sentiment prediction CLI
- Built comprehensive preprocessing pipeline for text data
- Created interactive testing interface with historical statistics
- Optimized model for production deployment

## [Jane Street Electronic Trading Competition](https://github.com/tetratensor/street-algo-trader)

### Overview

Algorithmic trading strategies for electronic exchange simulation, including market-making, arbitrage, and momentum strategies.

### Tech Stack

- Python 2.7+/3.x, NumPy
- Socket programming, JSON protocol
- Real-time market data processing
- Statistical analysis and signal generation

### Outcomes

- Implemented multiple trading strategies: pennying, micro-MACD, ETF arbitrage
- Built real-time market data processing system
- Developed risk management and position tracking
- Created automated trading client with WebSocket communication
- Achieved competitive performance in algorithmic trading simulation

## [Next.js Cloudflare Voice AI](https://github.com/tetratensor/Next.js-Cloudflare-Voice-AI-Assistant)

### Overview

Real-time voice AI assistant built with Next.js and deployed on Cloudflare Workers, featuring voice activity detection, speech-to-text, and text-to-speech.

### Tech Stack

- Next.js 15, React 19, TypeScript
- Cloudflare Workers, Durable Objects
- WebSocket communication, Voice Activity Detection
- Cloudflare AI, Tailwind CSS

### Outcomes

- Built real-time voice conversation system
- Implemented WebSocket-based audio streaming
- Created stateful voice sessions with Durable Objects
- Achieved global edge deployment for low latency
- Integrated multiple AI providers for speech processing

## [Realtime API Web Console](https://github.com/tetratensor/Realtime-AI-Web-Console)

### Overview

Real-time AI conversation web console with WebSocket communication between Next.js frontend and FastAPI backend, supporting multimodal AI interactions.

### Tech Stack

- Next.js, TypeScript, Tailwind CSS
- Python, FastAPI, WebSocket
- Gemini 2.0 Multimodal Live API
- GitHub Actions CI/CD

### Outcomes

- Built real-time voice and text conversation system
- Implemented WebSocket communication architecture
- Integrated multiple AI providers (Gemini, Nijivoice)
- Created responsive web interface with modern UI
- Set up automated CI/CD pipeline

## [Resume Analyzer](https://github.com/tetratensor/ML-powered_resume_analyser)

### Overview

Local, privacy-friendly resume analysis and classification system using traditional ML and modern embeddings for resume screening and advice generation.

### Tech Stack

- Python 3.8+, scikit-learn
- TF-IDF, Logistic Regression, sentence-transformers
- PDF/DOCX processing, pandas, NumPy
- YAML configuration

### Outcomes

- Built comprehensive resume analysis pipeline
- Implemented multiple ML algorithms for classification
- Created automated advice generation system
- Developed CLI tools for batch processing
- Achieved high accuracy on resume categorization

## [Stock Market Sentiment Analysis](https://github.com/tetratensor/Multimodal)

### Overview

Financial news sentiment analysis using fine-tuned DistilRoBERTa model for predicting market sentiment from financial news articles.

### Tech Stack

- Python, Transformers (Hugging Face)
- DistilRoBERTa, financial datasets
- Jupyter notebooks, pandas, NumPy
- Custom fine-tuning pipeline

### Outcomes

- Fine-tuned DistilRoBERTa for financial sentiment analysis
- Achieved 91.71% accuracy on financial news classification
- Built comprehensive training and evaluation pipeline
- Created automated data processing workflows
- Optimized model for production deployment

## [Multimodal AI Toolkit](https://github.com/tetratensor/Multimodal)

### Overview

Lightweight Python toolkit for end-to-end speech and text workflows including speech-to-text, NER anonymization, sentiment analysis, and document-to-speech conversion.

### Tech Stack

- Python 3.8+, VOSK, Transformers
- Hugging Face models, FFmpeg
- PDF/DOCX processing, TTS integration
- YouTube audio processing

### Outcomes

- Built comprehensive multimodal AI toolkit
- Implemented speech anonymization with beep insertion
- Created document-to-speech conversion system
- Developed question-answering from speech context
- Achieved high accuracy across multiple AI tasks

## [Time Logger Web](https://github.com/tetratensor/commew)

### Overview

Web-based time tracking application with comprehensive project management features, built with Next.js and modern UI components.

### Tech Stack

- Next.js 13, React 18, TypeScript
- Mantine UI, Tailwind CSS
- NextAuth, JWT authentication
- Storybook, Jest testing

### Outcomes

- Built comprehensive time tracking web application
- Implemented modern UI with Mantine components
- Created authentication and user management system
- Developed testing suite with Storybook integration
- Built responsive design for multiple devices

## [Financial Metrics vs Global Markets](https://github.com/tetratensor/FinancialMetrics_GlobalMarkets_Analysis)

### Overview

Comprehensive analysis project exploring how U.S. economic metrics (GDP and Consumer Price Index) impact the performance of major world stock exchanges. The project investigates correlations between U.S. economic indicators and global market performance across developed and developing countries.

### Tech Stack

- Python, Jupyter Notebooks
- FRED API (Federal Reserve Economic Data)
- Yahoo Finance API
- Pandas, NumPy, Matplotlib
- Statistical analysis libraries

### Outcomes

- Built comprehensive financial data analysis system
- Implemented automated data retrieval from FRED and Yahoo Finance APIs
- Analyzed correlations between U.S. GDP/CPI and 10 major global stock exchanges
- Created visualizations comparing developed vs developing market sensitivity
- Developed statistical models to test research hypotheses
- Achieved significant insights into global market interdependencies

## [LiveKit Voice Agents](https://github.com/tetratensor/LiveKit-Outbound-Caller-Voice-Agent)

### Overview

Production-ready voice agent system built with LiveKit Agents framework, featuring AI-powered conversations, function calling capabilities, and seamless Twilio integration for both inbound and outbound phone calls.

### Tech Stack

- Python 3.10+, LiveKit Agents framework
- OpenAI GPT-4o-mini, Deepgram STT, ElevenLabs TTS
- Twilio SIP trunking, WebRTC
- Docker, environment configuration
- Real-time communication protocols

### Outcomes

- Built production-ready voice agent with inbound/outbound call capabilities
- Implemented advanced speech processing with telephony-optimized models
- Created function calling system for real-time data access (weather, time queries)
- Integrated Twilio SIP trunking for PSTN connectivity
- Developed comprehensive monitoring and logging system
- Achieved high-quality voice interactions with noise cancellation and turn detection
- Built CLI tools for development, health checks, and model prewarming

## [Trained YOLOv8 Violence Detection](https://github.com/tetratensor/yolo-realtime-violence-ai)

### Overview

Real-time violence detection system using custom-trained YOLO model for analyzing video feeds, identifying potential violent behavior, and issuing automated alerts for immediate action.

### Tech Stack

- Python 3.6+, OpenCV, Ultralytics YOLO
- Custom dataset training, Roboflow integration
- SMTP email notifications, real-time video processing
- Dual-model architecture (general detection + violence detection)

### Outcomes

- Developed dual-model violence detection system with high accuracy
- Created custom dataset and trained specialized YOLO model
- Implemented real-time video processing with continuous monitoring
- Built automated email alert system with incident snapshots
- Achieved high true positive rate with low false positive rate
- Created comprehensive validation and testing framework
- Developed production-ready system for public safety applications
