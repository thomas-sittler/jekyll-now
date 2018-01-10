---
layout: post
title: "Regression anatomy"
---

[Valerio Filoso](http://fmwww.bc.edu/repec/bocode/r/reganat.pdf) writes:
>  Most econometrics textbooks limit themselves to providing the formula for the $$\beta$$ vector of the type
>  
>  $$\beta = (X′X)^{-1} X'Y.$$
>  
>  Although compact and easy to remember, this formulation is a sort black box, since it hardly reveals anything about what really happens during the estimation of a multivariate OLS model. Furthermore, the link between the $$\beta$$ and the moments of the data distribution disappear buried in the intricacies of matrix algebra. Luckily, an enlightening interpretation of the $$\beta$$s in the multivariate case exists and has relevant interpreting power. It was originally formulated more than seventy years ago by Frisch and Waugh (1933), revived by Lovell (1963), and recently brought to a new life by Angrist and Pischke (2009) under the catchy phrase regression anatomy. According to this result, given a model with K independent variables, the coefficient $$\beta$$ for the k-th variable can be written as 
>  
>  $$ \beta_k = \frac{cov(y,\tilde{x}_k)}{var(\tilde x)}$$
>  
>  where $$\tilde x_k$$ is the residual obtained by regressing $$x_k$$ on all remaining $$K − 1$$ independent variables.
>  
>  The result is striking since it establishes the possibility of breaking a multivariate model with K independent variables into $$K$$ bivariate models and also sheds light into the machinery of multivariate OLS. This property of OLS does not depend on the  underlying Data Generating Process or on its causal interpretation: it is a mechanical  property of the estimator which holds because of the algebra behind it.

Judd _et al._ (2017) have a [nice explanation](/images/multiple-regression-judd-et-al.pdf) of this too, pp.107-116.

I'm not sure how you would break a multivariate model with $$K$$ independent variables into $$K$$ bivariate models, it seems like you would need more. For example with three dependent variables and a constant ($$K=4$$), I worked out you need 5 base-level regressions (if you don't count the redundant ones in ligt blue) and 11 regressions of residuals on residuals. Am I missing something?

[![](/images/regression-anatomy.png)](images/regression-anatomy.png)

The cool thing is it does not matter in which order you add the independent variables. In my diagram, I start with just $$X_1$$ (equation [1]), then I add $$X_2$$ (equation [2]) and finally I add $$X_3$$ (equation [3]), but we could have done it in any of six ways.



<hr> <!-- hr to be added before footnotes--> 