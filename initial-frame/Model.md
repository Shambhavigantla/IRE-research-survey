The three questions every PIR paper answers
As you read PIR papers, always ask:
Question 1: What is the model?
- How many servers?
- Are databases replicated?
- Can servers collude?
- Information-theoretic or computational privacy?
Question 2: What is the cost?
Usually we care about:
\[
\boxed{\text{Communication}}
\]
How many bits must be exchanged?

Later, papers may also consider:
- server computation,
- storage,
- upload cost,
- download cost.
Question 3: What is the guarantee?
- Does the user get the correct item?
- Does each server learn nothing?
- What happens if servers collude?


①
PIR means retrieving \(x_i\) without revealing \(i\).
②
Downloading the entire database is perfectly private, but inefficient.
③
Multiple servers make information-theoretic PIR possible efficiently because each server can see an individually private/random-looking share of the query.