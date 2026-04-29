# 💡 Big Picture

This is a **Genetic Algorithm (GA)** that tries to **maximize a math function you type in**, like:

```
7 * x - x * x
```

It “evolves” possible values of `x` (encoded as binary strings) to find the best result.

---

## 🧬 Step-by-step flow

### 1. You input a function

```java
functionInput = sc.nextLine();
```

Example:

```
7 * x - x * x
```

This is what the algorithm will try to maximize.

---

## 2. Population is created (random guesses)

```java
List<String> population = new ArrayList<>();
for (int i = 0; i < popSize; i++) {
    population.add(generateRandomBinary());
}
```

* `popSize = 6`
* Each individual is a **6-bit binary string**

  * Example: `"101011"`
* That converts to numbers:

  * `000000 = 0`
  * `111111 = 63`

So your “search space” is **0–63**

---

## 🧪 3. Fitness evaluation (how good each x is)

```java
evaluate(binary)
```

Steps:

1. Convert binary → integer:

   ```java
   int x = Integer.parseInt(binary, 2);
   ```

2. Replace `x` in your function:

   ```java
   expr = functionInput.replace("x", "(" + x + ")");
   ```

Example:

```
7 * (12) - (12) * (12)
```

3. Evaluate math expression using `simpleEval()`

---

## 🧠 4. Sorting (selection pressure)

```java
population.sort((a, b) -> Double.compare(evaluate(b), evaluate(a)));
```

* Best fitness goes to the top
* Worst goes to bottom

So now:

```
[best, better, ..., worst]
```

---

## 🏆 5. Tracking best solution

```java
bestInGen = population.get(0);
```

This prints:

```
Generation X - Best x: ..., f(x): ...
```

Also tracks the **global best across all generations**

---

## 👶 6. Selection (survival of the fittest)

```java
List<String> survivors = new ArrayList<>(population.subList(0, popSize / 2));
```

* Top 50% survive
* Bottom 50% die 💀

So:

* 6 → only top 3 survive

---

## 🔀 7. Crossover (reproduction)

```java
String child = p1.substring(0, cp) + p2.substring(cp);
```

What happens:

* Pick 2 parents
* Cut at random point
* Combine them

Example:

```
Parent1: 101|011
Parent2: 010|111
Child:   101111
```

---

## 🎲 8. Mutation (random randomness)

```java
if (rand.nextDouble() < 0.05)
```

* 5% chance
* flips 1 random bit

Example:

```
101011 → 101001
```

This prevents getting stuck too early.

---

## 🔁 9. Repeat for 30 generations

```java
for (int g = 1; g <= generations; g++)
```

Each generation:

* evaluate
* sort
* select
* crossover
* mutate
* replace population

---

## 🧾 Final output

```java
Best x found: ...
f(x) = ...
```

This is the best solution the GA discovered.

---

## ⚠️ Important quirks (why your earlier bug happened)

You mentioned:

> evalSimple(String) is undefined

In your current code:

* you **don’t use evalSimple externally**
* it’s an **anonymous recursive parser inside `simpleEval`**

So the GA itself is fine — the confusion likely came from earlier refactoring or naming mismatch.

---

## 🧠 What this program *really is*

It’s basically:

> “Randomly guess numbers → score them → mix the good ones → repeat → hope evolution finds the max.”

---

## ⚡ One-sentence summary

You’re evolving 6-bit numbers (0–63) using selection, crossover, and mutation to maximize a user-defined math function.


