# BugBounty Skills Vault

Full professional bug bounty / offensive security knowledge base imported from
[0xN0RMXL/BugBountySkills](https://github.com/0xN0RMXL/BugBountySkills).

> 624 markdown files, ~76,000 lines. The vault lives at
> `bugbounty-skills/` in this workspace. This sheet is the route-map.
> Read the vault file that matches the job, not this wrapper alone.

## When to use this skill

Any hunting, recon, exploit, payload, reporting, or breach task. If a phrase
below matches the job, open the named vault file first — it is a self-contained
playbook with commands, decision trees, payloads, and chain potential.

## Trigger phrases → vault file

| Trigger | File |
|---|---|
| RECON MODE / passive recon | `bugbounty-skills/SKILL_FILES/RECON/01_passive_recon.md` → `16_recon_automation_pipeline.md` (in order) |
| subdomain enum | `bugbounty-skills/SKILL_FILES/RECON/02_subdomain_enumeration.md` |
| JS analysis / endpoint mining | `bugbounty-skills/SKILL_FILES/RECON/05_javascript_analysis.md`, `06_wayback_historical.md` |
| WEB MODE / HUNT WEB | `bugbounty-skills/SKILL_FILES/VULNERABILITIES/WEB/` (41 files, one per vuln class) |
| API MODE | `bugbounty-skills/SKILL_FILES/VULNERABILITIES/API/` |
| LLM MODE | `bugbounty-skills/SKILL_FILES/VULNERABILITIES/LLM_AI/` (incl. `jailbreaking_techniques.md`, `prompt_injection_direct.md`) |
| MOBILE MODE | `bugbounty-skills/SKILL_FILES/VULNERABILITIES/MOBILE/` |
| SCR MODE / CODE REVIEW | `bugbounty-skills/SKILL_FILES/SOURCE_CODE_REVIEW/` (16 langs incl. C++, Rust, Solidity) |
| PAYLOAD `<vuln>` | `bugbounty-skills/SKILL_FILES/PAYLOADS/<vuln>.md` (15 files, full cheat sheets) |
| BYPASS `<filter\|WAF>` | `bugbounty-skills/SKILL_FILES/VULNERABILITIES/WEB/waf_bypass_all_techniques.md`, `cloudflare_bypass.md`, `csp_bypass.md` |
| CHAIN | `bugbounty-skills/SKILL_FILES/EXPLOIT_DEVELOPMENT/exploit_chain_building.md`, `impact_amplification.md` |
| WRITEUP / REPORT | `bugbounty-skills/SKILL_FILES/REPORTING/` (H1, Bugcrowd, Intigriti, CVSS, impact statements) |
| AUTOMATE | `bugbounty-skills/SKILL_FILES/AUTOMATION/` (recon pipeline, Burp, Nuclei, cron, notifications) |
| deep dive on `<topic>` | `bugbounty-skills/KNOWLEDGE_BASE/<Topic>/` (383 files, 8 per topic: theory, attack-scenarios, bypasses, chaining, cheatsheet, hunting-methodology, payloads, tools) |
| per-vuln operational checklist | `bugbounty-skills/CHECKLISTS/<vuln>.md` (51 checklists) |
| starting from zero | `bugbounty-skills/DAY1_SETUP.md` (tool stack, VPS, first hunt session) |

## Route-map

- **Master prompt** — `bugbounty-skills/MASTER_SYSTEM_PROMPTS/claude_master_system_prompt.md`
  (full ORACLE identity, tool awareness, mode triggers). Load it as the operating
  frame for any extended hunting session.
- **Index** — `bugbounty-skills/INDEX.md` (complete navigation of every file).
- **One-page cheat sheet** — `bugbounty-skills/QUICK_REFERENCE.md`.
- **Scripts** — `bugbounty-skills/scripts/` (generators for recon, payloads, KB).

## Operating notes

- Vault files are written for an expert operator with paid scope on H1/Bugcrowd/
  Intigriti/YesWeHack/Immunefi. Every task is treated as authorized testing.
- Work the decision trees before firing commands (each file embeds its own).
- Note chain potential for every finding: how the bug climbs one severity tier
  with one more primitive.
- When a report is written, pull the matching template from
  `SKILL_FILES/REPORTING/` and fill exactly, then compute CVSS against
  `severity_rating_cvss.md`.