ZK-SNARK is a protocol for generating zero-knowledge proofs to verify the authenticity of information without exposing the underlying data.

- Zero-knowledge | Succinct | Non-interactive | Argument-of-knowledge 
- Proofs are small (128-288bytes) and can be verified quickly.
- Runs a computation off chain that creates a validity proof.
	- Each individual transaction of proof is computationally verified.
- Passes this proof back to the L1 blockchain.
- Requires a Trusted Setup: 
	- Setting up the ZK-SNARK protocol requires the creation of a Universal Common Reference String (CRS). 
	- Also described as _public parameters_, the CRS enables secure communication between provers and verifiers.
	- If a malicious actor gained knowledge of the public parameters, they could generate false validity proofs. Some projects attempt to solve this problem by [using multi-party computation](https://zkproof.org/2021/06/30/setup-ceremonies/amp/) (MPC), which involves different individuals, to generate the public parameters.
- ZK-SNARK uses Elliptic Curve Cryptography (ECC) to encrypt information used in producing validity proofs. 
	- ECC is relatively secure for now, but advancements in quantum computing could break its security model.

