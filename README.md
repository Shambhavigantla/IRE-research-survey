# Private Information Retrieval (Information-Theoretic Track)
 


The **information-theoretic foundations and capacity limits of Private Information Retrieval (PIR)** — the multi-server line from Chor–Goldreich–Kushilevitz–Sudan through the Sun–Jafar capacity results, including the connection to locally decodable codes (LDCs).
 

| | **Survey ** | **Term project** |
|---|---|---|
| Branch | Information-theoretic, **multi-server** | Computational, **single-server** |
| Math | Information theory + coding theory | Lattice / LWE cryptography |
| Question | Fundamental limits (what is possible) | Measured performance (how fast) |
| Objects | CGKS, capacity, LDC lower bounds | SimplePIR, VeriSimplePIR, benchmarks |
| Venues | IT / coding theory | Applied-crypto / systems |
 
 
##  Learning curve 
 
Ten core papers
 
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
