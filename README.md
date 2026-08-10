# Direct Products in List Learning

## Abstract

How much harder is it to learn several independent targets from product samples? We resolve three direct-product questions for multiclass and list learning.

First, if $K(\mathcal{C})$ is the minimum list size for which a class is PAC learnable, then

$$K(\mathcal{C}_1\otimes\cdots\otimes\mathcal{C}_r)=\prod_{j=1}^r K(\mathcal{C}_j).$$

The previous bounds differed exponentially in $r$. The proof strengthens the known product lemma for list Daniely and Shalev-Shwartz dimensions from $\prod_j k_j$ to $\prod_j(k_j+1)-1$ neighbors.

Second, randomized fixed-marginal success obeys exact parallel repetition. Deterministic learning behaves differently. A joint deterministic learner can use the other tasks' samples as endogenous randomness and approach randomized parallel repetition, while independent deterministic learners have a strictly worse success exponent. For two copies of a two-concept problem, joint learning reduces the minimax error from $7/16$ to $1/4$.

Third, if a class has graph dimension $g$, its $r$-fold product has graph dimension at most $2gr\log_2(3r)$. The logarithm is necessary even for binary halfspaces. Hence uniform convergence can deteriorate by $\Theta(\sqrt{r\log r})$, and this is the sharp worst-case law.

## Main results

**Theorem (Exact product law for minimum list size).** The minimum list size of a product class is exactly the product of the minimum list sizes. Previously the known upper and lower bounds differed exponentially in the number of factors $r$, so the multiplicative law was not determined.

**Theorem (Randomized parallel repetition is exact).** With fixed marginals, randomized success multiplies exactly across independent tasks. This is the clean case.

**Theorem (Deterministic learners separate).** Deterministic learning does not follow the randomized law. A learner that sees all tasks jointly can treat the other tasks' samples as a source of endogenous randomness and approach the randomized exponent, while learners restricted to their own task cannot. On two copies of a two-concept problem the minimax error drops from $7/16$ to $1/4$ under joint learning, which is a concrete separation rather than an asymptotic one.

**Theorem (Sharp graph-dimension growth).** Graph dimension of an $r$-fold product is at most $2gr\log_2(3r)$, and the logarithmic factor cannot be removed, with binary halfspaces as the witness. The consequence for practice is that uniform convergence degrades by $\Theta(\sqrt{r\log r})$ in the worst case, and that rate is tight.

**Why the list-DS product lemma had to be strengthened.** The exact product law follows only after improving the neighbor count in the known product lemma for list Daniely and Shalev-Shwartz dimensions from $\prod_j k_j$ to $\prod_j(k_j+1)-1$. The weaker count is what produced the exponential gap in earlier bounds.

## Keywords

list learning, direct product theorems, multiclass learnability, PAC learning, sample complexity, list size, product classes, graph dimension, parallel repetition

## Files

- `main.pdf`, `supplement.pdf`
- `main.tex`, `supplement.tex`
- `references.bib`
- `aistats2027.sty`, `fancyhdr.sty`
- `main.pdf.ots`, `supplement.pdf.ots`, `README.md.ots` OpenTimestamps priority proofs
