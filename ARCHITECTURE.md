# The Codified Labs Architecture Manifesto
### Principles of Spec-Driven Development (SDD) in the Age of AI Coding Agents

[ Human Intent ]
          │
          ▼
          ┌──────────────────────┐
│  Negative Constraint │  <-- Eliminates Hallucinations
│       Analysis       │
└──────────┬───────────┘
│
▼
┌──────────────────────┐
│ Relational Contracts │  <-- PostgreSQL DDL + UUIDv7
│   & API Envelopes    │
└──────────┬───────────┘
│
▼
┌──────────────────────┐
│ Deterministic Tests  │  <-- Gherkin Given/When/Then
│       Matrices       │
└──────────┬───────────┘
│
▼
[ Autonomous Agent ]   ──> Generates Production Code
---

## 1. The Context Dilution Law

As system prompt sizes increase horizontally with unrelated tools and instructions, an LLM's adherence to nuanced instructions degrades non-linearly. 

Bundles offering "150+ developer skills" violate basic attention mechanics. Injecting marketing rules, SEO scrapers, and generic styling advice into an IDE context window introduces noise that causes the model to ignore critical backend constraints.

**The Codified Labs Standard:**  
Our engines operate vertically. We deploy modular, decoupled rules that trigger only at specific lifecycle checkpoints (Scoping $\to$ Architecture $\to$ Criteria), keeping the active context window minimal, sharp, and deterministic.

---

## 2. The Negative Constraint Principle

LLMs are trained to be agreeable and generative. When given incomplete requirements, their default behavior is to guess reasonable-sounding defaults. In software engineering, "reasonable guesses" lead to technical debt:
* The model assumes database columns are nullable when they should be strictly constrained.
* The model selects auto-incrementing integer IDs because they are common in public training sets, introducing enumeration attack vectors.
* The model writes mock API responses without idempotency mechanics.

**The Codified Labs Standard:**  
Every engine we produce begins with explicit **Negative Constraints (Phase 1 Execution)**. We explicitly instruct the model on what it is forbidden from doing before allowing it to generate what it should do.

---

## 3. The Unbroken Chain of Custody

A technical specification is not an isolated document; it is a binding contract between product requirements and low-level code generation.

1. **Stage 1 (Product Intent):** Business scope must define explicit "Out-of-Scope" boundaries to prevent autonomous agents from refactoring adjacent systems.
2. **Stage 2 (Data Contract):** Database schemas must be defined in full PostgreSQL DDL—including foreign keys, cascade behaviors, and index types—prior to generating API controllers.
3. **Stage 3 (Verification Contract):** Acceptance criteria must be formatted in verifiable Gherkin syntax (`Given / When / Then`) covering concurrency, network timeouts, and permission boundaries.

No application code may be generated until all three stages pass the self-critique verification audit.
