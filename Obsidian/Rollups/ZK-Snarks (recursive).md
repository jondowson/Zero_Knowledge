
A recursive SNARK system generates proofs in parallel for different transaction blocks and aggregates them into one single block proof that gets submitted to the main blockchain, which means one SNARK can verify other SNARKs.

Recursive ZK-SNARKs dramatically increase the number of transactions that can be finalized with a ZK proof by including multiple L2 proofs in a single proof submitted to the L1 chain, which is currently limited by Ethereum’s 12-14 second block time.

**Plonky2 is a novel proving mechanism used in Polygon Zero, a proposed** [**Polygon ZK rollup**](https://www.alchemy.com/overviews/polygon-zk-rollups) **that uses recursive ZK-SNARKs to increase transactions.**

Recursive SNARKs scale the proof-generation process by aggregating several proofs into a recursive proof, and Plonky2 uses the same technique to decrease the time it takes to generate new block proofs. 

The Plonky2 proving mechanism generates proofs for **thousands of transactions in parallel** before recursively aggregating them into one block proof. This is more efficient than traditional proving mechanisms that try to generate the _entire_ block proof at once. 

The benefits of this approach are obvious.

**Plonky2 can generate a recursive proof in 0.17 seconds**, making it the fastest proving mechanism available. Moreover, Plonky2 produces proofs on a consumer-grade device, solving the hardware centralization issues with regular SNARK-based prover systems.

