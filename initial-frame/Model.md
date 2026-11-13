# PIR Model: The Core Questions to Ask

When reading a PIR paper, the fastest way to understand it is to answer three questions:

## 1) What is the model?

Ask:
- How many servers are involved?
- Is the database replicated across servers?
- Can servers collude with one another?
- Is the privacy guarantee information-theoretic or computational?

## 2) What is the cost?

The most common metric is:

\[
\boxed{\text{Communication}}
\]

In other words: how many bits must be exchanged between the client and servers?

Other costs may also matter:
- Server computation
- Storage overhead
- Upload cost
- Download cost

## 3) What is the guarantee?

Ask:
- Does the user always get the correct item?
- Does each server learn nothing about the queried index?
- What happens if servers collude?

---

## Quick takeaways

1. PIR means retrieving \(x_i\) without revealing the index \(i\).
2. Downloading the entire database is perfectly private, but it is inefficient.
3. Multiple servers make information-theoretic PIR practical, because each server only sees a private, random-looking share of the query.

---

## One-line summary

PIR is about retrieving a specific database item while hiding which item was requested, while balancing privacy, efficiency, and correctness guarantees.