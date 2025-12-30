You are helping me stand up a small, opinionated reference project that will be published as:
- A GitHub repository (code + data + examples),
- An accompanying long-form article or whitepaper, and
- A clearly documented, CPE-eligible activity with social/publication artifacts.

I want you to follow the **same overall project pattern** used in a previous Ransomware Defense Mapping project, but adapted to a new topic. This includes:
- A structured repo,
- Documentation and article,
- CPE justification,
- Social sharing content, and
- **Breadcrumbs that track what has been accomplished and what remains at each stage.**

## 1. New project inputs (I will fill these in)

- **Project name:** <PROJECT_NAME>
- **Primary security topic / threat / capability:** <TOPIC_OR_THREAT>
- **Primary modeling axis (analog of ATT&CK):** <BEHAVIOR_MODEL>
  (For example: MITRE ATT&CK techniques, kill-chain stages, PCI DSS requirements.)
- **Defensive pattern axis (analog of D3FEND):** <DEFENSE_MODEL>
  (For example: D3FEND, control families, defensive capabilities.)
- **Concrete controls / tests axis:** <CONTROL_AXIS>
  (For example: controls + Platform0-style jobs, policies + evidence collection.)
- **Target environments or scopes:** <ENVIRONMENTS>
  (For example: lab, staging, prod, specific CDEs.)

Your first task is to restate these inputs clearly and propose a one-sentence working definition for the project.

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
  - Repo layout (for example: `data/`, `controls/`, `src/`, `examples/`, `docs/`).
  - Data model class diagram.
  - Resolver / workflow sequence.
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
- Minimal seed data files (for example, `data/*.json`, `controls/*.jsonl`) expressing the behavior → defense → control mapping for a small, illustrative subset.
- `src/model.py` – dataclass skeletons for the core entities in the model.
- `src/resolver.py` – a simple scoring/resolution function and data loading logic.
- `src/cli.py` – CLI skeleton with at least `map` and `gaps` (or analogous) commands.
- `examples/example_chain.md` (or analogous) – one end-to-end scenario walkthrough.
- Root assets:
  - `.gitignore` – ignoring Python, venv, editor, and test artifacts.
  - `requirements.txt` – minimal dependencies (standard library by default).
  - `LICENSE` – MIT or other specified license.

Each child page must include its own **"You Are Here"** block that states:
- Purpose of the file.
- Status (draft / ready to paste).
- Next updates (for example, “adjust once we finalize the scoring logic”).

### 2.3 Article / whitepaper

Create:

1. A Notion article draft page with sectioned prose:
   - Introduction (problem framing and goals).
   - Background (explain the modeling axes: behavior model, defense model, controls/tests).
   - Data model.
   - Example walkthrough using the seed data.
   - From slides / diagrams to evidence / coverage.
   - Repository tour.
   - Conclusion and next steps.
   - At least one or two Mermaid diagrams for educational purposes.

2. A separate child page with **copy-paste-ready Markdown** for `docs/article.md` or an external blog, mirroring the Notion article content.

Both pages must have a **"You Are Here"** section noting:
- Status of the article (e.g., “sections 1–3 done, 4–7 need real CLI output”).
- Next updates (e.g., “insert final GitHub URL” or “tighten examples after first run”).

### 2.4 CPE evidence

Create a child page with a CPE log entry template that includes:

- Title.
- Certification body.
- CPE category.
- Date range.
- Hours by bucket (research, implementation, writing).
- Learning objectives (3–5 bullets).
- Description of the activity.
- Artifacts/evidence (repo URL, article URL, examples/diagrams).
- Attestation block: name, date, signature.

The CPE page must also include breadcrumbs describing:
- Whether this is a **template** or a **final** entry.
- Which fields still need to be filled in (e.g., actual URLs and hours).

### 2.5 Social / sharing content

Create a child page with:

- A LinkedIn-style **newsletter article summary** (shorter than the full article, with at least one diagram reference).
- A LinkedIn **intro post** with:
  - Hook (1–2 sentences).
  - 2–3 sentence summary.
  - Call to action linking to the repo and article (URLs to be filled in).
  - Relevant hashtags.

This page also needs a **"You Are Here"** section capturing:
- Whether URLs and diagrams are already inserted.
- What might be updated next based on feedback.

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

- Use clear, practitioner-focused language for security engineering / assessment audiences.
- Keep the project small and inspectable: prefer a **thin vertical slice** over exhaustive coverage.
- Assume local-first workflows (run entirely on a developer laptop or lab host, no external SaaS dependencies).
- Do **not** use Homebrew in instructions; use `python3 -m venv` style for Python.
- Include Mermaid diagrams for:
  - High-level project map.
  - Data model.
  - Resolver / workflow.
- Use dedicated "📋 … Source (Copy-Paste Ready)" child pages for any long source files.

When I provide new project inputs using this prompt, follow this framework to build the new repo plan, data model, article, CPE entry, and social content. Track progress with breadcrumbs and checklists so it is always clear what has been accomplished and what remains.
