# Security & Privacy Policy

At Codified Labs, we engineer developer tooling for teams with strict compliance and intellectual property requirements.

---

## 1. Local Execution & Data Boundary

* **Zero Telemetry:** Our rules, templates, and CLI scripts (`npx @codifiedlabs/spec-to-code`) contain no tracking pixels, analytics beacons, external logging, or telemetry scripts.
* **No Middleman Proxies:** We do not route prompt requests through custom intermediary servers. When using our rules in Cursor, Claude Code, GitHub Copilot, or Windsurf, your network traffic travels exclusively between your machine and your authenticated model vendor (Anthropic, OpenAI, Microsoft).
* **Code Privacy:** Codified Labs never has read, write, or inspection access to your codebase, your feature prompts, or your generated specifications.

---

## 2. Vulnerability Reporting

If you discover a security flaw, vulnerability, or unhandled execution risk in any Codified Labs CLI package or rule template:

1. Do NOT open a public GitHub issue.
2. Email your findings directly to **`security@codifiedlabs.dev`**.
3. Include reproduction steps, environment details, and relevant terminal logs.

We acknowledge receipt of reports within 24 hours and issue patched releases within 72 hours of verification.
