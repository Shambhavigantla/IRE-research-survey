# Private Information Retrieval — Survey Plan (Information-Theoretic Track)
 
> Working document for the IRE research-survey. Editable; rearrange freely.
 
---
 
## 1. One-line topic
 
The **information-theoretic foundations and capacity limits of Private Information Retrieval (PIR)** — the multi-server line from Chor–Goldreich–Kushilevitz–Sudan through the Sun–Jafar capacity results, including the connection to locally decodable codes (LDCs).
 
## 2. Scope caveat (read first)
 
This topic is cryptographic **information theory about private data access**, not the ranking/relevance learning theory of the instructor's approved examples (unbiased LTR, rank aggregation, convex LETOR surrogates). It is deep and self-contained, but it sits *outside* that approved axis, so **it needs the instructor's explicit sign-off before you start reading**. Use the pitch in §8 to get that sign-off first. If he declines, pivot to rank aggregation (an approved example) rather than spending days on a rejected scope.
 
## 3. Central question
 
How little must be communicated to retrieve record *i* from one or more servers that must learn **nothing** about *i* — and what is the exact information-theoretic limit? Privacy is posed as a *communication-complexity* problem; the organizing quantity is **capacity**: the most bits retrievable privately per bit downloaded.
 
## 4. Why it clears the theory bar
 
- Pure theory: communication complexity, explicit lower bounds, a Shannon-style capacity result with a closed form and a converse. No systems, no experiments in the core.
- A clear seminal canon spanning 30 years (1995 → present), with an unmistakable founding paper (CGKS) and an unmistakable modern turning point (Sun–Jafar capacity).
- Most self-contained topic on the shortlist: one coherent toolkit (finite-field linear algebra + information theory), so it is **learnable in a week** once the prerequisites are in place.
## 5. Non-overlap with the VeriSimplePIR term project (how to plan it)
 
Draw the line once, in writing, and hold it.
 
| | **Survey (this topic)** | **Term project** |
|---|---|---|
| Branch | Information-theoretic, **multi-server** | Computational, **single-server** |
| Math | Information theory + coding theory | Lattice / LWE cryptography |
| Question | Fundamental limits (what is possible) | Measured performance (how fast) |
| Objects | CGKS, capacity, LDC lower bounds | SimplePIR, VeriSimplePIR, benchmarks |
| Venues | IT / coding theory | Applied-crypto / systems |
 
**Operational rules to guarantee zero overlap:**
1. Never cite a lattice/LWE scheme as part of the survey's body.
2. Never discuss an implementation, a runtime, or a benchmark number.
3. Treat the *computational single-server* branch as a **single context paragraph** only (to explain the branch split), never as a chapter.
4. Frame the survey explicitly as the **theory layer** of the project's field — complement, not duplicate.
Held this way, the two deliverables share no method and no result.
 
## 6. Learning curve (staged)
 
Shape: **steep entry, then flattening.** The first two stages load the prerequisites and the model and cost the most; after that each paper reuses the same toolkit, so marginal cost drops. Budget your hardest days early.
 
- **Stage 0 — Prerequisites (½ day).** Basic information theory (entropy, mutual information — enough to know what "capacity" means); communication complexity (bits exchanged as the cost metric); linear algebra over finite fields (vectors/polynomials over GF(q)). *IR anchor:* a user querying a search index without revealing the query — privacy of the retrieve → serve half of the course.
- **Stage 1 — Problem & model (CGKS).** Retrieve record *i* so no server learns *i*; the trivial solution is "download everything," so the field is about beating that cost. Learn the two organizing axes: multi-server vs. single-server, and information-theoretic vs. computational. You live on the **information-theoretic, multi-server** branch.
- **Stage 2 — Constructions & upper bounds (Ambainis; Beimel–Ishai–Kushilevitz–Raymond).** How clever encodings drive communication down and what the best known constructions achieve. Finite-field machinery pays off here.
- **Stage 3 — Lower bounds & the LDC connection (Katz–Trevisan; Yekhanin; Efremenko).** The conceptual heart: PIR schemes and locally decodable codes are essentially the same object, and that equivalence is what lets you prove *limits*, not just constructions. The most viva-impressive stage.
- **Stage 4 — Capacity (Sun–Jafar).** The modern spine: capacity = most bits retrievable privately per bit downloaded (the analogue of Shannon channel capacity); its closed form and the converse. If you master one thing deeply, make it this.
- **Stage 5 — Extensions (colluding / coded / symmetric).** The lattice of richer models, each moving the capacity formula. Breadth showing the field is alive and has open regions.
## 7. Reading list (dependency order; ★ = seminal spine)
 
Ten core papers, tightened for a one-week budget. Read top to bottom.
 
1. **Gasarch (2004)** — *A Survey on Private Information Retrieval.* Skim first for the map (~½ day).
2. ★ **Chor, Goldreich, Kushilevitz & Sudan (1995/1998)** — *Private Information Retrieval.* Founding multi-server IT-PIR; the communication-complexity framing.
3. **Ambainis (1997)** — *Upper Bound on the Communication Complexity of PIR.* Improved multi-server construction.
4. **Beimel, Ishai, Kushilevitz & Raymond (2002)** — *Breaking the O(n^{1/(2k−1)}) Barrier for Information-Theoretic PIR.*
5. **Katz & Trevisan (2000)** — *On the Efficiency of Local Decoding Procedures for Error-Correcting Codes.* Establishes the PIR ↔ LDC link.
6. ★ **Yekhanin (2008)** — *Towards 3-Query Locally Decodable Codes of Subexponential Length.* The lower-bound-side breakthrough.
7. **Efremenko (2009)** — *3-Query Locally Decodable Codes of Subexponential Length.* Matching-vector construction; read right after Yekhanin.
8. ★ **Sun & Jafar (2017)** — *The Capacity of Private Information Retrieval* (IEEE Trans. IT). The capacity turning point and closed form.
9. **Sun & Jafar (2017)** — *The Capacity of Robust PIR with Colluding Databases.* The most-cited extension.
10. **Banawan & Ulukus (2018)** — *The Capacity of PIR from Coded Databases.* Bridges PIR and distributed-storage coding.
*Optional swap:* **Sun & Jafar (2019), Symmetric PIR** in place of #10 if you prefer server-privacy over the coding bridge.
 
**7-day pacing:** Day 1 — survey + start CGKS. Days 2–7 — the spine and supports in order (one paper/day, two on light ones). Days 8–10 overflow if available — writing and building the mental map (model → constructions → lower bounds → capacity → extensions) the viva will probe.
 
## 8. Two-sentence note to send the instructor (pre-approval)
 
> I'd like to propose a theory survey on the information-theoretic foundations and capacity limits of private information retrieval — the multi-server IT-PIR line from Chor–Goldreich–Kushilevitz–Sudan through the Sun–Jafar capacity results, including the connection to locally decodable codes. It is scoped to complement, not duplicate, my VeriSimplePIR benchmark project: the project measures a concrete computational (lattice-based) system, whereas the survey covers the information-theoretic limits and lower-bound theory of the primitive, with no overlap in methods or results.
 
## 9. IR-course connection
 
The motivating scenario — querying a search index without revealing the query — is privacy of the course's parse → retrieve → serve path. The capacity/communication-complexity intuitions (what private access *can* cost at best) are the mental models that make the systems side of private retrieval legible.
 
## 10. Honest bottom line
 
Best **week of learning** on the shortlist (narrow, deep, one toolkit) — but for a topic that may not be approved. Get the §8 sign-off before committing the week.