# Artificial Intelligence By Komeiji

![Koishi Love](https://media1.tenor.com/m/Ivza1kTpowkAAAAC/koishi-koishi-komeiji.gif)

- [Artificial Intelligence By Komeiji](#artificial-intelligence-by-komeiji)
  - [4.2 Knowledge and Reasoning](#42-knowledge-and-reasoning)
  - [4.2.1 Knowledge Representation Techniques](#421-knowledge-representation-techniques)
    - [1. Logical Representation](#1-logical-representation)
    - [2. Semantic Networks](#2-semantic-networks)
    - [3. Frames](#3-frames)
    - [4. Rules](#4-rules)
    - [5. Ontologies](#5-ontologies)
  - [4.2.2 Reasoning and Inference Mechanisms](#422-reasoning-and-inference-mechanisms)
  - [4.2.3 Summary Table of KR Techniques](#423-summary-table-of-kr-techniques)

## 4.2 Knowledge and Reasoning

Artificial intelligence systems operate on data. However, raw data alone does not lead to intelligence. AI must transform data into structured knowledge. Knowledge Representation (KR) achieves this by defining formats and methods for organizing information. This enables AI systems to simulate human-like thinking, allowing them to solve problems, understand relationships, and derive new knowledge from existing information.

This module covers:

* Key knowledge representation techniques
* Reasoning systems and inference mechanisms
* The role of ontologies in AI

---

## 4.2.1 Knowledge Representation Techniques

Knowledge Representation (KR) in AI refers to encoding information about the world into formats that AI systems can utilize to solve complex tasks. KR enables machines to reason, learn, and make decisions by structuring data in ways that mirror human understanding.

### 1. Logical Representation

* Uses formal logic to represent knowledge and infer new knowledge.
* **Types:**

  * **Propositional Logic:** Deals with facts as true or false statements. Example: “It is raining” → TRUE/FALSE
  * **First-Order Logic (FOL):** Allows quantifiers and predicates to describe relationships between objects. Example: “All humans are mortal” → ∀x(Human(x) → Mortal(x))

**Advantages:** Precise and unambiguous; supports automated reasoning
**Limitations:** Can become complex for large-scale knowledge

---

### 2. Semantic Networks

- Represents knowledge as a **graph structure**.
- **Nodes:** Concepts or objects (e.g., “Cat”, “Animal”)
- **Edges:** Relationships between nodes (e.g., “is-a”, “has-part”)

**Example:**

```txt
Cat → is-a → Animal
Cat → has-part → Tail
```

**Advantages:** Intuitive visualization of relationships
**Limitations:** Can be difficult to handle complex inferences

---

### 3. Frames

* Knowledge is represented as **structured objects** (frames) with slots (attributes) and values.
* Useful for **representing stereotypical situations**.

**Example Frame:**

```
Frame: Dog
  - Type: Animal
  - Has-legs: 4
  - Sound: Bark
```

**Advantages:** Easy to model real-world objects and inheritance
**Limitations:** Less flexible for highly dynamic knowledge

---

### 4. Rules

* Knowledge is encoded as **IF-THEN rules** for decision making.
* Supports **forward chaining** (data-driven) and **backward chaining** (goal-driven) inference.

**Example:**

```
IF temperature > 100°C THEN state = “Boiling”
```

**Advantages:** Clear, easy to implement for expert systems
**Limitations:** Can become large and unwieldy; lacks flexibility

---

### 5. Ontologies

* Ontologies define **formal specifications of concepts** and relationships in a domain.
* Used to enable **shared understanding** and interoperability between systems.

**Example:** Medical ontology might define:

* Concept: Disease
* Relationships: causes, treated-by, associated-with

**Advantages:** Supports knowledge sharing and reasoning over complex domains

---

## 4.2.2 Reasoning and Inference Mechanisms

* **Reasoning** allows AI to draw conclusions from existing knowledge.
* **Inference engines** implement rules and logic to derive new knowledge.

**Types of Reasoning:**

1. **Deductive Reasoning:** General → Specific

   * Example: “All humans are mortal; Socrates is a human → Socrates is mortal”
2. **Inductive Reasoning:** Specific → General

   * Example: “This swan is white; all observed swans are white → All swans are white”
3. **Abductive Reasoning:** Observations → Best Explanation

   * Example: “Grass is wet → It probably rained”

---

## 4.2.3 Summary Table of KR Techniques

| Technique              | Structure/Format                    | Advantages                            | Limitations                       |
| ---------------------- | ----------------------------------- | ------------------------------------- | --------------------------------- |
| Logical Representation | Statements & predicates             | Precise, supports automated reasoning | Complex for large knowledge bases |
| Semantic Networks      | Graph of nodes & edges              | Visual, intuitive relationships       | Hard for complex inference        |
| Frames                 | Object with slots                   | Easy inheritance, real-world modeling | Less flexible for dynamic info    |
| Rules                  | IF-THEN                             | Clear, effective for expert systems   | Can become large/unwieldy         |
| Ontologies             | Formalized concepts & relationships | Enables shared understanding          | Can be complex to design          |

