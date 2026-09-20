# RADAS V3 — Official Product & Development Roadmap

**Document role:** Single Source of Truth  
**Project:** RADAS V3 — AI Creative Studio  
**Repository:** `radas-v3`  
**Status:** Approved working baseline  
**Version:** 1.3
**Source baseline:** `Pasted markdown(6).md` — RADAS V3 — AI Creative Studio

---

## 1. Authority of This Document

This file is the official product and development roadmap for RADAS V3.

All future discussions, audits, architecture decisions, implementation plans, patches, tests and release decisions for RADAS V3 must refer to this document.

If a later request conflicts with this document:

1. Do not silently change direction.
2. Identify the conflict clearly.
3. Record the founder's decision.
4. Update this document first.
5. Continue work only against the updated version.

Chat discussions, temporary notes, mockups and implementation ideas are not authoritative unless incorporated into this file.

### Source-of-truth hierarchy

1. Latest approved version of this roadmap.
2. Approved phase specification linked from this roadmap.
3. Approved architecture decision record.
4. Repository code and tests at the locked phase baseline.
5. Temporary discussion or exploratory notes.

---

## 2. Official Product Definition

> RADAS V3 is an AI Creative Studio that transforms products and ideas into ready-to-use visual content, especially short-form videos, while intelligently managing AI models, cost and production workflow behind a simple user experience.

Core promise:

> Turn products and ideas into videos.

Versi BM:

> Dari produk atau idea kepada video dalam beberapa klik.

Core differentiator:

> User focuses on the idea. RADAS handles the creative production pipeline.

RADAS V3 is a separate product direction. It is not a new screen, theme or direct migration of RADAS V1 or V2.

---

## 3. Locked Project Boundaries

### 3.1 Repository isolation

- RADAS V1 remains preserved.
- RADAS V2 remains preserved.
- RADAS V3 uses a new repository named `radas-v3`.
- V3 must not overwrite, migrate or modify V1/V2 production repositories.
- V3 may reuse relevant branding, ideas, IP or frameworks only after explicit review.
- V3 architecture and UI are independent of V1/V2.

### 3.2 MVP product boundary

RADAS V3 MVP contains only three creation modes:

1. **Product Video**
2. **Story**
3. **Image**

Supporting areas:

- My Products
- My Creations
- Credits
- Settings

### 3.3 Explicitly outside MVP

- Remix / Reference Ad
- Separate Ad Skit screen
- AI Talent / reusable avatar library
- Brand Kit
- 60–120 second stories
- Campaign Generator
- Batch Generation
- Agency Workspace
- Advanced model settings
- Provider selection by users
- Raw prompt controls
- Developer controls
- Advanced resolution controls
- Unlimited generation
- Subscription-dependent content database

These items must not enter an MVP phase without an approved roadmap change.

---

## 4. Product Principles

1. **Output, not education.** RADAS produces usable creative assets; it does not sell prompts, worksheets or tutorials as its core product.
2. **Input to output.** Minimise settings between the user's intent and the completed asset.
3. **One creative AI.** Models, providers and technical workflows stay behind the RADAS interface.
4. **Visual-first experience.** The product should feel like an AI creative studio, not an affiliate analytics dashboard.
5. **Minimum founder maintenance.** Avoid manual curation, daily editorial work and continuously maintained product databases.
6. **Provider independence.** RADAS must not be permanently locked to Atlas Cloud or any single AI provider.
7. **Cost-aware by design.** Real provider costs and retry risk determine credit economics.
8. **Benchmark before pricing.** No final selling price or credit value may be locked before `RADAS COST-00` is completed.
9. **Audit before heavy refactoring.** Understand the Atlas baseline before replacing its architecture.
10. **Commercial launch requires licence clarity.** README claims alone are insufficient for final commercial clearance.

---

## 5. Target User Experience

### 5.1 Product Video

```text
Choose Product
↓
Choose Video Style
↓
Choose Duration
↓
Choose Quality
↓
Generate
```

Initial styles:

- UGC
- Commercial
- Product Demo
- POV
- Product Story

Initial duration:

- 10 seconds
- 15 seconds

User-facing quality:

- Fast
- Quality

### 5.2 Story

```text
Idea
↓
Script
↓
Character Definition
↓
Scene Plan
↓
Images and Motion
↓
Voice and Music
↓
Subtitle
↓
Final Video
```

Initial styles:

- Cinematic
- Emotional
- Comedy
- Horror
- Inspirational

Initial duration:

- 15 seconds
- 30 seconds

Longer stories are deferred until generation economics and reliability are stable.

### 5.3 Image

Initial types:

- Product Image
- Lifestyle Product Image
- Social Media Visual
- Poster
- Cinematic Image

Generated images may also serve as lower-cost intermediate assets in video composition.

---

## 6. Roadmap Governance

### 6.1 Phase status

Each phase must use one status:

- `NOT STARTED`
- `IN PROGRESS`
- `BLOCKED`
- `READY FOR REVIEW`
- `APPROVED`
- `COMPLETE`

### 6.2 Gate rule

A downstream phase may begin only when its required gate is approved. Exploratory research is allowed, but it must not silently become production implementation.

### 6.3 Phase completion record

Every completed phase must record:

- starting repository commit
- ending repository commit
- scope completed
- files or systems changed
- tests and audit evidence
- known risks
- deferred work
- founder approval

### 6.4 Change control

Any proposed change to product scope, architecture, provider strategy, pricing model or MVP feature set must be recorded under the Change Log at the end of this document.

---

# 7. Official Phased Roadmap

## PHASE 0 — Project Isolation and Governance

**Phase ID:** `RADAS-V3-00`
**Status:** `COMPLETE`
**Objective:** Establish RADAS V3 as a clean, isolated project with an auditable baseline.

### Scope

- Create the new `radas-v3` repository.
- Confirm V1 and V2 remain untouched.
- Add the official project README and this roadmap.
- Establish branch and commit conventions.
- Record the Atlas upstream repository URL, branch and exact commit.
- Record whether Atlas is cloned, forked or used only as a reference.
- Create an audit workspace without changing product behaviour.

### Deliverables

- new repository
- initial baseline commit
- upstream baseline record
- repository isolation confirmation
- project decision log structure
- environment-variable inventory template with no secrets committed

### Exit gate — `GATE-0`

- `radas-v3` exists independently.
- No V1/V2 repository or production environment has been modified.
- The exact Atlas baseline is reproducible.
- This roadmap is present in the V3 repository.

### Prohibited during this phase

- product feature development
- major refactoring
- UI redesign implementation
- production deployment

---

## PHASE 1 — Atlas Repository, Licence and Dependency Audit

**Phase ID:** `RADAS-V3-01 / AUDIT-00A`
**Status:** `COMPLETE`
**Depends on:** `GATE-0` — approved 2026-09-20
**Objective:** Determine exactly what Atlas contains, whether it builds, and what may safely be reused.

### Audit scope

#### Repository

- latest commit and selected baseline commit
- branch structure and activity
- repository completeness
- build and test commands
- deployment configuration
- missing or generated files

#### Licence

- root `LICENSE` file
- `package.json` licence field
- README licence claims
- file-level notices
- third-party assets and licences
- commercial use, modification and redistribution rights
- written confirmation from AtlasCloudAI if repository evidence remains incomplete

#### Dependencies

- Next.js and React versions
- Prisma and database adapters
- authentication packages
- AI SDKs and provider packages
- storage clients
- FFmpeg integration
- payment packages
- deprecated packages
- security advisories
- incompatible or abandoned dependencies

### Required classification

Every meaningful Atlas module must be classified as:

- `KEEP` — directly reusable or a strong reference
- `HIDE` — retained temporarily but excluded from V3 MVP UI
- `REPLACE` — incompatible with RADAS product or architecture
- `REMOVE LATER` — unused and safe to remove only after baseline verification
- `UNKNOWN` — requires further testing

### Deliverables

- Atlas baseline audit report
- licence evidence report
- dependency inventory
- module classification matrix
- initial risk register

### Exit gate — `GATE-1`

- Exact Atlas baseline is documented.
- Licence state is labelled clearly as `CONFIRMED`, `UNRESOLVED` or `REJECTED`.
- Build prerequisites are known.
- No commercial-safety claim is made without adequate evidence.
- `KEEP / HIDE / REPLACE` classification is complete enough for functional testing.

### Commercial restriction

Prototype and audit work may continue while the licence is unresolved. Commercial launch may not proceed until the required reuse rights are confirmed or Atlas code has been replaced with legally safe alternatives.

### Completion record — `GATE-1`

- Founder approval: `APPROVED - 2026-09-21`.
- Atlas baseline audited: `AtlasCloudAI/atlas-marketing-studio main@18ec178052f6f97612813997613d88ce34b02fc5`.
- Licence state: `UNRESOLVED`.
- Reuse boundary: `ZERO-CODE-REUSE` until canonical licence evidence confirms the required commercial rights.
- Clean clone of the exact baseline: `PASS`.
- Dependency installation: completed far enough to run the repository test suite; deprecated dependency warnings were recorded.
- Test suite: `PASS` — 11 tests passed, 0 failed.
- Production build on Windows / Node `v22.22.2`: `FAIL` before `next build` because `scripts/generate-prisma-clients.mjs` calls `spawnSync(...\prisma.cmd)` and Node returns `EINVAL`.
- The Windows failure is documented as a portability/build-tooling finding; it does not establish that Linux or Vercel builds fail.
- Atlas module classification and initial risk register are complete enough to proceed to functional baseline testing.
- No Atlas source has been imported into RADAS V3.

---

## PHASE 2 — Clean Functional Baseline

**Phase ID:** `RADAS-V3-02 / AUDIT-00B`  
**Status:** `IN PROGRESS`
**Depends on:** `GATE-1` — approved 2026-09-21
**Objective:** Run Atlas cleanly and document what genuinely works before redesigning it.

### Functional checks

- clean install
- production build
- local run
- login and logout
- product upload
- image generation
- video generation
- task submission
- asynchronous polling
- generation history
- credit charge
- credit refund on failure
- media storage
- output retrieval and download
- payment flow in test mode, if configured
- FFmpeg composition path

### Evidence required

For each flow, record:

- configuration required
- endpoint or action used
- expected result
- actual result
- logs and errors
- external dependency
- reproducibility
- pass, partial or fail status

### Deliverables

- clean-build report
- functional baseline matrix
- failure and blocker list
- environment configuration map
- reproducible baseline instructions

### Exit gate — `GATE-2`

- Clean build result is documented.
- All core flows have an evidence-backed status.
- Failures are mapped to specific layers.
- Atlas behaviour can be compared against future RADAS changes.

---

## PHASE 3 — Architecture, Data, Credits, Media and Security Audit

**Phase ID:** `RADAS-V3-03 / AUDIT-00C`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-2`  
**Objective:** Map all cost-bearing and security-sensitive paths before implementation.

### AI endpoint map

For every AI call, record:

- provider
- model
- endpoint
- input type
- output type
- duration constraints
- resolution constraints
- quoted or measurable cost
- task polling method
- timeout
- retries
- failure condition
- fallback behaviour

### Database audit

- User lifecycle
- Creation lifecycle
- CreditLedger lifecycle
- AdProduct / future My Products mapping
- AdAvatar and BrandKit relevance
- indexes
- ownership enforcement
- duplicate records
- race conditions
- concurrent credit spending
- idempotency
- failure and refund records

### Media audit

- upload size and type limits
- image processing
- public versus private URLs
- signed URL behaviour
- R2 / Blob behaviour
- retention and cleanup
- orphaned assets
- storage growth
- download permissions

### Auth and payment audit

- session handling
- protected routes
- user-resource ownership
- payment callback validation
- webhook signatures
- duplicate callbacks
- credit top-up idempotency

### Security audit

- API key exposure
- authentication bypass
- insecure direct object reference
- SSRF
- malicious URLs
- file upload abuse
- MIME spoofing
- oversized uploads
- webhook forgery
- prompt or job injection risk
- rate limits
- duplicate generation
- uncontrolled retries
- provider cost overrun
- log leakage

### Infrastructure decision audit

Evaluate, without prematurely locking:

- Cloudflare Workers
- D1
- R2
- Vercel
- Neon Postgres
- Vercel Blob
- FFmpeg execution constraints
- background job and serverless duration limits

Cloudflare is the preferred initial direction, but the final decision remains conditional on baseline and workload evidence.

### Deliverables

- AI endpoint map
- database and credit lifecycle map
- storage/auth/payment map
- security findings ranked by severity
- infrastructure fit report
- remediation backlog

### Exit gate — `GATE-3`

- Every generation path and cost-bearing action is mapped.
- Credit charge/refund risks are understood.
- Critical security findings have a defined treatment.
- Infrastructure constraints are evidence-backed.
- The system is ready for real cost benchmarking.

---

## PHASE 4 — Real Model and Cost Benchmark

**Phase ID:** `RADAS-COST-00`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-3`  
**Objective:** Determine actual generation economics, reliability and acceptable output quality before pricing or provider selection.

### Controlled benchmark

Use the same product, source image, prompt intent and evaluation method across candidates.

Benchmark available candidates such as:

- Mini
- Fast
- Standard

Test where supported:

- 480p
- 720p
- 5 seconds
- 10 seconds
- 15 seconds

These benchmark labels do not need to appear in the user interface.

### Record for every run

- provider and model
- provider quote
- actual API cost
- generation time
- queue time
- visual quality
- product consistency
- face/character consistency
- motion quality
- audio quality, where applicable
- output resolution
- file size
- success or failure
- retries
- effective cost including failed attempts

### Evaluation output

- cheapest acceptable image model
- cheapest acceptable video model
- most reliable model
- best quality model
- use-case suitability
- retry allowance recommendation
- cost range per completed asset
- evidence for Fast and Quality routing

### Cost-composition experiment

Compare full AI-video generation against a hybrid sequence using:

- short AI video clips
- generated still images
- pan, zoom and Ken Burns movement
- transitions
- subtitle and CTA overlays
- voice and music
- FFmpeg composition

The benchmark must measure cost per **completed final video**, not only cost per successful model call.

### Deliverables

- benchmark dataset
- representative outputs
- quality scoring rubric
- provider comparison
- recommended routing profiles
- retry and safety allowance
- provisional unit economics

### Exit gate — `GATE-4`

- At least one viable path exists for each planned MVP mode, or the unsupported mode is formally blocked.
- Actual cost and failure rates are known well enough to design credits.
- Fast and Quality profiles have evidence-backed provider options.
- No final customer pricing is yet presented as locked.

### Hard rule

Final pricing, credit value and broad feature implementation must not be locked before this gate.

---

## PHASE 5 — RADAS Target Architecture

**Phase ID:** `RADAS-V3-05`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-4`  
**Objective:** Design the minimum architecture required for the RADAS MVP using audit and benchmark evidence.

### Required architecture

```text
RADAS Application
↓
RADAS AI Router
↓
Provider Adapters
↓
Image / Video / Audio / Text Providers
```

Suggested internal structure:

```text
src/lib/ai/
├── router.ts
├── provider.ts
├── pricing.ts
└── providers/
    ├── atlas.ts
    ├── selected-provider.ts
    └── future-provider.ts
```

Standard internal capabilities:

- `generateText()`
- `generateImage()`
- `generateVideo()`
- `generateAudio()`
- `pollTask()`
- `calculateCost()`

### Routing rules

The user selects only:

- Fast
- Quality

Internally, RADAS may use evidence-backed routing profiles based on:

- use case
- cost
- quality
- speed
- reliability
- availability

Provider and model names remain hidden from normal users.

### Pricing engine design

```text
Actual Provider Cost
+ Retry/Safety Allowance
= RADAS Internal Cost
+ RADAS Margin
= User Credit Charge
```

Provider prices must be configuration-driven or recorded in a maintainable pricing layer, not scattered as unexplained hard-coded values.

### Key decisions required

- selected database
- selected media storage
- selected auth path
- background task mechanism
- FFmpeg execution location
- provider adapter contract
- job idempotency strategy
- credit reservation and settlement strategy
- failed-job refund strategy

### Deliverables

- target architecture document
- provider interface contract
- generation job lifecycle
- credit lifecycle
- media lifecycle
- architecture decision records
- implementation sequence

### Exit gate — `GATE-5`

- Architecture supports more than one provider without user-facing complexity.
- Credit and job lifecycles are safe under retries and concurrency.
- Infrastructure is selected based on tested requirements.
- No unnecessary database migration is included.

---

## PHASE 6 — New RADAS V3 Product and UI Specification

**Phase ID:** `RADAS-V3-06`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-5`  
**Objective:** Design the V3 interface from zero as an AI creative studio.

### Navigation

```text
RADAS

Create
├── Product Video
├── Story
└── Image

My Products
My Creations
Credits
Settings
```

### Home

```text
RADAS AI

What do you want to create?

[ Product Video ]
[ Story ]
[ Image ]

Recent Creations
```

### Design requirements

- premium
- minimal
- visual-first
- generous spacing
- simple commands
- strong preview experience
- clear generation progress
- mobile friendly
- creator friendly
- no analytics dashboard clutter
- no affiliate research appearance
- no exposed provider or model configuration

### Required UX specifications

- empty states
- upload states
- validation errors
- pending and queued states
- generating states
- completed states
- failed and retry states
- insufficient-credit state
- download/output state
- mobile layout
- accessibility baseline

### Deliverables

- approved information architecture
- approved low-fidelity flows
- approved visual direction
- responsive screen specification
- state and error catalogue
- component inventory

### Exit gate — `GATE-6`

- Founder approves the V3 product flow and visual direction.
- The design is not a recoloured V1/V2 or Atlas dashboard.
- All MVP states are specified before broad frontend implementation.

---

## PHASE 7 — Core Platform Foundation

**Phase ID:** `RADAS-V3-07`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-6`  
**Objective:** Build the stable foundation shared by all creation modes without exposing deferred features.

### Scope

- V3 application shell
- auth and user ownership
- My Products
- My Creations
- generation status
- media upload and storage
- provider interface
- initial AI router
- creation records
- credit ledger foundation
- job idempotency
- error handling
- observability baseline

### Atlas handling

- Preserve useful and verified baseline behaviour.
- Hide non-MVP features.
- Replace Atlas-specific coupling incrementally.
- Do not break the known generation path while introducing the router.
- Do not delete deferred modules merely for code cleanliness before dependencies are understood.

### Exit gate — `GATE-7`

- A user can authenticate, save a product and view owned creations.
- Generation jobs have durable status and ownership.
- Duplicate submission and duplicate charging have defined protection.
- The provider layer is no longer structurally locked to one provider.

---

## PHASE 8 — Image MVP

**Phase ID:** `RADAS-V3-08`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-7`  
**Objective:** Release the lowest-cost complete creative workflow first and validate the platform foundation.

### Scope

- Product Image
- Lifestyle Product Image
- Social Media Visual
- Poster
- Cinematic Image
- Fast and Quality routing
- creation status
- thumbnail and preview
- download
- credit settlement and failure refund

### Why image first

- lower generation cost
- faster test cycle
- validates upload, storage, jobs, credits and history
- creates reusable assets for video workflows

### Exit gate — `GATE-8`

- Image flows complete end to end.
- Credit charge and refund behaviour is verified.
- Outputs are stored and accessible only to authorised users.
- Actual production-like cost remains within the approved benchmark range.

---

## PHASE 9 — Product Video MVP

**Phase ID:** `RADAS-V3-09`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-8`  
**Objective:** Turn a saved or uploaded product into a ready-to-use short-form video.

### Scope

- product selection
- UGC
- Commercial
- Product Demo
- POV
- Product Story
- 10-second and 15-second duration
- Fast and Quality profiles
- scene planning
- short generated clips
- image-motion segments
- subtitle
- CTA
- voice/music where supported
- FFmpeg composition
- final MP4

### Cost-control requirement

Default composition should prefer the lowest-cost acceptable mix of still images, short generated motion clips and FFmpeg effects. Full-duration AI video must not become the default unless benchmark evidence supports it.

### Exit gate — `GATE-9`

- Product Video works end to end for the approved styles and durations.
- Final video cost is measured against the approved range.
- Product appearance is acceptably consistent.
- Failed composition and provider failures settle credits safely.
- Output is usable in a short-form social workflow.

---

## PHASE 10 — Story MVP

**Phase ID:** `RADAS-V3-10`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-9`  
**Objective:** Transform a short idea into a coherent visual story.

### Scope

- idea input
- script generation
- character definition
- scene planning
- image generation
- motion generation
- voice
- music
- subtitles
- composition
- 15-second and 30-second output
- Cinematic, Emotional, Comedy, Horror and Inspirational styles

### Deferred

- 60–120 second stories
- advanced character library
- reusable AI actors
- multi-episode continuity

### Exit gate — `GATE-10`

- Story works end to end for approved durations.
- Scene continuity and character consistency meet the agreed MVP threshold.
- Cost per completed story is measured and controlled.
- Failures do not produce duplicate charges or uncontrolled retries.

---

## PHASE 11 — Credits, Packaging and Payment

**Phase ID:** `RADAS-V3-11`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-10` and validated cost evidence  
**Objective:** Convert measured unit economics into a safe commercial model.

### Preferred commercial model

```text
One-Time RADAS Access
+ Starter Credits
+ Optional Credit Top-Ups
```

No unlimited generation. Subscription is not required for the initial model.

### Pricing work

- use actual provider cost
- include effective retry/failure cost
- include storage and composition cost
- include payment fees
- include safety allowance
- apply RADAS margin
- define credit packs
- define expiry policy, if any
- define refund treatment

### Payment candidates

- Stripe
- Billplz
- ToyyibPay

Selection must follow integration fit, fees, webhook quality and Malaysian customer requirements.

### Exit gate — `GATE-11`

- Credit value is supported by benchmark evidence.
- Payment top-ups are idempotent.
- Generation charging is concurrency-safe.
- Refund and failed-job rules are explicit.
- There is no unlimited-cost exposure.

---

## PHASE 12 — Production Hardening

**Phase ID:** `RADAS-V3-12`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-11`  
**Objective:** Make RADAS safe, observable and operationally manageable for real users.

### Hardening scope

- authentication and authorisation review
- API key protection
- ownership enforcement
- upload limits
- MIME and file-content validation
- URL and SSRF protection
- webhook validation
- rate limits
- user quotas
- duplicate-generation protection
- credit-abuse protection
- retry limits
- timeout handling
- provider budget caps
- concurrency controls
- storage cleanup
- orphan cleanup
- log redaction
- alerting
- audit trail
- health checks
- backup and recovery
- privacy and retention rules
- dependency vulnerability review

### Reliability scenarios

- provider timeout
- provider outage
- partial scene failure
- FFmpeg failure
- storage failure
- payment callback replay
- worker restart
- duplicate user click
- polling interruption
- job completes after client disconnect
- refund operation fails temporarily

### Exit gate — `GATE-12`

- No unresolved critical security issue.
- Cost caps and retry limits are enforced.
- Core failure scenarios have tests.
- Operations can identify, trace and reconcile failed jobs.
- Licence is cleared for the code actually used in the commercial build.

---

## PHASE 13 — Controlled Launch and Validation

**Phase ID:** `RADAS-V3-13`  
**Status:** `NOT STARTED`  
**Depends on:** `GATE-12`  
**Objective:** Validate the product with controlled real usage before wider marketing.

### Launch sequence

1. founder-only production test
2. controlled invited users
3. capped credit exposure
4. observe generation success and support load
5. correct cost or reliability issues
6. approve wider launch

### Launch metrics

- generation completion rate
- median generation time
- retry rate
- failure rate
- refund rate
- cost per completed image
- cost per completed Product Video
- cost per completed Story
- credit margin
- storage growth
- repeat creation rate
- downloads per completed creation
- founder support time

### Exit gate — `GATE-13`

- Unit economics remain within approved limits.
- Reliability meets the launch target.
- Founder maintenance is acceptable.
- No critical credit, security or storage issue is open.
- Wider launch is explicitly approved.

---

# 8. Phase Dependency Map

```text
V3-00 Project Isolation
↓
V3-01 Atlas / Licence Audit
↓
V3-02 Functional Baseline
↓
V3-03 Architecture / Security Audit
↓
COST-00 Real Benchmark
↓
V3-05 Target Architecture
↓
V3-06 New UI Specification
↓
V3-07 Core Foundation
↓
V3-08 Image MVP
↓
V3-09 Product Video MVP
↓
V3-10 Story MVP
↓
V3-11 Credits and Payment
↓
V3-12 Production Hardening
↓
V3-13 Controlled Launch
```

The order may be changed only through an approved update to this roadmap.

---

# 9. Atlas Baseline Disposition

## KEEP or use as strong reference

- Next.js application architecture
- Prisma where proven stable
- authentication
- User
- Creation
- CreditLedger
- product storage
- generation history
- asynchronous task polling
- generation status
- error handling
- media upload and storage
- FFmpeg
- credit architecture
- payment architecture
- Cloudflare and Vercel deployment knowledge

## HIDE from MVP

- Reference Ad
- separate Ad Skit screen
- Avatar Library
- Brand Kit
- advanced model settings
- provider selection
- raw prompt controls
- developer options
- advanced resolution configuration

## REPLACE or abstract

- Atlas Cloud lock-in
- hard-coded provider pricing
- user-facing model complexity
- UI that does not match RADAS V3
- any unsafe credit, retry or ownership implementation found in audit

No module may be permanently classified without repository-level evidence.

---

# 10. Definition of MVP Complete

RADAS V3 MVP is complete only when:

- V1 and V2 remain unaffected.
- Product Video, Story and Image operate end to end.
- My Products and My Creations work with user ownership.
- Users see Fast and Quality, not raw provider/model choices.
- AI Router supports provider abstraction.
- Generation jobs are durable, observable and idempotent.
- Credits are charged and refunded safely.
- Real unit economics are known.
- Payment top-up is safe and verified.
- Uploads and media access are secured.
- Critical security findings are resolved.
- Atlas reuse rights are confirmed or affected code is replaced.
- Founder maintenance remains low.
- Controlled launch evidence supports wider release.

---

# 11. Non-Negotiable Stop Conditions

Stop and seek a decision if:

- a task would modify RADAS V1 or V2
- Atlas licence evidence remains insufficient for the intended commercial use
- a provider cost cannot be bounded
- retries may create uncontrolled spending
- credits can be double-spent or double-charged
- a user can access another user's products or creations
- API keys may reach the client
- uploads or external URLs create an unresolved critical security risk
- a proposed feature expands MVP without an approved roadmap change
- a pricing proposal is based on estimates rather than completed benchmark evidence

---

# 12. Immediate Approved Work

The active work package is:

## `RADAS-V3-02 / AUDIT-00B — Clean Functional Baseline`

`RADAS-V3-01 / AUDIT-00A` was completed and `GATE-1` was approved by the founder on 2026-09-21.

`AUDIT-00B` is authorised for evidence-backed functional baseline work only. The Atlas licence remains `UNRESOLVED`, the `ZERO-CODE-REUSE` boundary remains active, and no RADAS product implementation or Atlas source import is authorised by this phase transition.

---

# 13. Decision Register

| ID | Decision | Status |
|---|---|---|
| DEC-001 | RADAS V3 is a separate product and repository. | LOCKED |
| DEC-002 | Repository name is `radas-v3`. | LOCKED |
| DEC-003 | RADAS V1 and V2 remain unchanged. | LOCKED |
| DEC-004 | V3 positioning is AI Creative Studio. | LOCKED |
| DEC-005 | MVP modes are Product Video, Story and Image. | LOCKED |
| DEC-006 | Atlas is a baseline/reference candidate, not a literal product clone. | LOCKED |
| DEC-007 | Commercial Atlas reuse requires stronger licence confirmation. | LOCKED |
| DEC-008 | AI provider architecture must support abstraction and routing. | LOCKED |
| DEC-009 | User-facing quality choices are Fast and Quality. | LOCKED |
| DEC-010 | Final pricing waits for `RADAS COST-00`. | LOCKED |
| DEC-011 | Preferred monetisation is one-time access plus credit top-ups. | PROVISIONAL |
| DEC-012 | Cloudflare Workers, D1 and R2 are the preferred initial infrastructure direction. | PROVISIONAL |
| DEC-013 | FFmpeg-based hybrid composition is the preferred cost-control strategy. | PROVISIONAL PENDING BENCHMARK |

---

# 14. Change Log

## Version 1.3

- Recorded founder approval and completion of `RADAS-V3-01 / AUDIT-00A` and `GATE-1` on 2026-09-21.
- Recorded Atlas licence state as `UNRESOLVED` with a `ZERO-CODE-REUSE` boundary.
- Recorded clean-clone success, 11/11 passing tests and the Windows production-build failure at `spawnSync(...\prisma.cmd) EINVAL`.
- Activated `RADAS-V3-02 / AUDIT-00B` for clean functional baseline work.
- Preserved infrastructure and target-architecture decisions as provisional until the roadmap-authorised architecture phases.

## Version 1.2

- Recorded founder approval and completion of `RADAS-V3-00 / GATE-0`.
- Recorded Phase 0 merge commit `699ae12f8d6d4976804f674a4b78db9e52f7a1ac`.
- Activated `RADAS-V3-01 / AUDIT-00A` for repository, licence and dependency audit only.

## Version 1.1

- Marked `RADAS-V3-00` as `IN PROGRESS`.
- Established the approved governance scaffold and audit baseline.
- Recorded Atlas `main@18ec178052f6f97612813997613d88ce34b02fc5` as the reproducible audit baseline.

## Version 1.0

- Established the official single source of truth.
- Converted the RADAS V3 concept into gated development phases.
- Preserved the original product direction, constraints and audit-first principle.
- Added governance, exit criteria, stop conditions and definition of MVP complete.

---

# 15. Approval Record

| Version | Approval | Date | Notes |
|---|---|---|---|
| 1.3 | Approved phase transition | 2026-09-21 | GATE-1 approved by founder; AUDIT-00A complete; RADAS-V3-02 / AUDIT-00B authorised. |
| 1.2 | Approved phase transition | 2026-09-20 | GATE-0 approved by founder; RADAS-V3-01 / AUDIT-00A authorised. |
| 1.1 | Approved for phase execution | 2026-09-20 | RADAS-V3-00A Governance Scaffold approved by founder. |
| 1.0 | Approved as official working baseline | — | Created under founder instruction as the single source of truth for RADAS V3. |
