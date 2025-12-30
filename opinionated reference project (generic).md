You are helping me stand up a small, opinionated reference project that will be published as:
- A GitHub repository (code + data/config + examples),
- An accompanying long-form article or whitepaper, and
- A clearly documented, CPE-eligible activity with social/publication artifacts.

This prompt is **framework-only**. Do NOT assume any specific domain like ATT&CK, D3FEND, PCI, or ransomware unless I provide it. Your job is to build the project pattern and breadcrumbs around whatever topic I give you.

## 1. New project inputs (I will fill these in)

- **Project name:** <PROJECT_NAME>
- **Domain / problem area:** <DOMAIN>
  (For example: "phishing simulations", "PCI DSS evidence mapping", "cloud misconfigurations".)
- **Primary modeling axis (axis A):** <AXIS_A>
  (For example: behaviors, requirements, stages, entities.)
- **Secondary modeling axis (axis B):** <AXIS_B>
  (For example: defenses, controls, capabilities, outcomes.)
- **Concrete implementation / evidence axis:** <AXIS_C>
  (For example: tests, jobs, scripts, checklists, data sources.)
- **Target scopes or environments:** <SCOPES>
  (For example: lab, staging, prod, specific business units.)

Your first task is to restate these inputs clearly and propose a **one-sentence working definition** for the project.

---

## 2. What to create (high-level)

Using those inputs, create the following artifacts in Notion, ready for copy-paste into a GitHub repo and external article. **Every artifact must include breadcrumbs that state what has been accomplished and what remains.**

### 2.1 Repo plan and structure (parent hub page)

Create a main hub page for the new project that includes:

- A **"You Are Here"** section at the top with:
  - Parent project reference (if any).
  - Purpose of the page.
  - Current status (what is already done).
  - Next updates (what still needs doing).
- Diagrams (Mermaid) for:
  - High-level project map (concept → repo → article → CPE/log → social).
  - Repo layout (for example: `data/`, `config/`, `src/`, `examples/`, `docs/`).
  - Data / domain model class diagram based on AXIS_A / AXIS_B / AXIS_C.
  - Workflow or resolver sequence (how inputs flow through the system to outputs).
- A README spine with headings that fit the new topic.
- Suggested GitHub description and topics/tags.
- A **checklist** covering:
  - Repo scaffolding.
  - Data/model implementation.
  - Article completion.
  - CPE log completion.
  - Social / sharing assets.

### 2.2 Copy-paste-ready repo contents (child pages)

Under the hub page, create child pages titled "📋 … Source (Copy-Paste Ready)" for:

- `README.md` – full content aligned to the new topic.
- Seed data / config files in `data/` and/or `config/` that express a **small, illustrative subset** of the model using AXIS_A / AXIS_B / AXIS_C.
- `src/model.py` (or equivalent) – skeletons for core model types (classes / dataclasses / types).
- `src/resolver.py` (or equivalent) – a thin layer that:
  - Loads the data/config.
  - Computes a simple, interpretable result (for example, a score, classification, or coverage view) per scope.
- `src/cli.py` (or equivalent) – minimal CLI with 1–3 commands (for example `show`, `gaps`, `summary`) that operate on a single axis value + scope.
- `examples/example_flow.md` (or similar) – one end-to-end scenario walkthrough using realistic IDs/names from the seed data.
- Root assets at repo top-level:
  - `.gitignore` – ignoring Python and venv artifacts (or analogous stack-specific ignores).
  - `requirements.txt` (or analogous) – minimal dependencies (standard library by default).
  - `LICENSE` – MIT or other specified license.

Each child page must include its own **"You Are Here"** block that states:
- Purpose of the file.
- Status (draft / ready to paste).
- Next updates (for example, “update once we finalize scoring logic” or “add more examples later”).

### 2.3 Article / whitepaper

Create:

1. A Notion article draft page with sectioned prose:
   - Introduction (problem framing and goals in the given DOMAIN).
   - Background (explain AXIS_A, AXIS_B, AXIS_C for this project).
   - Data / domain model.
   - Example walkthrough using the seed data (from `examples/example_flow.md`).
   - From slides / diagrams / concepts to **evidence or concrete outputs**.
   - Repository tour (what is in `data/`, `src/`, `examples/`, `docs/`).
   - Conclusion and next steps.
   - At least one or two Mermaid diagrams for educational purposes.

2. A separate child page with **copy-paste-ready Markdown** for `docs/article.md` or an external blog, mirroring the Notion article content.

Both pages must have a **"You Are Here"** section noting:
- Status of the article (for example, “sections 1–3 done, 4–7 need real tool output”).
- Next updates (for example, “insert final GitHub URL” or “tighten examples after first run”).

### 2.4 CPE evidence

Create a child page with a CPE log entry template that includes:

- Title.
- Certification body.
- CPE category.
- Date range.
- Hours by bucket (research, implementation, writing/documentation).
- Learning objectives (3–5 bullets) tailored to the DOMAIN.
- Description of the activity.
- Artifacts/evidence (repo URL, article URL, examples/diagrams).
- Attestation block: name, date, signature.

The CPE page must also include breadcrumbs describing:
- Whether this is a **template** or a **final** entry.
- Which fields still need to be filled in (for example, actual URLs, final hours, certification body).

### 2.5 Social / sharing content

Create a child page with:

- A LinkedIn-style **newsletter article summary** (shorter than the full article, using accessible language and referencing at least one diagram or example).
- A LinkedIn **intro post** with:
  - Hook (1–2 sentences) grounded in the DOMAIN.
  - 2–3 sentence summary of what the reference project does.
  - Call to action linking to the repo and article (placeholder URLs to be filled in later).
  - Relevant hashtags for the DOMAIN.

This page also needs a **"You Are Here"** section capturing:
- Whether URLs and diagrams are already inserted.
- What might be updated next based on audience feedback.

---

## 3. Breadcrumb and memory model

Throughout the creation phase you must:

- Use a **"You Are Here"** block at the top of every page and major child page.
- Maintain a **checklist** on the hub page that clearly indicates:
  - What is done.
  - What remains.
  - Where to look for copy-paste-ready assets.
- When a major artifact becomes stable (for example, README, article, CLI examples), update its page status from draft to ready and adjust the hub checklist accordingly.
- Prefer diagrams and concrete examples over abstract descriptions, especially when explaining flows or data models.

---

## 4. Style and constraints

- Use clear, practitioner-focused language appropriate to the DOMAIN.
- Keep the project small and inspectable: prefer a **thin vertical slice** over exhaustive coverage.
- Assume local-first workflows (run entirely on a developer laptop or lab host, no external SaaS dependencies, unless explicitly stated otherwise).
- For Python-based projects, do **not** use Homebrew in instructions; use `python3 -m venv` style for virtual environments.
- Include Mermaid diagrams for:
  - High-level project map.
  - Data/domain model.
  - Workflow / resolver.
- Use dedicated "📋 … Source (Copy-Paste Ready)" child pages for any long source files or configs.

When I provide new project inputs using this prompt, follow this framework to build the new repo plan, data/model, article, CPE entry, and social content. Track progress with breadcrumbs and checklists so it is always clear what has been accomplished and what remains.
