This page outlines the steps for creating a ZK-SNARK proof.

Concepts:
- A 'Circuit' is a multistep decomposition of an algebraic expression. 
- A 'Gate' within a circuit has two inputs and one output.
- A 'Witness' expression is used to define each intermediary value of the expression at each step in the circuit, expressed as a vector.

Algebraic expression:

- y = x<sup>3</sup> + 2x + 5

The circuit is decomposed into 4 Steps that represent the three gates in this example:

- Note that the first gate requires 2 steps to handle x<sup>3</sup> as the notation does not accommodate multiplying to a power.

1. T1 = x * x
2. z = T1 * x
3. T2 = (z + 2x) * 1
4. y = (T2 + 5) * 1

	