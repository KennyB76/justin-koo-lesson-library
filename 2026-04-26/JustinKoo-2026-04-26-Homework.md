# 📐 Justin's Homework — Recursion & Tilings

**Student:** Justin Koo · **Grade:** 10 (Horace Mann) · **Date:** 2026-04-26
**Topic:** Linear Recurrences · Tiling Arguments · Characteristic Equation
**Due:** Next class (Sunday 2026-05-03)

---

## Topic Recap

Today we built mastery on three big tools:

| Tool | Form | Today's exemplar |
|------|------|------------------|
| **Tower of Hanoi** | $T(n) = 2T(n-1) + 1$ | First-order, non-homogeneous |
| **Lego Tilings** | $L_n = L_{n-1} + L_{n-2}$, $L_1=1, L_2=2$ | Second-order, homogeneous (Fibonacci-shifted: $L_n = F_{n+1}$) |
| **Tiling cut argument** | $L_{m+k} = L_m L_k + L_{m-1} L_{k-1}$ | Two-case decomposition (cut vs. straddle) |
| **Characteristic eqn** | $x^2 - a_1 x - a_2 = 0$ | $L_n$ closed form via golden ratio |

> **Goal of this homework:** make sure each tool is reliably callable on a problem you've never seen before. Show all work.

---

## Problem 1 · Tile a 7-Strip — Both Methods

Compute $L_7$ using **both** methods.

**(a) Case analysis** by number of 2-tiles $k$. Build the table:

| $k$ | $\binom{7-k}{k}$ |
|-----|------------------|
| 0 | __________ |
| 1 | __________ |
| 2 | __________ |
| 3 | __________ |
| **Total** | $L_7 = $ __________ |

**(b) Recurrence build-up** from $L_1 = 1, L_2 = 2$:

$$L_3 = ?, \;\; L_4 = ?, \;\; L_5 = ?, \;\; L_6 = ?, \;\; L_7 = ?$$

Both methods should give the same answer.

---

## Problem 2 · Tiling Argument

Use a tiling argument (cut-vs-straddle case analysis) to **prove**:

$$L_8 = L_3 L_5 + L_2 L_4$$

Then **verify numerically**: plug in your $L$ values and confirm the equation holds.

> Tip: place the cut between unit 3 and unit 4. Walk through Case A (no straddle) and Case B (a 2-tile covers units 3 and 4) — same playbook as Problem 4 from the Lego notes.

---

## Problem 3 · Modified Tilings — Squares & 3-Bricks

Suppose you tile an $n$-strip using only **1-tiles** (length 1) and **3-tiles** (length 3). Let $T_n$ = number of valid tilings.

(a) Set up the recurrence by considering what the **first tile** is. Justify the cases.

(b) State the initial values $T_1, T_2, T_3$.

(c) Compute $T_1$ through $T_8$.

(d) Bonus: which classical sequence is this? (Hint: it's a famous near-cousin of Fibonacci.)

---

## Problem 4 · Hanoi Adjacent-Only — Closed Form

Recall the adjacent-only Hanoi recurrence we derived:

$$A(n) = 3 A(n-1) + 2, \quad A(1) = 2$$

Use the **shift trick** to find the closed form.

(a) Find a constant $c$ so that $U(n) = A(n) + c$ becomes a pure geometric recurrence.
(b) Solve $U(n)$.
(c) Un-substitute to get $A(n)$.
(d) Verify $A(2)$ and $A(3)$ against your closed form.

> Hint: try $U(n) = A(n) + 1$ and see if the "+2" disappears.

---

## Problem 5 · Characteristic Equation — Closed Form for $L_n$

Apply the 5-step characteristic-equation method to:

$$L_n = L_{n-1} + L_{n-2}, \;\; L_0 = 1, \;\; L_1 = 1$$

(Use $L_0 = 1$ by convention.)

**Step 1** Identify the recurrence and constants $a_1, a_2$.
**Step 2** Write and solve the characteristic equation $x^2 - a_1 x - a_2 = 0$. Call the roots $\varphi$ and $\psi$.
**Step 3** State the general solution $L_n = C_1 \varphi^n + C_2 \psi^n$.
**Step 4** Use the initial values to solve for $C_1, C_2$.
**Step 5** State the closed form. Verify $L_5$ by both your closed form and the recurrence.

> This is **Binet-style** for our shifted Fibonacci. Test-likely.

---

## Problem 6 · Challenge — Triple-Tile Sequence

Tile an $n$-strip using **1-tiles, 2-tiles, AND 3-tiles** (any combination, in any order).

Let $H_n$ = number of valid tilings.

(a) Set up the recurrence by considering the first tile (3 cases).
(b) State the initial values $H_1, H_2, H_3$.
(c) Compute $H_1$ through $H_8$.
(d) **Bonus:** the sequence you'll get is the **Tribonacci numbers**. Look up the characteristic equation for it (cubic) — you don't need to solve it, but state it.

---

## Problem 7 · Conceptual Quick-Hits

Short answers (1-2 sentences each).

(a) Why does the Hanoi recurrence have a "+1" while the Lego recurrence has no constant term? What does that tell you about the structure of each problem?

(b) In the tiling argument, why are Cases A and B always **mutually exclusive**?

(c) For the cut $L_{m+k} = L_m L_k + L_{m-1} L_{k-1}$, what does the **second term** ($L_{m-1} L_{k-1}$) physically represent on the strip?

---

## Submission Checklist

- [ ] Show all work clearly — partial credit for setup, full credit for clean derivations.
- [ ] **Box** every final answer.
- [ ] State which tool/method you're using at the start of each problem (it earns you points).
- [ ] If a sanity check is requested, do it — small arithmetic catches big errors.

---

*Newton School Fort Lee · Mr. Kenny · Pre-Calculus*
