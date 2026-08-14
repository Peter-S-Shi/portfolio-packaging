# Portfolio Packaging

Turn a mature software repository into a clear, evidence-driven, recruiter-readable GitHub portfolio project.

`portfolio-packaging` is an Agent Skill for the **post-RC presentation stage**. It assumes product development, hardening, and release-candidate validation are already complete.

Its job is simple:

> Help a finished project become easy to understand, easy to evaluate, and strong as professional evidence.

---

## Why this exists

Many repositories become technically complete before they become portfolio-ready.

The code may work. Tests may pass. The release candidate may be done. But a first-time visitor may still encounter:

- a README that reads like a development log;
- important capabilities buried under internal terminology;
- missing or weak screenshots and outputs;
- engineering depth that is hard to discover;
- repository metadata that says little about the product;
- too much documentation, or the wrong information in the wrong place.

`portfolio-packaging` provides a structured workflow for the last presentation mile.

---

## What it does

```text
Mature repository
      ↓
Portfolio Story Audit
      ↓
README Packaging
      ↓
Optional specialist integrations
      ↓
Repository presentation
      ↓
Portfolio QA
      ↓
Preview + user approval
```

The Skill focuses on:

- portfolio positioning;
- recruiter-readable product story;
- README information architecture;
- real-proof selection;
- engineering-evidence selection;
- repository metadata;
- optional specialist integrations;
- presentation QA;
- safe handoff before publication.

---

## What it does not do

This is not a product-development or release-engineering workflow.

By default, it does not:

- add features;
- fix product bugs;
- refactor application code;
- redesign product architecture;
- expand tests;
- reopen hardening;
- change product behavior.

If packaging reveals that a public claim is broader than the product supports, the default response is to narrow the claim—not silently change the product.

---

## Four principles

### README-first

Use `README.md` as the primary product homepage and navigation layer.

### Minimum sufficient change

Make only the changes that materially improve clarity, evidence, and professional presentation.

### Real proof before claims

Prefer current screenshots, outputs, workflows, examples, and engineering evidence over marketing language or decoration.

### Product first, engineering second

First help a visitor understand the product. Then expose enough engineering depth for a technical reviewer to evaluate it.

---

## Repository structure

```text
portfolio-packaging/
├── SKILL.md
├── README.md
├── .gitignore
├── references/
│   ├── story-audit.md
│   ├── readme-packaging.md
│   └── portfolio-qa.md
└── integrations/
    ├── README.md
    └── .gitignore
```

The project is intentionally documentation-first.

Scripts, templates, and example libraries should be added only after repeated real use proves that they solve a stable recurring problem.

---

## How the pieces fit

### `SKILL.md`

The parent orchestration contract:

```text
what to do
when to read what
what is in scope
what requires user approval
```

### `references/story-audit.md`

How to understand the mature project before editing it:

```text
Audience
One-sentence value
Problem solved
Core capabilities
Primary proof
Engineering evidence
First successful action
```

### `references/readme-packaging.md`

How to present that story in GitHub without turning every repository into the same template.

### `references/portfolio-qa.md`

How to decide whether the public presentation is ready.

### `integrations/README.md`

How optional third-party specialist Skills plug into the workflow without becoming part of the core repository.

---

## Optional integrations

Third-party specialist Skills may be installed locally under:

```text
integrations/
```

Their source is Git-ignored by default.

The public repository tracks the integration contract, not third-party source.

Example:

```text
integrations/
├── README.md
├── .gitignore
└── beautify-github-readme/   # local only
```

The parent Skill owns portfolio strategy and final QA. A specialist receives only a bounded task.

> Integrate capabilities, not third-party source.

The core workflow must remain useful even when no integration is installed.

---

## What a successful package should communicate

A first-time visitor should quickly understand:

```text
What is this?
Who is it for or what problem does it solve?
What can it actually do?
What real proof should I look at?
What engineering ability does this project demonstrate?
Where do I go next if I want to try or inspect it?
```

The README should support both:

### Fast scan

For recruiters and hiring managers:

```text
product
proof
main capabilities
technical signal
```

### Deep inspection

For engineers:

```text
mechanism
architecture
testing
privacy
technical docs
source code
```

---

## Default packaging footprint

Typical public changes:

```text
README.md
assets/readme/**
repository presentation metadata
```

Existing specialized documentation is updated only when necessary.

Product code remains protected by default.

The Skill intentionally avoids documentation sprawl such as automatically creating:

```text
PORTFOLIO.md
SHOWCASE.md
FEATURES.md
CASE_STUDY.md
```

---

## Usage

Typical packaging pass:

```text
Use $portfolio-packaging to package this post-RC repository for a public GitHub portfolio.
Start read-only, preserve product code, and show me the README/asset diff before any push or publication.
```

Audit only:

```text
Use $portfolio-packaging to audit this mature repository for portfolio readiness.
Do not edit anything yet.
```

With local integrations:

```text
Use $portfolio-packaging to improve the README and repository presentation.
Use available local integrations when they add real value, but keep third-party source outside the public repository.
```

---

## Current maturity

This is an early working version.

The intended maturation path is:

```text
initial Skill architecture
→ real repository pilot
→ revise
→ test on different product types
→ identify stable cross-project rules
→ public-ready Skill
```

The goal is not the largest possible instruction set.

The goal is a small, clear, reusable workflow that remains reliable across different mature software projects.
