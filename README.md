# Hackathon 2026 — Help

Ask your questions here by raising an issue. **Read this FAQ first**

## Before you ask: the 60-second checklist
1. Did you **accept the org invite** email? Check spam. (Sent from GitHub, subject "You've been invited to join the ewfx organization".)
2. Does `https://github.com/ewfx/hack26-<your-github-username>` load for you and show your repo?
3. Did you already push the required `ACCESS_CHECK.md` commit during the access-check window? If write access is broken, that's the fastest way to confirm it.
4. Are you using **your own GitHub account's credentials** to push (not an old cached token)? See "Push/write access" below.

If none of that resolves it, raise an issue with the template below.

## Repo access

| Step | What happens |
|---|---|
| Registration | You give us your GitHub **username** (not just email) |
| Invite | You get an org invite email — accept it (read access to your own repo only) |
| Repo creation | We create `ewfx/hack26-<your-username>` from the template and add you as a **collaborator with push access** directly — no team "request to join" step this year |
| Access check window | Push a small commit (e.g. edit `ACCESS_CHECK.md`) so we can confirm write access *before* event day |
| Event day | Build in your repo |
| Code freeze | Your access is switched to **read-only** at the announced freeze time |
| Demo grace window | You may still edit `artifacts/demo/DEMO.md` for 30 minutes after freeze to add your demo link — nothing else |

### Push/write access
"git push" returning 403, or no repo showing up under your account, is almost
always one of:
- **You haven't accepted the invite yet.** Check github.com/settings/organizations or the invite email again (including spam).
- **Wrong GitHub account.** Make sure you're pushing with the same GitHub account whose username you registered with — check `git config user.name`/credential manager, or push over HTTPS with a fresh Personal Access Token if in doubt.
- **You're trying to push after code freeze.** Access is read-only by design at that point — see the demo grace window above for the one exception.

We cannot debug local git/IDE configuration issues for you individually
during the event — a quick search usually resolves auth issues faster than
waiting for a reply. We *can* fix org-side access problems (missing invite,
wrong permission level, repo not created) — raise an issue for those.

## Problem statements
Problem statements and their prefixes are announced at kickoff (event day,
hour 0) — see the org profile page and the announcement channel. Once
announced, put your chosen prefix in `submission.yaml` at your repo root.
**Repos are not renamed** — your repo name (`hack26-<username>`) stays fixed regardless of
which problem statement you pick.

## Demo videos
- Keep it to 2-3 minutes.
- Prefer an **unlisted YouTube link** or a **Loom link**. Avoid Google Drive
  links — reviewers have hit access/corporate-network issues with them in
  the past.
- Put the link in `artifacts/demo/DEMO.md`. You may add/edit this one file
  for 30 minutes after code freeze.

## Sample data
If a problem statement includes sample data, it will be linked from the
problem-statement announcement. **Do not commit real personal data anywhere
in your repo** — the evaluator specifically scans for it (see the submission
checklist in your repo's README) and it will cost you points even if it's
"just test data" from a real source. Use synthetic/generated data instead.

## Evaluation
Submissions are scored by an automated, deterministic script — no GenAI/LLM
judges your code. It checks things like artifact completeness, security,
dependency vulnerabilities, PII handling, code structure, and whether your
app actually builds and runs, alongside basic code-quality signals. The
exact scoring thresholds aren't published, but the categories being scored
are described in your repo's submission checklist. The top-ranked
submissions from the auto-score are then judged live by a human panel at
the finale.

## Still stuck?
Raise an issue using the "Help request" template. Include your GitHub
username and repo URL — we can't help without them.
