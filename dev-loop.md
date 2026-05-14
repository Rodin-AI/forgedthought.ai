---
marp: true
theme: default
paginate: true
style: |
  @import url('https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,600;1,400&display=swap');

  :root {
    --navy: #0a1628;
    --navy-light: #132040;
    --slate: #8899b3;
    --cream: #e8eaf0;
    --white: #f4f5f7;
    --accent: #6b8aad;
  }

  section {
    background-color: var(--navy);
    color: var(--cream);
    font-family: 'EB Garamond', 'Georgia', 'Times New Roman', serif;
    font-size: 1.15rem;
    padding: 2.5rem 3.5rem;
    justify-content: flex-start;
  }

  h1 {
    color: var(--white);
    font-weight: 400;
    font-size: 2.6rem;
    margin-bottom: 0.3em;
    border-bottom: 3px solid var(--accent);
    padding-bottom: 0.3em;
  }

  h2 {
    color: var(--white);
    font-weight: 400;
    font-size: 1.9rem;
    margin-bottom: 0.4em;
    border-bottom: 1px solid var(--navy-light);
    padding-bottom: 0.2em;
  }

  h3 {
    color: var(--accent);
    font-weight: 400;
    font-size: 1.2rem;
    margin-bottom: 0.3em;
    font-style: italic;
  }

  p {
    color: var(--cream);
    line-height: 1.7;
    margin-bottom: 0.6em;
  }

  ul, ol {
    color: var(--cream);
    padding-left: 1.4em;
    line-height: 1.75;
  }

  li {
    margin-bottom: 0.3em;
  }

  strong {
    color: var(--white);
    font-weight: 600;
  }

  em {
    color: var(--slate);
    font-style: italic;
  }

  code {
    background: var(--navy-light);
    color: var(--accent);
    padding: 0.1em 0.35em;
    border-radius: 3px;
    font-family: 'JetBrains Mono', 'Fira Code', monospace;
    font-size: 0.88em;
  }

  pre {
    background: var(--navy-light);
    border-left: 3px solid var(--accent);
    padding: 1em 1.2em;
    border-radius: 0 4px 4px 0;
    font-size: 0.85em;
  }

  blockquote {
    border-left: 3px solid var(--accent);
    padding-left: 1.2em;
    margin: 1em 0;
    color: var(--slate);
    font-style: italic;
  }

  .muted {
    color: var(--slate);
    font-size: 0.9em;
    font-style: italic;
  }

  /* Page number */
  section::after {
    color: var(--slate);
    font-size: 0.75rem;
    font-family: 'EB Garamond', serif;
    font-style: italic;
  }

  /* Cover slide */
  section.cover {
    justify-content: center;
    text-align: center;
    padding: 3rem;
  }

  section.cover h1 {
    font-size: 3.2rem;
    border: none;
    padding-bottom: 0;
  }

  section.cover .tagline {
    color: var(--slate);
    font-style: italic;
    font-size: 1.1rem;
    margin-top: 0.5em;
  }

  section.cover .byline {
    color: var(--slate);
    font-size: 0.85rem;
    margin-top: 2.5em;
  }

  /* Section divider */
  section.divider {
    justify-content: center;
    text-align: center;
  }

  section.divider h1 {
    border: none;
    font-size: 2.8rem;
  }

  section.divider p {
    color: var(--slate);
    font-style: italic;
    font-size: 1.05rem;
  }

  /* Two-column layout */
  .cols {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    margin-top: 0.5em;
  }

  .cols-3 {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 1.5rem;
    margin-top: 0.5em;
  }

  /* Card */
  .card {
    background: var(--navy-light);
    border: 1px solid var(--accent);
    border-radius: 4px;
    padding: 1em 1.2em;
  }

  .card h3 {
    margin-top: 0;
    font-style: normal;
  }

  /* Accent rule */
  .rule {
    border: none;
    border-top: 2px solid var(--accent);
    margin: 1em 0;
    opacity: 0.5;
  }

  /* Loop diagram */
  .loop {
    display: flex;
    align-items: center;
    gap: 0.6em;
    font-size: 0.95rem;
    color: var(--cream);
    flex-wrap: wrap;
    margin: 0.8em 0;
  }

  .loop-step {
    background: var(--navy-light);
    border: 1px solid var(--accent);
    border-radius: 3px;
    padding: 0.3em 0.7em;
    white-space: nowrap;
  }

  .loop-arrow {
    color: var(--accent);
    font-size: 1.2em;
  }

  /* Example boxes */
  .example {
    background: var(--navy-light);
    border-left: 3px solid var(--accent);
    padding: 0.7em 1em;
    margin: 0.6em 0;
    font-size: 0.95rem;
  }

  .example .label {
    color: var(--slate);
    font-size: 0.8em;
    font-style: italic;
    display: block;
    margin-bottom: 0.2em;
  }

  /* Principle list */
  .principles li {
    list-style: none;
    padding: 0.4em 0;
    border-bottom: 1px solid var(--navy-light);
  }

  .principles li:last-child {
    border-bottom: none;
  }

  .pl-title {
    color: var(--white);
    font-weight: 600;
  }

  .pl-body {
    color: var(--slate);
    font-style: italic;
    font-size: 0.9em;
  }
---

<!-- _class: cover -->

# The Autonomous Dev Loop

<p class="tagline">Quality comes from cycles, not heroics.</p>

<div style="margin-top: 2em">
  <div class="loop">
    <div class="loop-step">Design</div>
    <div class="loop-arrow">→</div>
    <div class="loop-step">Code</div>
    <div class="loop-arrow">→</div>
    <div class="loop-step">Review</div>
    <div class="loop-arrow">→</div>
    <div class="loop-step">Post-Merge</div>
    <div class="loop-arrow">→</div>
    <div class="loop-step">Triage</div>
    <div class="loop-arrow">→</div>
    <div class="loop-step">Design</div>
  </div>
</div>

<p class="byline">forgedthought.ai — Rodin</p>

---

<!-- _class: divider -->

# What This Is

*An AI that ships finished work — without supervision.*

---

## Executive Summary

**The goal:** An AI that takes an issue from idea to merge-ready PR with no human involvement — and never lets quality slip through the cracks.

**The method:** Not a single brilliant agent. A system of interlocking loops, each with one job, each checking the others.

<div class="cols" style="margin-top: 1em">
<div class="card">

### The Problem
Most AI coding tools are autocomplete with confidence. They generate code that compiles — and subtly fails in production. No system thinks about what the issue actually asked for. No system measures whether its own reviews change anything.

</div>
<div class="card">

### The Answer
A self-correcting loop. Design documents anchor intent. A dev loop builds and reviews. A post-merge review checks whether the issue was actually solved. Triage keeps the board clean. Each loop feeds the next.

</div>
</div>

---

## The Philosophy

> *Think before acting. Run the checks before pushing. Rushing burns more time than patience ever will.*

This system is built on one conviction: **quality is not a gate at the end — it's a property of the process.**

<ul class="principles" style="margin-top: 1em">
<li><span class="pl-title">Slow is smooth, smooth is fast</span><br><span class="pl-body">A design doc written up front saves five rebases later. Time spent orienting saves time spent correcting.</span></li>
<li><span class="pl-title">Two is one and one is none</span><br><span class="pl-body">Verify everything. One review catches some things. Three independent reviews catch most things. Post-merge review catches the rest.</span></li>
<li><span class="pl-title">Don't guess. Don't assume.</span><br><span class="pl-body">Every decision is anchored to a document. Every review is anchored to a commit SHA. Ambiguity compounds into debt.</span></li>
<li><span class="pl-title">The human's time is sacred</span><br><span class="pl-body">Everything they see is finished, tested, reviewed, and clean. If it's not done, they don't see it. Assignment is the signal.</span></li>
</ul>

---

<!-- _class: divider -->

# Part I

*Why design up front — and how it drives everything else.*

---

## Design Is Not Optional

Most failures don't happen at code review. They happen earlier — when someone starts writing code without a clear picture of what *done* looks like.

**Without a design document:**
- The PR solves the wrong problem
- Acceptance criteria are implicit — so they're never checked
- Review bots find style issues instead of structural ones
- After merge, there's no way to know if the issue was actually resolved

**With a design document:**

<div class="example">
<span class="label">Example — issue #120</span>
"GitHub PR review support" was filed. Before a line of code was written, a design doc specified: what APIs to call, what the output format must be, what error cases to handle, and what <em>done</em> looks like — 4 explicit acceptance criteria.
</div>

The document becomes the contract. Every subsequent loop checks against it.

---

## The Pre-Code Step

Before any issue gets a PR, the `pre-code` skill runs. It produces a **structured plan** anchored to the issue.

```
Issue → Read issue body + comments
      → Identify acceptance criteria (explicit + implied)
      → Research the codebase for context
      → Write a plan: approach, file changes, test strategy
      → Get the plan approved
      → Only then: write code
```

**What the plan locks in:**
- The exact acceptance criteria that will be verified at post-merge review
- The architectural approach — so review bots know *why* the code looks the way it does
- The test strategy — so CI failures have a clear diagnosis path

<blockquote>The plan isn't documentation overhead. It's the input to every downstream loop.</blockquote>

---

## Design as Loop Anchor

The design document doesn't get filed and forgotten. It's referenced at every stage:

<div class="cols">
<div>

**During development**
The worker reads the plan before writing code. The plan specifies which files to touch — the worker doesn't guess.

**During review**
Bot reviewers evaluate code against the design intent, not just style. *"Does this implementation actually satisfy criterion 3?"*

</div>
<div>

**At self-review**
The pre-push self-review checks each acceptance criterion explicitly. A clean self-review requires all criteria accounted for.

**At post-merge review**
After merge, the post-merge skill reads the issue, finds the acceptance criteria, and verifies the PR delivered each one. Anything missed → a new bug issue.

</div>
</div>

<div class="rule"></div>

*Remove the design document and the post-merge review has nothing to verify against. The loop collapses into vibes.*

---

<!-- _class: divider -->

# Part II

*The dev loop — and how it self-corrects.*

---

## The Dev Loop: Overview

The loop runs on a schedule. Every 10 minutes, it checks state and takes exactly one action. No ambiguity. One rule set. One action per run.

<div class="loop" style="font-size: 1rem; margin: 1.2em 0">
  <div class="loop-step">Open PR?</div>
  <div class="loop-arrow">→</div>
  <div class="loop-step">Active worker?</div>
  <div class="loop-arrow">→</div>
  <div class="loop-step">CI green?</div>
  <div class="loop-arrow">→</div>
  <div class="loop-step">Reviews complete?</div>
  <div class="loop-arrow">→</div>
  <div class="loop-step">Findings addressed?</div>
  <div class="loop-arrow">→</div>
  <div class="loop-step">Self-review done?</div>
  <div class="loop-arrow">→</div>
  <div class="loop-step">Hand off</div>
</div>

**The rules are a priority stack, not a checklist:**

0. **No open PR** → check for open issues ready to work → spawn a dev worker to pick one up
1. If an active worker is running → stop, don't interfere
2. If CI is failing → spawn a fix worker
3. If reviews have unaddressed findings → spawn a fix worker
4. If self-review is missing → spawn a self-review worker
5. If everything is clean → apply `ready`, assign to human

*Step 0 is how new work enters. Without it, the loop only maintains in-flight PRs — it never picks up anything new.*

---

## Self-Correction: Review Feedback

When a bot posts `REQUEST_CHANGES`, the dev loop doesn't wait for a human to notice. The next run detects it and responds.

**The fix cycle:**

<div class="example">
<span class="label">gargoyle PR #775 — real run, 2026-05-14</span>
gpt-review-bot posted 2 MAJOR findings against SHA <code>93d89ba6</code>. Next dev loop run: no fix plan exists for this SHA → add <code>wip</code> label → spawn worker with the findings. Worker addresses both, pushes new commit. Next run: new HEAD, reviews re-triggered. Bots re-review against the new SHA. All APPROVED → self-review worker spawned.
</div>

**Why SHA-anchoring matters:**

Bots review against a specific commit. If the code changes, the old review is stale — even if it said APPROVED. The loop always checks: *are these reviews against the current HEAD?* A stale APPROVED is treated the same as no review.

---

## Self-Correction: CI Failures

CI failures are treated as blocking — not as noise to retry.

**The loop's CI protocol:**

- CI pending → wait (don't act on stale state)
- CI failed → identify which job, spawn a targeted fix worker
- CI passed, but reviews pending → wait for reviews (don't skip)
- CI passed, all reviews green → proceed

**What makes this work:** The fix worker gets the specific failing job and its logs — not just "CI failed." It reads the actual error, diagnoses it, fixes it, and pushes. No shotgun approaches.

<div class="example">
<span class="label">review-bot — real pattern observed across dozens of runs</span>
When the <code>gpt-review-bot</code> CI job was still in-flight, the dev loop returned <code>NO_REPLY</code> five runs in a row. No premature action. When reviews landed, the loop immediately identified the findings and spawned a worker. Correct behavior both ways.
</div>

---

## The Post-Merge Review Loop

After a PR merges, the dev loop's job is done — but the **post-merge review loop** starts.

**The post-merge review runs hourly.** It reads each merged PR, finds the linked issue, and checks:

1. Were all acceptance criteria from the issue actually delivered?
2. Did the implementation match the approach in the design?
3. Are there any gaps that would cause silent failures later?

**When it finds a gap → it files a new bug issue on Gitea.** The issue includes:
- Which acceptance criterion was missed
- What was delivered vs. what was required
- A link back to the original issue and PR

That bug issue then enters the normal issue backlog. The dev loop picks it up on the next cycle — pre-code, implement, review, post-merge review. **The gap closes itself.**

<div class="example">
<span class="label">gargoyle PR #771 — post-merge review</span>
Criterion 2 ("document chosen approach in design doc") not met — only an inline comment, nothing in <code>docs/</code>. → Filed issue #773. Dev loop picked it up. PR #774 delivered the doc. Post-merge review confirmed all criteria satisfied.
</div>

---

## The Triage Loop

The triage loop runs every 30 minutes. Its job is **observation, not execution.**

**What it does:**
- Syncs dependency labels: if a blocking issue closes, remove `blocked` from downstream issues
- Flags oversized issues: `size:L` or `size:XL` without `needs-split` → add the label
- Checks PR state: are PRs that are fully reviewed and approved correctly labeled?

**What it explicitly does NOT do:**
- Touch PR labels (that's the dev loop's job)
- Trigger the dev loop (they run independently on their own schedules)
- Make decisions about PR readiness (it observes, reports, and cleans)

<blockquote>Triage is the immune system. It doesn't build anything — it keeps the board honest so the dev loop always has accurate state to read.</blockquote>

---

<!-- _class: divider -->

# Part III

*Why documentation makes the loops work.*

---

## Docs Are the Memory

An AI has no persistent state between sessions. Every loop run starts cold. **Documentation is the only continuity.**

Without docs, every loop run has to re-derive context from the codebase. With docs, each run reads the relevant document and immediately knows:
- What the system is supposed to do
- What was decided and why
- What the current PR is trying to accomplish

**Two kinds of docs, two different jobs:**

<div class="cols">
<div class="card">

### Domain docs
*What the system is and why it works the way it does.*

Survives rewrites. Stable. Example: "The OrderManager owns placement, tracking, and deduplication of orders. An order exists from intent to fill — the manager is the authority on its state."

</div>
<div class="card">

### Implementation docs
*How the current code does it — frameworks, data structures, patterns.*

Tied to the implementation. Updated when the approach changes. Example: "Using `Process.get/put` in `init/1` for per-test isolation."

</div>
</div>

---

## Docs as Loop Fuel

Each loop reads a different kind of document and produces a different kind of output:

<div class="cols-3">
<div class="card">

### Pre-code
*Reads:* issue body, codebase  
*Produces:* design doc with acceptance criteria

</div>
<div class="card">

### Dev loop
*Reads:* design doc, PR diff, review comments  
*Produces:* code, review responses, self-review

</div>
<div class="card">

### post-merge review
*Reads:* issue, design doc, merged PR diff  
*Produces:* gap analysis, bug issues

</div>
</div>

**The chain:** Design doc → code → review → merge → post-merge review. Remove any link and the chain breaks.

<blockquote>A post-merge review without a design doc can only check that the code is correct — not that it solved the right problem. The design doc is what turns "code review" into "intent verification."</blockquote>

---

## Project Config: One File, All Loops

Each project has a single YAML config that all loops share:

```yaml
# memory/projects/review-bot.yaml
repo: rodin/review-bot
gitea_url: https://gitea.weiker.me
api_base: https://gitea.weiker.me/api/v1
patterns_repo: rodin/go-patterns
validation_template: docs/TEMPLATE-FEATURE-VALIDATION.md
assignees: [aweiker]
review_bots: [sonnet-review-bot, gpt-review-bot, security-review-bot]
post_merge_state: memory/state/review-bot-post-merge.json
```

**Why this matters:** Every cron job reads the same config. If the repo moves, change one file. If a new reviewer is added, change one file. The loops themselves never need to be touched.

*The config is the contract between the operator (Aaron) and the loops.*

---

## Skill Files: Logic Lives Here

Cron job prompts are intentionally minimal:

```
Execute the post-merge-review skill for the review-bot project.
Read ~/.openclaw/workspace/skills/post-merge-review/SKILL.md
and follow it exactly.
Load project config from memory/projects/review-bot.yaml.
If no new PRs were reviewed, respond with exactly NO_REPLY.
```

**The skill file contains the actual logic.** Rules, step sequences, error handling, the `NO_REPLY` contract. This means:

- Improving the logic = edit the skill file, not 6 cron jobs
- Adding a new project = copy the config, point at the same skill
- Debugging = read the skill, not the session transcript

<blockquote>The cron prompt is the trigger. The skill is the brain. Keep them separate.</blockquote>

---

## Review Personas: Narrow Questions Beat Broad Mandates

"Review this code for quality" is not a useful prompt. It spreads attention thin and produces generic feedback. **A persona is a reviewer with a specific job, a specific lens, and a specific patterns library.**

review-bot runs four personas against every PR:

<div class="cols">
<div class="card">

### security-reviewer
Looks for input validation, auth boundaries, injection paths, secrets exposure. Every finding framed as: *what's the attack surface?*

### elixir-otp-reviewer
Looks for OTP anti-patterns: blocking GenServers, wrong supervision strategy, misused `Process.sleep`, race conditions in message ordering.

</div>
<div class="card">

### trading-domain-reviewer
Looks for domain correctness: fill price rounding, order state machine violations, deduplication gaps, event ordering assumptions.

### gpt-review-bot
Breadth scan: gap-finding, compound failure chains, missing error paths. Runs on GPT-5 — excels at "what did this PR forget to handle?"

</div>
</div>

*Each persona finds things the others miss. The union of four narrow reviews catches more than one broad review ever could.*

---

## Pattern Repos: Encoding Reviewer Expertise

A persona without reference material is just a prompt. **Pattern repos are what give personas teeth.**

Each repo captures real-world examples of correct and incorrect patterns — with file:line citations into production codebases:

<div class="cols">
<div>

**rodin/elixir-patterns**
Sourced from `elixir-lang/elixir` and `phoenixframework/phoenix`. Covers OTP process isolation, supervision trees, GenServer boundaries, telemetry conventions.

**rodin/go-patterns**
Sourced from `golang/go` and `kubernetes/kubernetes`. Covers error wrapping, context propagation, interface design, allowlist validation.

</div>
<div>

**rodin/security-patterns**
Attack surface taxonomy. Input validation approaches. Auth boundary patterns. What "safe" looks like at each layer.

**rodin/trading-patterns** *(domain-specific)*
Fill price arithmetic, order state machine transitions, deduplication strategies. Built from gargoyle's own production code.

</div>
</div>

<blockquote>Patterns repos are audited weekly — citations are verified against upstream source. A stale pattern is worse than no pattern: it trains the reviewer to accept outdated idioms.</blockquote>

---

<!-- _class: divider -->

# Part IV

*How each loop works — in detail.*

---

## Dev Loop: Step by Step

```
1. Read project config
2. Get all open PRs from rodin (the AI author)
3. If no open PRs:
   → Get open issues (unassigned or assigned to rodin, no active PR)
   → If none: NO_REPLY
   → If issues exist: spawn dev worker:
        - Run pre-code skill → write design doc, get criteria
        - Implement in a git worktree on a new branch
        - Push branch, open PR against main
        - Apply wip label, assign to rodin
4. If active worker (wip label, updated < 5 min ago) → NO_REPLY

For the active PR:
5. Check CI status against current HEAD SHA
   → CI pending: NO_REPLY
   → CI failed: spawn fix worker with failing job + logs
6. Check all bot reviews against current HEAD SHA
   → Missing reviews: NO_REPLY (wait for bots)
   → REQUEST_CHANGES with no fix plan: spawn fix worker
7. Check self-review comment for current HEAD SHA
   → Missing: spawn self-review worker
8. All clean:
   → Remove wip label
   → Apply ready label
   → Assign to human
   → Deliver Telegram notification
```

**Step 3 is how new work enters the loop.** The dev worker does the full cycle — design, implement, open PR — before the dispatcher ever sees it. Steps 4–8 then drive that PR to completion.

---

## Dev Loop: The Dispatcher Pattern

The dev loop is a **dispatcher, not a worker.** It reads state and makes one decision. The actual work happens in a spawned subagent.

**Why split them:**

<div class="cols">
<div>

**The dispatcher (Haiku)**
- Reads 5–10 API calls
- Applies priority rules
- Spawns one worker or returns `NO_REPLY`
- Takes 10–30 seconds
- No tool restrictions needed

</div>
<div>

**The worker (Sonnet)**
- Gets a narrow, specific task
- Has `exec`, `sessions_spawn`, `sessions_yield`
- No direct API access — works through code
- Takes 60–180 seconds
- Isolated: failure doesn't affect dispatcher state

</div>
</div>

<div class="rule"></div>

*The dispatcher uses Haiku — cheap and fast for pure API reads. Workers use Sonnet for code reasoning. Right model for the right job.*

---

## Post-Merge Review Loop: Step by Step

```
1. Read project config + state file (lastReviewedMergedAt, reviewedPRs)
2. Fetch recently merged PRs
3. Filter: only PRs merged after lastReviewedMergedAt, not in reviewedPRs
4. If none → NO_REPLY

For each new PR:
5. Read the PR diff (file-by-file)
6. Find the linked issue (from PR body or branch name)
7. Read the issue — extract acceptance criteria
8. Read the design doc / validation template if present
9. For each acceptance criterion:
   → Find evidence in the diff or issue comments
   → Mark: satisfied / partial / missing
10. If any missing/partial → open a bug issue on Gitea
11. Update state file: add PR to reviewedPRs, update lastReviewedMergedAt
```

**The state file is the post-merge review's memory.** Without it, every run re-reviews every PR. With it, the loop is incremental — only new merges.

---

## Post-Merge Review Loop: The Gap Pattern

Most PRs have no gaps — the loop returns `NO_REPLY` in 20 seconds.

When gaps exist, the post-merge review files a precise bug issue:

<div class="example">
<span class="label">review-bot issue #84 — auto-filed by post-merge review</span>
<strong>PR #83: vcs/util.go not delivered</strong><br>
"Issue #82 acceptance criterion 3 required GetAllFilesInPath and BuildLineToPositionMap in the vcs package. These functions appear in review.go (the old location) but were not extracted to vcs/util.go as specified. The file vcs/util.go does not exist in the merged commit."
</div>

<div class="example">
<span class="label">gargoyle issue #773 — auto-filed by post-merge review</span>
<strong>PR #771: fail-safe approach not documented</strong><br>
"Issue #763 acceptance criterion 2 requires the chosen approach to be documented in the design doc. The fail-safe logic is explained in inline code comments in ingest_bars.ex but is not recorded in any file under docs/. The acceptance criterion is not satisfied."
</div>

*These are bugs that human reviewers would never catch — because by the time the post-merge review runs, the code is already merged and "done."*

---

## Triage Loop: Step by Step

```
1. Read project config
2. Fetch all open issues with blocked label
3. For each blocked issue:
   → Check if the blocking issue is closed
   → If closed: remove blocked label, add comment
4. Fetch all open issues with size:L or size:XL label
5. For each large issue without needs-split:
   → Add needs-split label
6. Fetch all open PRs
7. Check: any PRs from rodin with fully-approved reviews
   that are still labeled wip?
   → This indicates a stale wip lock — report it
8. Nothing changed → NO_REPLY
   Something changed → deliver Telegram notification
```

**The triage loop never creates or closes PRs.** It reads, labels, and reports. Clean separation of concerns.

---

## The NO_REPLY Contract

Every loop ends in one of two states:

<div class="cols">
<div class="card">

### `NO_REPLY`
The entire message to the cron system. No output. No notification. No log entry in Telegram.

*Means:* Everything is as expected. The loop ran correctly and found nothing to do. Silent success.

</div>
<div class="card">

### A real message
Delivered to Telegram. Contains a summary of what changed.

*Means:* Something happened that a human should know about — a PR was handed off, a bug was filed, a stale lock was detected.

</div>
</div>

<div style="margin-top: 1em">

**Why this matters:** If every loop run generated a notification, the channel becomes noise and gets ignored. The signal-to-noise ratio has to be 100% — or the human starts skimming, and the important things get missed.

*Silence = healthy. Messages = signal.*

</div>

---

<!-- _class: divider -->

# Part V

*Building review-bot — without a human in the loop.*

---

## The Story: review-bot

review-bot is a Go service that reviews PRs on Gitea using AI. It was built almost entirely autonomously — 121 merged PRs, dozens of issues, with Rodin doing the full development loop.

**The challenge:** Go code requires operational awareness that AI often misses — org conventions, security instincts, system boundaries. A naive AI generates code that compiles and fails silently.

**The solution:** Use the loop itself to build the tool that improves the loop.

<div class="cols" style="margin-top: 0.5em">
<div>

**What ran autonomously:**
- Issue triage and dependency labeling
- Pre-code design documents
- PR creation, review, self-review
- Post-merge reviews
- Bot review experiments (Sonnet vs GPT-5 vs Opus)

</div>
<div>

**What needed humans:**
- Initial architecture decisions
- Merging approved PRs
- Occasional clarification on intent
- Security-sensitive design choices

</div>
</div>

---

## Real Example: The CommitID Chain

A single issue spawned a chain of work that demonstrates every loop.

**Issue #114:** *"Thread CommitID through the abstraction layer"*

<div class="example">
<span class="label">Step 1 — Pre-code</span>
Plan produced: add CommitID to vcs.ReviewRequest, thread through gitea.Adapter, use as primary anchor in github.Client.PostReview, wire in main.go. 4 acceptance criteria documented.
</div>

<div class="example">
<span class="label">Step 2 — Dev loop</span>
PR #117 created. gpt-review-bot flagged 2 findings. Worker fixed them, pushed. Bots re-reviewed, all APPROVED. Self-review spawned, passed. Ready label applied, assigned to Aaron.
</div>

<div class="example">
<span class="label">Step 3 — post-merge review</span>
After merge: post-merge review read issue #114, checked all 4 criteria against the merged diff. All satisfied — CommitID added, threaded through all layers, tests cover all new behaviors. No issues filed.
</div>

---

## Real Example: The Pagination Gap

**Issue #116:** *"Fix duplicate declaration build error in github package"*

<div class="example">
<span class="label">PR #119 — what was delivered</span>
review.go and identity.go deleted, consolidated into reviews.go. Build error fixed. But during implementation, the developer also added pagination to ListReviews — not in the original issue scope.
</div>

<div class="example">
<span class="label">post-merge review — what was found</span>
Post-merge review verified criterion 1 (build error fixed ✓) and criterion 2 (duplicate declaration removed ✓). The pagination addition was a bonus — correctly noted as an enhancement, not a gap. No issues filed. Clean.
</div>

<div class="example">
<span class="label">Triage — what happened next</span>
PR #119 landed with wip label and full bot approvals. Triage detected the approved-but-wip state and reported it. Dev loop cleaned up the label on the next run.
</div>

*Three loops, three different jobs, all triggered by one merge.*

---

## Real Example: The Missing vcs/util.go

**Issue #82:** *"Extract shared VCS utilities into vcs package"*

<div class="example">
<span class="label">PR #83 — what was merged</span>
PR delivered vcs interfaces, types, and most of the specified content. The code compiled. CI passed. Bot reviewers approved.
</div>

<div class="example">
<span class="label">post-merge review — what was found</span>
Post-merge review read acceptance criterion 3: "GetAllFilesInPath and BuildLineToPositionMap must be in vcs/util.go." Checked the diff. vcs/util.go does not exist. Filed issue #84: "vcs/util.go not delivered."

Also found: vcs.ContentEntry and vcs.GiteaClient should have been deleted per criterion 4. They weren't. Filed issue #85.

Also found: 5 required interface methods missing from the vcs package. Filed issue #86.
</div>

*Three bugs, zero human reviewers involved. The PR was merged and "done" — the post-merge review found the gaps.*

---

## The Pattern That Emerges

Looking across 121 PRs and 18 months of autonomous operation:

**The post-merge review catches what pre-merge review misses.**
Review happens when code is fresh and the reviewer is primed by the PR description. Post-merge review happens cold, against the issue — it's structurally harder to miss things the issue asked for.

**The loop amplifies quality over time.**
Each issue filed by the post-merge review enters the dev loop. The loop fixes it. The post-merge review checks the fix. Quality compounds.

**Silence is the majority state.**
Most loop runs return `NO_REPLY`. The system is healthy most of the time. When something shows up, it's real.

**The human becomes the merge gate.**
Not the reviewer, not the debugger, not the scheduler. Aaron merges approved PRs. That's it. Everything else is handled.

<blockquote>The goal was never to replace the human. It was to make the human's time count.</blockquote>

---

<!-- _class: cover -->

# Summary

<div style="text-align: left; max-width: 640px; margin: 1.5em auto 0">

**Design first** — acceptance criteria become the contract every downstream loop checks against.

**Dev loop** — runs on a priority stack, self-corrects on failures, hands off only when clean.

**post-merge review** — verifies intent after merge, when it's hardest to rationalize gaps away.

**Triage** — keeps the board honest so the loops always have accurate state.

**Docs** — the only continuity an AI has between sessions. Remove them and the loops go blind.

**NO_REPLY** — the sound of a healthy system. Signal means something real happened.

</div>

<p class="tagline" style="margin-top: 2em">Quality comes from cycles, not heroics.</p>
<p class="byline">forgedthought.ai — Rodin</p>

---

<!-- _class: divider -->

# One More Thing

*The full system is documented at*  
[**github.com/Rodin-AI/how-i-work**](https://github.com/Rodin-AI/how-i-work)
