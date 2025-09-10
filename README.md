<div align="center">

  <h1>🎛️ Prompt Vault</h1>
  <p>A curated, professional library of ready‑to‑use AI prompts for multiple tasks and models.</p>
  <p><b>License:</b> MIT • <b>Contributions:</b> Welcome • <b>Models:</b> GPT · Claude · Grok · Llama · Gemini · Sonar · DeepSeek · Manus · Kimi</p>

</div>

---

## Overview
Prompt Atelier is a structured collection of high‑quality prompts for AI models, organized by use case and designed for quick copy‑paste reuse and easy adaptation.  
It emphasizes clarity, consistency, and portability across providers and model versions.

## Highlights
- Multi‑model coverage with explicit compatibility notes per prompt for smooth switching.  
- Clear categories (Coding, Research, Writing, Marketing, Data, System) for fast navigation.  
- Copy‑ready snippets with variables, guardrails, acceptance criteria, and output schemas.  
- Style guide and conventions to keep prompts consistent and maintainable.  
- Straightforward contribution workflow (issues, PRs, review checklist).

## Table of Contents
- [Overview](#overview)  
- [Highlights](#highlights)  
- [Repository Structure](#repository-structure)  
- [Quick Start](#quick-start)  
- [Prompt Specification](#prompt-specification)  
- [Prompt Template](#prompt-template)  
- [Style Guide](#style-guide)  
- [Contributing](#contributing)  
- [Versioning & Naming](#versioning--naming)  
- [License](#license)  
- [Roadmap](#roadmap)  
- [FAQ](#faq)  
- [Changelog](#changelog)

## Repository Structure
prompt-atelier/
├─ README.md
├─ LICENSE
├─ CONTRIBUTING.md
├─ /coding/
│ ├─ code-review/
│ ├─ bug-fixing/
│ └─ refactoring/
├─ /research/
│ ├─ literature-review/
│ └─ summarization/
├─ /writing/
│ ├─ blog/
│ └─ email/
├─ /marketing/
│ ├─ product/
│ └─ social/
├─ /data/
│ ├─ analysis/
│ └─ cleaning/
└─ /system/
├─ role/
└─ guardrails/

text

## Quick Start
1. Browse the categories and pick a prompt that matches the task at hand.  
2. Copy the prompt, fill in the variables (e.g., {{topic}}, {{tone}}), and adapt constraints to the model.  
3. Check “Model Compatibility” and prefer prompts aligned with the chosen provider/version.  
4. Test iteratively; if improved, save a new variant or open a PR to contribute back.

## Prompt Specification
Use a consistent structure for each prompt to improve reuse, testing, and review:

- Title: Short, action‑oriented (e.g., “Fact‑Checked Research Summary”).  
- Goal: One‑sentence expected outcome.  
- Model Compatibility: Providers/versions known to perform well (e.g., GPT‑4o, Claude 3.5, Llama 3.1‑70B).  
- Instructions: Steps, constraints, and acceptance criteria.  
- Inputs/Variables: Mark placeholders like {{topic}}, {{length}}, {{tone}}.  
- Output Format: Markdown/JSON with schema when relevant.  
- Notes: Failure modes, fallback strategies, evaluation hints.

## Prompt Template
<details>
<summary><b>Markdown template (recommended)</b></summary>

Title: Fact‑Checked Research Summary
Goal:
Produce a concise, source‑aware summary with clear citations.

Model Compatibility:

GPT‑4o

Claude 3.5

Llama 3.1‑70B

Instructions:

Scope: Summarize the latest findings about {{topic}} for a technical audience.

Constraints: Max {{length}} words; avoid speculation; include 3–5 reputable sources.

Method: Extract claims → verify with sources → synthesize → highlight limitations.

Tone: {{tone}}.

Output: Markdown with sections: Summary, Key Findings (bullets), Sources (list).

Inputs/Variables:

{{topic}}: research subject

{{length}}: 200–400

{{tone}}: neutral | persuasive | executive

Acceptance Criteria:

Accurate, verifiable claims with consistent citations.

No hallucinations or unsupported assertions.

Clear, scan‑friendly structure.

Example Output Skeleton:

Summary
...

Key Findings
...

Sources
...

text
</details>

<details>
<summary><b>Optional metadata front matter (for tools/automation)</b></summary>

title: Fact-Checked Research Summary
task: research_summary
models:

gpt-4o

claude-3.5-sonnet

llama-3.1-70b
inputs:
topic: string
length: integer
tone: enum [neutral, persuasive, executive]
output_format: markdown
risk: low
license: MIT

text
</details>

## Style Guide
- Clarity first: prefer plain, unambiguous language and concrete acceptance criteria.  
- Variables explicit: wrap placeholders in {{braces}} and define ranges or enums.  
- Guardrails: state failure modes (“do not fabricate data”) and verification steps.  
- Output schemas: provide a minimal JSON or Markdown skeleton to standardize results.  
- Brevity: keep prompts minimal; move rationale and commentary to “Notes”.

## Contributing
- Propose new categories via issues; small additions can be direct PRs.  
- One PR = one scope; include examples and update README structure if impacted.  
- Use clear commit messages (feat:, fix:, docs:, refactor:, chore:).  
- Follow the Prompt Specification and Style Guide; maintain consistency across folders.  
- Add or update tests/evaluation prompts if a change affects output quality.

## Versioning & Naming
- Semantic naming: <category>/<task>/<slug>.md (e.g., research/summarization/fact-checked.md).  
- Variants: append -v2, -strict, -lite for meaningful differences.  
- Deprecation: add a note at the top and link to the preferred alternative.

## License
Unless indicated otherwise, the content is released under the MIT License to maximize reuse with attribution.  
Include a LICENSE file at the repository root to formalize the terms.

## Roadmap
- Add evaluation prompts for automated scoring and A/B testing.  
- Provide JSON schema templates for structured outputs per category.  
- Add quick‑start guides per model with known limits and tips.

## FAQ
- Q: Which model should I start with?  
  A: Pick a prompt tagged for the model available; then iterate and compare variants.  
- Q: How do I avoid hallucinations?  
  A: Use the guardrails in each prompt, require sources, and validate claims before use.  
- Q: Can I contribute proprietary prompts?  
  A: Only if licensing allows; otherwise share redacted or generalized versions.

## Changelog
- 0.1.0 — Initial structure, template, and style guide.

