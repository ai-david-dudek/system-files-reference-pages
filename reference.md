# Muse System Files Reference

Snapshot as of: 2026-10-25. Generic reference only. Your tree may be a subset; folders appear as features are used; runtime folders may vary by deployment.

This page mirrors the home directory of a Muse instance, the area shown as “System Files” in the Muse app. System Files is a window into Muse’s own filesystem, not files on your device. This page describes purpose and expected contents at folder and file level only. It does not list file contents, and it does not name any real person, group, project, goal, or chat.

The interactive version of this reference is [index.html](index.html), served as the Pages site. This markdown version is the same generic tree, readable in the GitHub repository view.

## How to read this page

Markdown (`.md`) files are prose or notes meant to be read, and, where the tier allows, edited by a person. YAML (`.yaml`) and JSON (`.json`) files are structured settings or state meant to be read by software; hand-editing them can break the thing that reads them.

## Legend — edit tier (text badge, never colour alone)

- ● Editable — You are the intended author or owner. Hand-editing is expected and safe, within the file’s own rules.
- ◐ Edit via Muse — Muse maintains the file. Give corrections in conversation so Muse can reconcile them with background jobs and other records. Hand-editing can be overwritten or left inconsistent.
- ■ Do not edit — Runtime-managed, generated, system-provided, or private. Hand-editing risks breaking a job, losing state, or exposing a secret.
- _[Filesystem only]_ — Exists in the home directory but may not appear in the System Files browser.
- _[Appears when used]_ — The folder only exists once the corresponding feature has been used.

GitHub renders the `<details>` sections below as collapsible. Use your browser’s find function to search this page; the interactive search and tier filter are in [index.html](index.html).

## Index by edit tier

### ● Editable

- `SOUL.md`
- `IDENTITY.md`
- `USER.md`
- `workspace/`
- `workspace/your_files/`
- `workspace/user/`
- `workspace/custom-skills/<skill-name>/`

### ◐ Edit via Muse

- `AGENTS.md`
- `MEMORY.md`
- `PROACTIVE_PREFERENCES.md`
- `TOOLS.md`
- `HEARTBEAT.md`
- `memory/`
- `memory/YYYY-MM-DD.md`
- `memory/people/`
- `memory/groups/`
- `workspace/goals/<goal-slug>/`
- `workspace/custom-connectors/custom.<provider>/`
- `side-chats/<chat-id>/`

### ■ Do not edit

- `docs/`
- `config/`
- `memory/bank/ and memory/index/`
- `dreams/`
- `dreams/YYYY-MM-DD.md`
- `dreams/alignment/derived/ALIGNMENT_SYNTHESIS.md`
- `dreams/alignment/raw/ and dreams/alignment/repair/`
- `workspace/system/system_prompt.md`
- `workspace/ — other working folders`
- `.ssh/`
- `Other dot-directories and runtime files`

## Home directory — root files

- **`AGENTS.md`** — ◐ Edit via Muse

  Purpose: Muse’s operating manual for this workspace — conventions, durable lessons, and tool quirks learned here. Expected contents: workspace conventions and lessons worth keeping for future sessions. Not about the user; about how work gets done here. New entries are added only on the user’s say-so, not as a side effect of discussion.

- **`SOUL.md`** — ● Editable

  Purpose: Persona and tone — who Muse is in this instance, how it speaks, and what standards it holds itself to. Expected contents: persona description, tone guidance, and retained capabilities the user has asked Muse to keep. Changes here change how Muse presents itself, so they are user decisions.

- **`IDENTITY.md`** — ● Editable

  Purpose: Identity facts in short form. Expected contents: name, character, vibe, and signature emoji, if any. The short-form counterpart to `SOUL.md`.

- **`USER.md`** — ● Editable

  Purpose: Who the user is. Expected contents: name, what to call them, timezone, and context the user has shared about what they care about and how they work.

- **`MEMORY.md`** — ◐ Edit via Muse

  Purpose: Curated long-term memory. Expected contents: durable facts, preferences, decisions, commitments, and boundaries, organised under headings. Not a transcript, not a transaction log, and not a copy of a todo list. Routine progress and diagnostics do not belong here.

- **`PROACTIVE_PREFERENCES.md`** — ◐ Edit via Muse

  Purpose: The user’s preferences about proactive messages. Expected contents: what, if anything, Muse may surface unasked, and when. A one-time dismissal is not a permanent opt-out unless the user says so.

- **`TOOLS.md`** — ◐ Edit via Muse

  Purpose: Local tool notes. Expected contents: device names, host aliases, and environment-specific quirks that make tool use reliable in this setup. Not a skill; a local supplement to skills.

- **`HEARTBEAT.md`** — ◐ Edit via Muse _[Appears when used]_

  Purpose: Recurring checks for the heartbeat worker — one check per line, picked up on the next tick. Expected contents: a short checklist, often an empty template in a fresh instance. In instances with a heartbeat enabled, the worker runs on a regular schedule and executes this checklist. If your instance has no heartbeat, you may not see this file.

## Standard directories

<details open>
<summary><code>docs/</code> — ■ Do not edit</summary>

Purpose: Product documentation for Muse — how skills, connectors, scheduling, artifacts, and related surfaces work. Expected contents: reference documents maintained by the product team. System-provided and replaced on deployment. Read-only reference; do not edit, and do not treat it as the user’s own writing.

</details>

<details open>
<summary><code>config/</code> — ■ Do not edit _[Filesystem only]_</summary>

Purpose: Settings and runtime state for the Muse instance. Expected contents: `home.yaml` (home-level settings), `skills.yaml` (preferred skills and connectors for kinds of task), `workspace-state.json` and related state files, and runtime bookkeeping files. Contents are managed by the app and by Muse’s own settings actions, not by hand-editing.

</details>

<details open>
<summary><code>memory/</code> — ◐ Edit via Muse</summary>

Purpose: Muse’s memory store — the dated record behind the curated summary in `MEMORY.md`, plus the people and groups Muse knows about.

- **`memory/YYYY-MM-DD.md`** — ◐ Edit via Muse

  Expected contents: dated daily notes — what was learned or decided on that date, in dated form.

- **`memory/people/`** — ◐ Edit via Muse

  Pattern folder. Expected contents: `INDEX.md`, listing every person page, closest to the user first, plus one `<person>.md` file per person, holding the relationship and durable facts the user stated. No real person is named in this reference; this entry explains the pattern.

- **`memory/groups/`** — ◐ Edit via Muse

  Pattern folder, as for people. Expected contents: `INDEX.md` plus one `<group>.md` per group or community, holding the user’s role and context for that group.

- **`memory/bank/ and memory/index/`** — ■ Do not edit

  Expected contents: runtime-managed memory storage. Readable for diagnosis, never edited directly.

</details>

<details open>
<summary><code>dreams/</code> — ■ Do not edit</summary>

Purpose: Nightly self-improvement material — how Muse maintains coherence and alignment with the user over time.

- **`dreams/YYYY-MM-DD.md`** — ■ Do not edit

  Expected contents: dated self-improvement notes from nightly background processes.

- **`dreams/alignment/derived/ALIGNMENT_SYNTHESIS.md`** — ■ Do not edit

  Expected contents: a derived synthesis of how Muse and the user relate, built from past interaction by a background pass. It is a summary, not the source of truth, and it changes as new material is derived. Do not edit it as if editing it changes the underlying history.

- **`dreams/alignment/raw/ and dreams/alignment/repair/`** — ■ Do not edit

  Expected contents: raw and repair material behind the derived summaries. Runtime-managed.

</details>

<details open>
<summary><code>workspace/</code> — ● Editable</summary>

Purpose: The working area. Everything Muse creates or works on lives under here, except the root identity and memory files above.

- **`workspace/your_files/`** — ● Editable

  Expected contents: user-facing deliverables — documents, files, and project subfolders the user is meant to see and download. Files placed here show up in the Library. Project subfolders under here are a pattern (`<project>/`), not system folders.

- **`workspace/goals/<goal-slug>/`** — ◐ Edit via Muse _[Appears when used]_

  Pattern folder, one per goal. Expected contents: `GOAL.md` (Muse’s own notes on the goal, not a document for the user); `files/` (documents for the user that support that goal, written there from the first write, not copied in afterwards); `hidden_files/` (internal bookkeeping — run logs, watermarks, seen lists, source snapshots, and other state the user should not see as goal documents). The `files/` part is user-facing; `GOAL.md` and `hidden_files/` are Muse’s working notes and state.

- **`workspace/user/`** — ● Editable

  Expected contents: material the user handed Muse to keep — `files/` (uploaded or handed-over files), `media_library/` (uploaded photos and media), and `reference/` (reference documents the user asked Muse to keep). Uploads land here and persist; they do not automatically appear in the Library.

- **`workspace/custom-skills/<skill-name>/`** — ● Editable _[Appears when used]_

  Pattern folder, one per user-created skill. Expected contents: a `SKILL.md` playbook and any supporting files that skill needs.

- **`workspace/custom-connectors/custom.<provider>/`** — ◐ Edit via Muse _[Appears when used]_

  Pattern folder, one per user-created connector. Expected contents: `connector.yaml`, `CONNECTOR.md`, and helper scripts. Credentials are not stored in these files; they go through the secure connection flow.

- **`workspace/system/system_prompt.md`** — ■ Do not edit

  Expected contents: a copy of the main chat’s system prompt, saved at startup. A reference copy, not a live control — editing it does not change the running system prompt.

- **`workspace/ — other working folders`** — ■ Do not edit _[Filesystem only]_

  Expected contents: runtime and working folders for Muse’s own machinery (agents, scheduling, skills, feed, voice, and similar). Grouped here as a category, not enumerated, because they vary by deployment. Do not treat them as user projects. Project folders the user recognises belong under `your_files/` or under `goals/<goal-slug>/files/`, as above.

</details>

<details open>
<summary><code>side-chats/<chat-id>/</code> — ◐ Edit via Muse _[Appears when used]_</summary>

Pattern folder, one per side chat. The folder name is a chat ID, not a title. Expected contents: that chat’s continuity files, including its memory file and its discretion rules (what may be shared, offered, discussed, or done in that chat, including the user’s own rules for it). Side-chat titles are not listed in this reference; the point is the structure, not an inventory of chats.

</details>

<details open>
<summary><code>.ssh/</code> — ■ Do not edit _[Filesystem only]_</summary>

Purpose: Persistent SSH configuration and keys. Expected contents: SSH configuration and key pairs. Private keys live here and must never be exposed, copied into chat, memory, or ordinary files, or shared. This entry explains that the folder exists and why it is private; it does not list key contents.

</details>

- **`Other dot-directories and runtime files`** — ■ Do not edit _[Filesystem only]_

  Examples: cache, local configuration, lock files, data, hooks, prompts, and subscription state. Expected contents: runtime-managed files and folders, not user content. Grouped as a category here, not promised as an exhaustive list, because runtime folders vary by deployment.

## What this reference does not do

- Name any real person, group, project, goal, chat, uploaded file, or custom skill or connector.
- Give counts derived from one instance, or copy example contents from any real memory, people, group, daily-log, or dream file.
- Present a deployment-specific or unverified file as universal. Where universality cannot be verified, this page says “may vary by deployment” or “appears when used”.
- Present the System Files browser as if it were the whole home directory. The browser is a window into the filesystem, and some areas are filesystem-only, as flagged above.

End of generic reference. For a personal version with your own projects and goals, use the personal page built from the same tree, kept private and unpublished.

<!-- Generated from muse-system-files-reference.html by generate_reference_md.py. Do not hand-edit the tree entries; regenerate instead. -->