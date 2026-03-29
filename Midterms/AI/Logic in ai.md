# 4.1 Logic in AI

![Koishi](https://media1.tenor.com/m/m7GJ0rllCYoAAAAC/koishi-komeiji-touhou.gif)

- [4.1 Logic in AI](#41-logic-in-ai)
  - [4.1.1 Role of Knowledge in AI](#411-role-of-knowledge-in-ai)
  - [4.1.2 Logic as a Tool for AI](#412-logic-as-a-tool-for-ai)
  - [4.1.3 Types of Logic in AI](#413-types-of-logic-in-ai)
    - [1. Propositional Logic](#1-propositional-logic)
    - [2. First-Order Logic (FOL)](#2-first-order-logic-fol)
    - [3. Other Logical Systems](#3-other-logical-systems)
  - [4.1.4 Reasoning in Logic-Based AI](#414-reasoning-in-logic-based-ai)
  - [4.1.5 Summary Table of Logic in AI](#415-summary-table-of-logic-in-ai)

Humans appear intelligent because they **know things** and can use that knowledge to make decisions and solve problems. This intelligence is not based solely on reflexes but on **reasoning processes** that operate on internal representations of knowledge.

In AI, **logic** provides the formal framework for these reasoning processes. Logic allows AI systems to represent knowledge precisely, make inferences, and reason systematically.

---

## 4.1.1 Role of Knowledge in AI

Knowledge and intelligence in AI share a **symbiotic relationship**:

* **Knowledge as a Foundation:** Provides **facts, rules, and data** that AI systems use for decision-making.
* **Intelligence as a Mechanism:** Uses reasoning to **interpret, manipulate, and derive new knowledge** from existing information.

Without structured knowledge, reasoning cannot occur; without reasoning, knowledge cannot be applied effectively.

---

## 4.1.2 Logic as a Tool for AI

Logic is used in AI to:

1. **Represent Knowledge:** Encodes facts, objects, and relationships in a structured, unambiguous way.
2. **Infer New Knowledge:** Allows the system to **draw conclusions** from existing information using formal rules.
3. **Support Decision-Making:** Enables AI to choose actions based on known facts and logical consequences.

---

## 4.1.3 Types of Logic in AI

### 1. Propositional Logic

* **Structure:** Simple statements (propositions) that are either **true** or **false**.
* **Connectives:** AND (∧), OR (∨), NOT (¬), IMPLIES (→)
* **Example:**

  * Proposition: “It is raining” → TRUE/FALSE
  * Rule: “If it is raining, then the ground is wet” → `Raining → WetGround`

**Advantages:** Simple, precise, easy to compute
**Limitations:** Cannot represent objects or relationships in detail

---

### 2. First-Order Logic (FOL)

* **Structure:** Extends propositional logic with **quantifiers**, **predicates**, and **variables**.
* **Uses:** Represent relationships between objects, general rules, and more complex knowledge.
* **Example:**

  * Rule: “All humans are mortal” → ∀x(Human(x) → Mortal(x))
  * Fact: Human(Socrates) → Socrates is mortal

**Advantages:** More expressive than propositional logic, supports complex reasoning
**Limitations:** Reasoning can be computationally expensive

---

### 3. Other Logical Systems

* **Modal Logic:** Adds notions of possibility, necessity, and belief. Useful for reasoning about uncertainty.
* **Non-Monotonic Logic:** Allows reasoning with **incomplete or changing information**; conclusions can be revised.
* **Fuzzy Logic:** Handles reasoning with **degrees of truth** rather than strict true/false. Useful for real-world approximate reasoning.

---

## 4.1.4 Reasoning in Logic-Based AI

AI uses logical reasoning to **derive conclusions**:

1. **Deductive Reasoning:** Guaranteed conclusions if premises are true.

   * Example: All humans are mortal; Socrates is human → Socrates is mortal
2. **Inductive Reasoning:** Generalizations from specific instances; conclusions are probable, not guaranteed.

   * Example: Observed 100 swans are white → All swans might be white
3. **Abductive Reasoning:** Inferring the most likely explanation for an observation.

   * Example: Grass is wet → It probably rained

---

## 4.1.5 Summary Table of Logic in AI

| Logic Type          | Structure/Use                  | Strengths                                     | Limitations                |
| ------------------- | ------------------------------ | --------------------------------------------- | -------------------------- |
| Propositional Logic | True/False statements          | Simple, precise                               | Limited expressiveness     |
| First-Order Logic   | Predicates, objects, relations | Highly expressive, supports complex reasoning | Computationally expensive  |
| Modal Logic         | Possibility, necessity         | Reasoning about knowledge and belief          | More complex               |
| Non-Monotonic Logic | Reasoning with changing info   | Flexible, adapts to new info                  | Hard to implement          |
| Fuzzy Logic         | Degrees of truth               | Handles uncertainty and approximation         | Not exact, less formalized |
