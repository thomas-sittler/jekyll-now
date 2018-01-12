---
layout: post
title: "Diagrams of linear regression"
---

I made a big diagram describing some assumptions (MLR1-6) that are used in linear regression. In my diagram, there are five categories (in rectangles with dotted lines) of mathematical facts that follow from different subsets of MLR1-6.

[![thelinearmodel](/images/linear-regression-diagram.png)](/images/linear-regression-diagram.png)

In the diagram, I stick to the brute mathematics. But of course what really matters is the causal interpretation. As Pearl (2009) writes, “behind every causal claim there must lie some causal assumption that is not discernible from the joint distribution and, hence, not testable in observational studies”. Interpreting $$\beta$$ (and hence $$\hat{\beta}$$) causally means MLR4 becomes a (strong) causal assumption.

Typically in econometrics, giving a causal interpretation is done thus: 
* MLR1 holds in every possible world (alternatively: it specifies not just actual, but all potential outcomes), hence $$U$$ is unobservable even in principle
* yet we make assumption MLR4 about $$U$$

Pearl’s method is more explicit: replace $$MLR\{1 \quad 4\}$$ with the causal graph below, where $$:=$$ is used to make it extra clear that the causation only runs one way. MLR1 corresponds to the expression for $$Y$$ (and, redundantly, the two arrows towards $$Y$$), MLR4 corresponds to the absence of arrows connecting $$X$$ and $$U$$. We thus avoid “hiding causal assumptions under the guise of latent variables” (Pearl). (To see me rant about this, see [here](/econometrics-notation/#inconsistent-causal-language).)

![](/images/regression-causal-diagram.png)

The second diagram gives the asymptotic distribution of the IV estimator.

[![iv](/images/instrumental-variables.png)](/images/instrumental-variables.png)

<hr> <!-- hr to be added before footnotes-->