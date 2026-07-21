# M0 Quiz — Foundation Check

*Import into Google Classroom as a Quiz assignment. All 5 questions are multiple choice. Mark correct answers before publishing.*

---

**Q1.** You need to rename a variable in one file. Which effort level is most appropriate?

- A) Low ✓
- B) Medium
- C) High
- D) Max

*Explanation: Low effort is sufficient for a targeted single-file change. Higher effort pulls more context and costs more credits with no quality gain for this task.*

---

**Q2.** You are comparing two models in the picker. Model A has lower input cost but higher output cost than Model B. You need to generate a 1,500-word document. Which model is cheaper for this task?

- A) Model A — lower input cost always wins
- B) Model B — lower output cost wins when generating long responses ✓
- C) They cost the same
- D) Cannot determine without knowing exact token counts

*Explanation: For tasks that produce long outputs, output cost dominates the total. Lower output cost wins.*

---

**Q3.** Which VS Code Copilot mode can run terminal commands and read multiple files automatically?

- A) Ask
- B) Edit
- C) Agent ✓
- D) Inline Chat

*Explanation: Agent mode has a full toolbelt including terminal execution, file system access, and web search.*

---

**Q4.** A developer skips writing a spec and iterates with the AI based on what comes back. After 15 iterations the output no longer matches the original intent. This is an example of:

- A) Normal AI behaviour — models are non-deterministic
- B) Token budget exhaustion
- C) Context window overflow
- D) Drift caused by the absence of a stable specification ✓

*Explanation: Without a spec as a stable target, iterative prompting accumulates drift. SDD (Spec-Driven Development) prevents this.*

---

**Q5.** When is a 1M token context window warranted over a 200k window?

- A) Always — more context always produces better answers
- B) When asking questions that require synthesising information across a very large codebase or full documentation library ✓
- C) When the effort level is set to Max
- D) When using Agent mode

*Explanation: 1M context is more expensive and slower. It is warranted only when the task genuinely requires broader context than 200k can hold.*
