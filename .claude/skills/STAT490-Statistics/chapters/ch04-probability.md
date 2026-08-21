# Chapter 4: Probability

## Core Idea

Probability quantifies uncertainty in a procedure that produces outcomes. Define the procedure, sample space, event, and reference set first. Choose a source: observed relative frequency, a classical equally likely model, or informed subjective judgment. Probability ranges from 0 (impossible) to 1 (certain). A very small probability under an assumption supports the rare event rule: question the assumption, not the cause.

Distinguish same-trial "or" and "and" from sequential "and." In addition, `P(A and B)` is an overlap; in multiplication, it can mean A followed by B.

## Frameworks Introduced (exact named concepts, when to use, how)

- **Sample Space, Simple Event, Event, and Compound Event:** The sample space contains every possible simple outcome. An event is a set of outcomes; a compound event combines events. Make outcomes fine-grained enough that none can be split further.

- **Reference-Set Model:** Every probability has a denominator. Unconditional probability uses the full sample space; `P(B | A)` uses only outcomes in A. Ask, "Among which outcomes am I counting?"

- **Relative Frequency Approximation of Probability:** With repeated data, estimate `P(A)` as `number of A outcomes / number of trials`; more observations usually improve the approximation. The **Law of Large Numbers** says long-run relative frequency tends toward the actual probability, though short runs need not look balanced.

- **Classical Approach to Probability (Requires Equally Likely Outcomes):** If `n` simple outcomes are equally likely and A occurs in `s`, use `P(A) = s/n`. No information does not imply equal likelihood. Use **Subjective Probabilities** when data and an equally likely model are unavailable, and label the result an estimate.

- **Rare Event Rule for Inferential Statistics:** If a result is extremely unlikely under a stated assumption, treat it as evidence against that assumption. It does not establish why the result occurred.

- **Complementary Events and Rule of Complementary Events:** The complement `A^c` is the event that A does not occur. `P(A) + P(A^c) = 1`, so `P(A^c) = 1 - P(A)`. Use it when the complement is easier to calculate.

- **Formal Addition Rule and Intuitive Addition Rule:** For inclusive same-trial "or," `P(A or B) = P(A) + P(B) - P(A and B)`. Subtract the overlap once. For **Disjoint (or Mutually Exclusive) Events**, the overlap is 0, so probabilities add.

- **Conditional Probability:** When information restricts the reference group, `P(B | A) = P(A and B) / P(A)`, provided `P(A) > 0`. Restrict attention to A, then find the proportion also satisfying B; usually `P(B | A)` differs from `P(A | B)`.

- **Formal Multiplication Rule and Intuitive Multiplication Rule:** For sequential "and," `P(A and B) = P(A)P(B | A)`. Multiply along a branch, adjusting each later probability for what already occurred.

- **Independent and Dependent Events:** Events are independent when one does not change the other: `P(B | A) = P(B)` and `P(A and B) = P(A)P(B)`. Otherwise they are dependent. Replacement often supports independence; sampling without replacement usually creates dependence. Dependence is not necessarily causation.

- **Treating Dependent Events as Independent: The 5% Guideline for Cumbersome Calculations:** For sampling without replacement, use the independence approximation only when the sample is no more than 5% of the population and exact calculation is cumbersome. If exact factors are easy, use them; the guideline is not literal independence.

- **Complements: The Probability of "At Least One":** At least one means one or more. Calculate `P(at least one) = 1 - P(none)`. For `n` independent trials with occurrence probability `p`, use `1 - (1-p)^n`; for dependent trials, use conditional factors for none.

- **Simulation:** Use simulation when a procedure is easy to imitate but enumeration is difficult. Preserve outcome probabilities, run complete trials, record the target event, and repeat. Estimate probability as successes divided by simulated trials; it is an approximation.

- **Counting:** The **Fundamental Counting Rule** multiplies successive choices: `m` followed by `n` choices gives `mn` sequences. The **Factorial Rule** gives `n! = n(n-1)...2(1)`, with `0! = 1`. For `r` of `n` different items when order matters, use **Permutations** `nPr = n!/(n-r)!`; for identical categories arranged together, use `n!/(n1! n2! ... nk!)`. When order does not matter, use **Combinations** `nCr = n!/[(n-r)!r!]`.

- **Bayes' Theorem (Bayes' rule):** Reverse a conditional with `P(A | B) = P(B | A)P(A)/P(B)`, where `P(B) > 0`. If `A1, ..., Ak` form a mutually exclusive, exhaustive partition, calculate `P(B) = sum_j P(B | Aj)P(Aj)`, then `P(Ai | B) = P(B | Ai)P(Ai)/P(B)`. **Test Sensitivity and Test Specificity** are conditional rates: positive among cases present and negative among cases absent. Neither alone gives the probability a positive result is correct; base rates matter.

## Key Concepts (5-10)

1. **Model before calculating.** Define the sample space and event; in a sequence, `fff`, `ffm`, and `mff` are different outcomes even if they have the same count of girls.
2. **Choose the source deliberately.** Use data for relative frequency, equal likelihood for the classical rule, and informed judgment for subjective probability.
3. **Use complements strategically.** "Not" and "at least one" often become a simpler none calculation followed by `1 -`.
4. **Treat "or," "and," and conditions differently.** Addition controls overlap; multiplication adjusts later probabilities; `P(B | A)` uses only outcomes in A.
5. **Check independence and choose the tool.** No replacement usually changes probabilities, so apply the 5% guideline only as justified. Count by order, simulate difficult procedures, and use Bayes to update evidence.

## Mental Models

- **The reference-set and tree models:** Write the denominator first. Use the full sample space unconditionally and a restricted sample space conditionally. In a tree, branch first, place conditional probabilities later, multiply paths, and add disjoint targets.
- **The overlap and reliability models:** Subtract shared outcomes for a union. For independent backups, multiply failure probabilities when all must fail, then use the complement for at least one working.

## Anti-patterns

- Assigning `1/2` merely because there are two verbal outcomes, or using `s/n` without checking equal likelihood.
- Adding overlapping probabilities without subtracting `P(A and B)`.
- Multiplying unconditional probabilities when the second event is affected by the first, especially without replacement.
- Confusing `P(B | A)` with `P(A | B)`, the **confusion of the inverse** or prosecutor's fallacy.
- Reading "at least one" as "exactly one," or using `1 - P(none)` with an incorrectly modeled none case.
- Calling events independent because their wording seems unrelated; shared equipment, mechanics, power, or a changing sample can create dependence.
- Simulating two dice with one uniform number from 2 through 12, using the wrong counting rule, treating simulation as exact, or confusing actual odds with payoff odds.
- Treating a very small probability as proof, rather than evidence evaluated under an assumption.

## Worked Example

### Polygraph Tree and Bayes' Theorem

Let `L` mean a subject actually lied and `+` mean a positive result. Among 98 subjects:

| Actual state | Positive (`+`) | Negative (`-`) | Total |
| --- | ---: | ---: | ---: |
| Lied (`L`) | 42 | 9 | 51 |
| Did not lie (`not L`) | 15 | 32 | 47 |
| Total | 57 | 41 | 98 |

Choose the actual state first, then the test result:

```text
Start
|- L (51/98)
|  |- + (42/51): 42/98
|  `- - (9/51): 9/98
`- not L (47/98)
   |- + (15/47): 15/98
   `- - (32/47): 32/98
```

The terminal paths sum to `98/98`. Sensitivity is `P(+ | L) = 42/51 = 0.824`; the reverse question is `P(L | +) = 42/57 = 0.737`, because its reference set is the 57 positive results. Bayes verifies it:

```text
P(L | +)
  = [(42/51)(51/98)] / [(42/51)(51/98) + (15/47)(47/98)]
  = (42/98)/(57/98) = 42/57 = 0.737.
```

Specificity is `P(- | not L) = 32/47 = 0.681`. A positive result's correctness also depends on base rate and false positives. The same-trial union `P(+ or L) = (42 + 15 + 9)/98 = 66/98` is not sequential multiplication.

## Key Takeaways (3-7 actionable)

- Define the procedure, sample space, event, and reference set before choosing a formula.
- Use complements for "not" and "at least one" when the none case is easier.
- For "or," check overlap; for sequential "and," check whether the next probability changes.
- Put the condition after the bar and use it as the denominator.
- Decide whether order matters before using permutations or combinations; simulate when exact counting is impractical.
- Treat a rare result as evidence against an assumption, not proof of an explanation.

## Connects To

- **Inferential statistics and hypothesis testing:** The rare event rule supplies the logic for questioning a null assumption.
- **Binomial probability and sampling:** Independent-trial multiplication, counting, replacement, dependence, and the 5% guideline support later models.
- **Medical testing and forensic reasoning:** Conditional probability, Bayes, sensitivity, specificity, and base rates govern how evidence changes a diagnosis or accusation.
- **Reliability and computational statistics:** Complements and independent failure probabilities quantify redundancy; simulation estimates probabilities when enumeration is difficult.
