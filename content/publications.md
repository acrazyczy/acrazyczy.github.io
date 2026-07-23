---
title: "Publications"
date: 2025-10-13
hidemeta: true
description: "Publications of Ziyi Cai"
---

---

**(α-β) stands for alphabetic order.**

---

## Preprints

<div class="publication-list">

<div class="publication-item">
  <div class="pub-title">Dense Language Generation Made Simple: Deterministic, Randomized, and Multi-Order Algorithms</div>
  <div class="pub-authors"><span class="my-name">(α-β)</span> <span class="my-name">Ziyi Cai</span>, Shuangping Li, Yiheng Shen, Kangning Wang, and Peng Zhang</div>
  <div class="pub-venue">In <span class="journal-name">Submission</span></div>
   <div class="pub-languages">
      <div class="pub-language">Online Algorithm</div>
      <div class="pub-language">Formal Languages</div>
      <div class="pub-language">Learning Theory</div>
        </div>
  <div class="pub-links">
    <input type="checkbox" id="lgtl-abstract-toggle" class="pub-abstract-checkbox" />
    <label for="lgtl-abstract-toggle" class="pub-button abstract">&#128221; Abstract</label>
   <div class="pub-abstract">
      <i>Language generation in the limit</i> is a theoretical framework for studying how a generator can learn to produce new valid strings from a stream of positive examples. In this model, an adversary chooses an unknown language from a countable family and enumerates its elements in an arbitrary order, while the generator must eventually output only elements of the language that have not yet appeared in the enumeration. Reliable generation is thus formalized through two eventual guarantees: validity and novelty relative to the observed data. To further quantify the breadth of the generator's outputs, Kleinberg and Wei (FOCS 2025, STOC 2026) introduced lower density as a measure of output coverage. Given an order representing the importance or relevance of possible outputs, lower density is the asymptotic lower bound, as $n$ grows, on the fraction of the first $n$ elements of the target language that the generator outputs before they appear in the data. Kleinberg and Wei showed that $1/2$ is the optimal lower-density guarantee for deterministic algorithms.

We develop a simple and unified framework for obtaining optimal lower-density guarantees. We first give a deterministic algorithm that recovers the optimal guarantee of $1/2$ with a significantly simpler analysis than prior work. We then demonstrate the flexibility of our framework through two extensions. First, against an oblivious adversary, randomization raises the optimal guarantee to $1-1/e$. Second, for any finite collection of orders, the optimal deterministic and randomized guarantees can be achieved simultaneously with respect to every order, so accommodating multiple notions of importance or relevance entails no loss in the optimal guarantee.
    </div>
<!-- <a href="https://arxiv.org/pdf/2602.08871" class="pub-button paper">&#128214; PDF</a> -->
  </div>
</div>


</div>

---

## Publications

<div class="publication-list">

<div class="publication-item">
  <div class="pub-title">Distortion of Metric Voting with Bounded Randomness</div>
  <div class="pub-authors"><span class="my-name">(α-β)</span> <span class="my-name">Ziyi Cai</span>, D. D. Gao, Prasanna Ramakrishnan, and Kangning Wang</div>
  <div class="pub-venue">In <span class="journal-name">Proceedings of the 27th ACM Conference
on Economics and Computation (EC)</span>, 2026</div>
   <div class="pub-languages">
      <div class="pub-language">Computational Social Choice</div>
      <div class="pub-language">Algorithmic Game Theory</div>
        </div>
  <div class="pub-links">
    <input type="checkbox" id="distortion-randomness-abstract-toggle" class="pub-abstract-checkbox" />
    <label for="distortion-randomness-abstract-toggle" class="pub-button abstract">&#128221; Abstract</label>
<a href="https://arxiv.org/abs/2602.08871" class="pub-button arxiv">
  <span class="pub-button-icon" aria-hidden="true">
    <img src="/icon/arxiv-logomark-small.svg" alt="" />
  </span>
  <span>arXiv</span>
</a>
   <div class="pub-abstract">
      We study the design of voting rules in the metric distortion framework. It is known that any deterministic rule suffers distortion of at least $3$, and that randomized rules can achieve distortion strictly less than $3$, often at the cost of reduced transparency and interpretability. In this work, we explore the trade-off between these paradigms by asking whether it is possible to break the distortion barrier of $3$ using only "bounded" randomness. We answer in the affirmative by presenting a voting rule that (1) achieves distortion of at most $3 - \varepsilon$ for some absolute constant $\varepsilon > 0$, and (2) selects a winner uniformly at random from a deterministically identified list of constant size. Our analysis builds on new structural results for the distortion and approximation of Maximal Lotteries and Stable Lotteries.
    </div>
<!-- <a href="https://arxiv.org/pdf/2602.08871" class="pub-button paper">&#128214; PDF</a> -->
  </div>
</div>

<div class="publication-item">
  <div class="pub-title">Weaver’s Discrepancy for Gaussian Random Vectors</div>
  <div class="pub-authors"><span class="my-name">(α-β)</span> <span class="my-name">Ziyi Cai</span>, Qing Chen, and Peng Zhang</div>
  <div class="pub-venue">In <span class="journal-name">SIAM Journal on Discrete Mathematics</span>, Volume 39, Issue 3, Sep 2025</div>
   <div class="pub-languages">
      <div class="pub-language">Discrepancy Theory</div>
        </div>
  <div class="pub-links">
    <input type="checkbox" id="weaver-abstract-toggle" class="pub-abstract-checkbox" />
    <label for="weaver-abstract-toggle" class="pub-button abstract">&#128221; Abstract</label>
    <a href="https://epubs.siam.org/doi/10.1137/24M1678878" class="pub-button paper">&#128214; Paper</a>
    <div class="pub-abstract">We study Weaver’s discrepancy for \(n\) independent and identically distributed Gaussian random vectors in \(d\) dimensions. Weaver’s discrepancy for a list of vectors is defined as the minimum operator norm of the signed sum of the vectors’ outer products among all possible sign choices. First, we establish that when \(d = O(1)\), with probability at least \(0.99\), Weaver’s discrepancy is \(\Theta (\sqrt {n} 2^{-\frac {2n}{d(d+1)}})\). Second, we demonstrate that for \(\Omega (n^{2/3}) = d=O(n)\), Weaver’s discrepancy is \(\Omega (d)\), and for \(\Omega (n^{0.01}) = d=O(n)\), the discrepancy is \(O(\sqrt {dn})\), both with high probability; these two bounds match when \(d = \Theta (n)\). Our proofs mainly utilize the first- and second-moment methods. One exception is that for the upper bound when \(d = O(n)\), we show that independently and uniformly chosen signs achieve this upper bound with high probability.
    </div>
  </div>
</div>
</div>
