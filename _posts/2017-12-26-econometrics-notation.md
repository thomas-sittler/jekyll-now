---
layout: post
title: Econometric adventures
date: 2017-12-26 22:43
---

I took Oxford's advanced undergraduate econometrics course. My experience of the course, and really of the entire field, was the following: the concepts are simple, the real challenge is making sense of notation so obfuscatory that you wonder if it's done on purpose.

In order to arrive at this view, I went through a long and confusing journey, one I wish upon no friend. This document's structure takes my journey in reverse order.[^history] I start with what I eventually pinned down as the clear mathematical facts. Once armed with this toolkit, I do my best to explain why standard notation is confusing, and attempt to guess, from context, what econometricians actually mean.

The examples I give really are of standard practice. I give quotes from a few textbooks and our lecture slides, but I promise that you will find the same thing almost everywhere. And the confusing usages are not just a convenience of notation that is readily acknowledged in conversation. When I asked people about this in person, all I got were long, confusing back-and-forths.

<!-- In my view, it's an indictment of the field that I spent about _ten times longer_ engaging in this interpretative guesswork than I spent understanding the underling concepts. -->

[^history]: For the curious, or those who have to much time on their hands, I include a [full version history](https://github.com/thomas-sittler/thomas-sittler.github.io/tree/master/regression-history), showing how this document evolved. It could be an interesting window into my thought process. 

# Contents
{: .no_toc}
1. toc
{:toc}

# The facts
## Preliminaries
We start with a set of ordered pairs $$\{ \langle X_1 , Y_1 \rangle,\langle X_2 , Y_2 \rangle,\langle X_3 , Y_3 \rangle, ..., \langle X_n,Y_n \rangle\}$$. 

You can think of $$X_i$$ and $$Y_i$$ as 
* real numbers (facts about each of the the $$n$$ individuals in the population) 
* or as random variables (probability distributions over facts about $$n$$ individuals in a sample), 

all the maths will apply equally. (I will return to this fact and comment on it).


## The conditional expectation function minimises  $$\sum w_i^2$$
### Some algebraic facts
We write the equality:

$$Y_i = f(X_i) + w_i $$

Where $$Y_i$$ and $$X_i$$ are known, but $$w_i$$ depends on our choice of $$f$$.

### Minimisation problem
Suppose we want to solve

$$\min_{f(X_i)}  \sum w_i^2 \leftrightarrow \min_{f(X_i)}  \sum(Y_i-f(X_i))^2$$

The solution is $$f(X_i)=E[Y_i \mid X_i]$$, that is, $f$ is the conditional expectation function (CEF). The proof of this is in appendix A. Suppose we specify $$f(X_i)$$ as such, we then get:

$$ Y_i = E[Y_i \mid X_i] + w_i $$

Now $$f$$ is known and $$w_i$$ is known (by the subtraction $$w_i = Y_i - E[Y_i \mid X_i]$$).


##  The linear regression model minimises $$\sum (e_i + w_i)^2$$
### Some algebraic facts

Now we write the following equality:

$$ E[Y_i \mid X_i] = \beta_0 +\beta_1 X_i + e_i $$

This says that $$E[Y_i \mid X_i]$$ is equal to a linear function of $$X_i$$ plus some number $$e_i$$.

We then have

$$ \begin{array}{ll}
Y_i &= E[Y_i \mid X_i] + w_i \\
    &= \beta_0 +\beta_1 X_i + e_i + w_i
\end{array} $$

As before $$w_i$$ is known, whereas $$e_i$$ is a function of $$\beta_0$$ and $$\beta_1$$. 

Here $$e_i$$ is the distance, for observation $$i$$, between the linear regression model (LRM) and the CEF; while $$w_i$$ is the distance between the CEF and the actual value of $$Y_i$$. We can then call $$u_i = e_i + w_i$$ the distance between the LRM and the actual value.[^gripe]

We can also see that $$E[u_i \mid x_i] =0$$ is equivalent to $$e_i=0$$, i.e. the CEF and the LRM occupy the same coordinates.

[^gripe]: As a separate gripe from the main one in this post, I note that often what I call $$e_i+w_i$$ is just written as $$w_i$$, by this I mean that in the same document, people will write $$Y_i = \beta_0 + \beta_1X_i + w_i$$ _and_ $$Y_i = E[Y_i \mid X_i] + w_i$$. This is either a terrible choice of notation (same name for two different objects) or an implicit and unnecessary (in this case) assumption that $$e_i=0$$ and $$u_i = w_i$$.

### Minimisation problem
Suppose we want to solve

$$ \min_{\beta_0, \beta_1} \sum (e_i + w_i)^2 \leftrightarrow \min_{\beta_0, \beta_1} \sum (Y_i  - \beta_0 -\beta_1 X_i)^2 $$

The solution is 

$$
\begin{aligned}
\beta_0 &= \bar{y}- \beta_1\bar{x} \\
\beta_1 &= \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2}
\end{aligned}
$$

I prove this in appendix B. (It's possible to prove an analogous result in general using matrix algebra, see appendix C.)

Suppose we specify that $$\beta_0$$ and $$\beta_1$$ are equal to these solution values. Now that $$\beta_0$$ and $$\beta_1$$ are known, $$e_i$$ is known too (by the subtraction $$e_i = E[Y_i \mid X_i] - \beta_0 -\beta_1X_i$$). As before, $$w_i$$ is known.

Thus, in our regression equation,

$$
\begin{aligned}
Y_i &= \beta_0 + \beta_1 X_i + e_i + w_i \\
&= \beta_0 + \beta_1 X_i + u_i
\end{aligned}
$$

all of $$Y_i$$, $$X_i$$, $$\beta_0$$, $$\beta_1$$, $$e_i$$ and $$w_i$$ (and thus $$u_i$$), are known.

# Comments
Two things to note about the facts above. 

* Whether we are using real numbers of random variables does not matter for anything we've said so far. All we have used are the expectation and summation operators and their properties. Textbooks often warn about the important distinction between the sample and the population, but as far as these algebraic facts are concerned the difference is immaterial!
* I have not used "hat" notation (as in $$\hat{\beta}$$). Instead I have described the results of optimisation procedures carefully using words, like "the solution to this minimisation problem is ...". The way standard econometrics uses the hat is a good example of obfuscatory notation.

# Hermeneutics I: the hat symbol
## Inconsistent hats
Econometrics textbooks, within the same sentence or paragraph, routinely use the hat in two ways which seem to me to be incompatible.

### Sample analogues?
In Stock and Watson, p. 158, we have Claim A:
> The linear regression model is:
> 
> $$Y_i = \beta_0 + \beta_1 X_i + u_i$$
>
> Where $$\beta_0 + \beta_1 X$$ is the population regression line or population regression function, $$\beta_0$$ is the intercept of the population regression line, and $$\beta_1$$ is the slope of the population regression line. 

And Stock and Watson, p. 163 gives Claim B:
> The OLS estimators, $$\hat{\beta_0}$$ and $$\hat{\beta_1}$$, are sample counterparts of the population coefficients $$\beta_0$$ and $$\beta_1$$. Similarly, the OLS regression line $$\hat{\beta_0} + \hat{\beta_0}X$$ is the sample counterpart of the population regression line $$\beta_0 + \beta_1 X$$ and the OLS residuals $$\hat{u_i}$$ are sample counterparts of the population errors $$u_i$$. 

So far so good.

### Loss function minimisers?

Stock and Watson, p. 187 (Claim C):
> The OLS estimators, $$\hat{\beta_0}$$ and $$\hat{\beta_1}$$ are the values of $$b_0$$ and $$b_1$$ that minimise $$\sum_{i=1}^n (Y_i - b_0 - b_1 X_i)^2$$. 

This quote is the biggest culprit. After many conversations, I finally understood that we're supposed to take the quote to mean:

> The OLS estimators, $$\hat{\beta_0}$$ and $$\hat{\beta_1}$$ are the values of $$b_0$$ and $$b_1$$ that minimise $$\sum_{i=1}^j (Y^{sample}_i - b_0 - b_1 X^{sample}_i)^2$$, where $$j$$ is the number of observations in the sample ($$j<n$$ if $$n$$ is the population size) and  $$Y^{sample}_i$$ and $$X^{sample}_i$$ are the $$i$$th values in the sample.

I swear, I'm not taking this quote out of context! Nowhere, in the entire textbook, would you find a clue that the $$X_i$$ and $$Y_i$$ in claim C are _completely different quantities_ than $$X_i$$ and $$Y_i$$ in claim A. This is criminal negligence. (I'm also not cherry-picking. My lecture notes cheerfully call $$\hat{\beta_0}$$ and $$\hat{\beta_1}$$ the 'OLS' solutions, and this usage is standard.)

Of course, I'm the kind of person to take claim C at face value, and combine it with claim A, to arrive at $$\beta_0 = \hat{\beta_0}$$ and $$\beta_1= \hat{\beta_1}$$, which, I gathered from context, was _not_ a desirable conclusion.

## Confusing hats
The following is not as bad as the above, since it avoids explicit contradiction, but still sows confusion by using the hat to mean different things when put on top of different values. 

Claim D, from Stock and Watson p. 163:
> The predicted value of $$Y_i$$, given $$X_i$$, based on the OLS regression line, is $$\hat{Y_i} = \hat{\beta_0} + \hat{\beta_1}X_i$$. 

This is compatible with the loss function minimiser usage of the hat: claim C, which us $$\hat\beta_0$$ and $$\hat\beta_1$$ are loss function minimisers; claim D then tells us that $$\hat{Y_i}$$ is the value obtained when you compute the values of $$b_0$$ and $$b_1$$ which minimise a loss function, and plug them into the regression function.

But, of course, this "predicted value" verbiage is incompatible with the sample analogue usage. $$\hat Y_i$$ can't be both the predicted value (whether in a sample or not) and the _actual_ value in a sample. That would imply that predictions are always perfect!

So _even if_ we amend claim C as I've done above, we still can't say that the hat is consistently used to mean sample analogue, since in the case of $$\hat Y_i$$ it's apparently used to mean predicted value. (More specifically predicted value _in a sample_, one guesses from context).

# Inconsistent causal language
Here is an entirely separate category of wrongdoing. In all of the above we have taken the statement

$$
Y_i = \beta_0 + \beta_1 X_i + u_i
$$

to be an innocuous equality: $$Y_i$$ is equal to regression intercept, plus regression slope times $$X_i$$, plus some remaining difference. Call this this the _algebraic claim_.

But it turns out that the statement is sometimes used to make a completely different, and incredibly strong, causal claim. Econometricians [switch between the two usages](http://slatestarcodex.com/2014/11/03/all-in-all-another-brick-in-the-motte/). 

In keeping with the above structure, I'll start by clearly stating the causal claim, then I'll analyse quotes which trade on the ambiguity between the causal and algebraic claims. 

## The causal claim

We think of

$$
Y_i = \beta_0 + \beta_1 X_i + u_i
$$

Not as a regression equation, but as a complete causal account of everything causally affecting $$Y$$. (Sometimes the equation is said to describe the _data generating process_, which packs a big claim into an innocuous-sounding phrase). For example, if there are $$\phi$$ things causally affecting $$Y$$, we have:

$$
Y_i = \beta_0 + \beta_1 X_i + \beta_2A_i + \beta_3 B_i + ... + \beta_\phi \Omega_i
$$

We can think of this claim as equivalent to an infinite lists of counterfactuals, giving the potential values of $$Y$$ for every combination of values of the causal factors $$X,A,B...,\Omega$$.[^determinism] It also makes the claim that nothing else has a causal effect on $$Y$$ and that the causal effects are the same for every individual (since there are no $$i$$ subscripts on $$\beta_1,\beta_2,...\beta_\phi$$). The coefficient $$\beta_1$$ is certainly _not_ the value that minimises $$\sum_i(Y_i - \beta_0 - \beta_1 X_i)^2$$, it is the true causal effect of $$X$$.

[^determinism]: If we think the world is non-deterministic, the claim becomes $$Y_i = \beta_0 + \beta_1 X_i + \beta_2A_i + \beta_3 B_i + ... + \beta_\phi \Omega_i + \varepsilon_i$$, where $$\varepsilon_i$$ are random variables, and we have a list of counterfactuals giving the potential _distributions_ of $$Y$$ for every combination of values of the causal factors. (I'm not super sure about this).

That's a rather huge claim. In any realistic case, causal chains are incredibly long and entangled, so that basically everything affects everything else in some small way. So the claim often amounts to an entire causal model of the world.

# Hermeneutics II: causation in sheep's clothing
In the first part, I have restricted my attention to the confusions that arise when taking the algebraic interpretation as given. This interpretation is by far the most natural one. Regression is a mathematical operation, "$$=$$" is an algebraic symbol, and so on. Phrases like "slope of the population regression line" are routinely used while no hint is ever made at any causal meaning of the claim $$Y_i = \beta_0 + \beta_1 X_i + u_i$$. But you'll see below many claims which only make sense under the causal interpretation.

## Algebra or causes?
Stock and Watson p. 158, claim E: 
> The term $$u$$ is the error term [...]. This term
contains all the other factors besides $$X$$ that determine the value of the dependent variable, $$Y$$,
for a specific observation $$i$$

This is a favourite trick: use a word like "determines", which heavily implies a causal claim, but stay just shy of being unambiguously causal. That way you can always retreat to the algebraic claim. (Other favourites which I see _all the time_ in published papers are "contributes to", "is associated with", "explains", "influences"...).

Indeed, under the algebraic interpretation, claim E is puzzling. What on earth does it mean for a number to "contain", "factors" that "determine" the value of another number? As far as the mathematics is concerned, we have no concept of "determine", much less of a number "containing" another number.

A causal variant of claim E would be:
> The term $$u$$ is the further-causes term [...]. This term
contains all the other factors besides $$X$$ that cause the value of the dependent variable, $$Y$$,
for a specific observation $$i$$

Wooldrige, p.92f, claim F:
> Assumption MRL.4:
> > $$E[u \mid x_1, x_2, x_3 , ... , x_k]=0$$
>
> When assumption MLR.4 holds, we often say that we have **exogenous explanatory variables**. If $$x_j$$ is correlated with $$u$$ for any reason, then $$x_j$$ is said to be an **endogenous explanatory variable** [...] Unfortunately, we will never know for sure whether the average value of the unobservables is unrelated to the explanatory variables.

Under the algebraic interpretation, MLR.4 is the claim that the conditional expectation function is exactly the regression line. (In the notation I use above, $$e_i=0$$). This is a pretty strong claim, but has nothing to do with exogeneity. The exogeneity part of Claim F only makes sense under the causal interpretation, and I suspect that in the end we are to take Claim F causally. In that case, Claim F uses the language or correlation ("if $$x_j$$ is correlated with $$u$$ for any reason") to make an extremely strong causal claim, inviting confusion.  

While some parts of claim F seem to require the causal interpretation, the phrase "error term" in claim E calls for the algebraic one. And most of the quotes from part one, such as claims A and B, which call $$Y_i = \beta_0 + \beta_1 X_i + u_i$$ the "population regression function", rely on the algebraic claim.

Stock and Watson, p.131, claim G:
> The causal effect of a treatment is the expected effect on the outcome of interest of the treatment as measured in a ideal randomized controlled experiment. This effect can be expressed as the difference of two conditional expectations. Specifically, the causal effect on $$Y$$ of treatment level $$x$$ is the difference in the conditional expectations $$E[Y \mid X=x] - E[Y \mid X=0]$$    where $$E[Y\mid X=x]$$ is the expected value of of $$Y$$ for the treatment group (which received treatment level $$X=x$$) in an ideal randomized controlled experiment and $$E[Y \mid X=0]$$ is the expected value of $$Y$$ for the control group (which receives treatment level $$X=0$$).

Stock and Watson, p. 170, claim H:
> The first of the three least squares assumptions is that the conditional distribution of $$u_i$$ given $$X_i$$ has a mean of zero. This assumption is a formal mathematical statement about the "other factors" contained in $$u_i$$ and asserts that these other factors are unrelated to $$X_i$$ in the sense that, given a value of $$X_i$$, the mean of the distribution of these other factors is zero.

Claim G is good because there is appropriate hedging: causal effects are the difference between conditional expectations only in an idealised RCT. An idealised RCT is the only case where where the causal claim and the algebraic claim have the same meaning. 

In claim H however, the sentence "This assumption is a formal mathematical statement about the "other factors" contained in $$u_i$$" trades on the ambiguity between the algebraic and causal claims. Mathematical statements are about sums and products, not about causality in the world. This kind of writing promotes a kind of magical thinking in which, say, the expectation operator (really just a sum) can tell us about the what we would causally "expect" to see if we intervened on the world.

## Knowns or unknowns?
I want to go back to a part of claim F, which I did not discuss above:
> Unfortunately, we will never know for sure whether the average value of the unobservables is unrelated to the explanatory variables.

We see the same talk of unobservables in the University of Oxford Econometrics lecture slides, Michaelmas Term 2017, (claim J):
> The simple regression model  
> $$y_i = \beta_1 x_i + \beta_2 + u_i$$  
> * $$y_i$$ and $$x_i$$ are observable random scalars
> * $$u_i$$ is the unobservable random disturbance or error
> * $$\beta_1$$ and $$\beta_2$$ are the parameters (constants) we would like to estimate

On the causal usage, $$u_i$$ are indeed practically impossible to observe. But then so are $$\beta_1$$ and $$\beta_2$$, but these are simply called parameters, and not unobservables.

However, on the algebraic usage (combined with taking $$\beta_1$$ and $$\beta_2$$ to be loss function minimising coefficients), if $$y_i$$ and $$x_i$$ are known, so are $$\beta_1$$ and $$\beta_2$$, and by a simple subtraction, $$u_i$$ is known too.

We can see the same phenonemon even more clearly with $$Y_i = E[Y_i \mid X_i] + w_i$$. This is equality is always discussed under the algebraic usage. If we know $$Y_i$$ and $$X_i$$ we can obviously get $$w_i$$ by a subtraction. Yet econometricians insist on calling $$w_i$$ unknown; they are laying the groundwork to hoodwink you later by switching to the causal usage. 

# Appendix A
Proof that the solution to

$$ \min_{f(X_i)} E[u_i^2] \leftrightarrow \min_{f(X_i)} E[(Y_i-f(X_i))^2] $$

is $$f(X_i)=E[Y_i \mid X_i]$$.

$$\square$$ Taking the first-order condition:

$$
\begin{aligned}
 \frac{d E[(Y_i-f(X_i))^2]}{df(X_i)} &=0 \\ E[\frac{d (Y_i-f(X_i))^2}{df(X_i)}] &=0 \\ E[\frac{Y_i^2 -2Y_if(X_i)+f(X_i)^2}{df(X_i)}] &= 0 \\ E[-2Y_i+2f(X_i)] &=0 \\ E[-2Y_i+2f(X_i) \mid X_i] &=0 \\ -2E[Y_i \mid X_i] + 2f(X_i) &=0 \\ f(X_i) &= E[Y_i \mid X_i] \qquad \blacksquare
\end{aligned}
$$


# Appendix B
Proof that the solution to

$$
\min_{\beta_0, \beta_1} E[(e_i + u_i)^2] \leftrightarrow \min_{\beta_0, \beta_1} E[(Y_i  - \beta_0 -\beta_1 X_i)^2] 
$$

is

$$
\begin{aligned}
\beta_0 &= \bar{y}- \beta_1\bar{x} \\
\beta_1 &= \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2}
\end{aligned}
$$


$$\square$$ Let

$$
L = \sum_{i=1}^n (y_i - \beta_1 - \beta_2 x_i)^2
$$

We solve:

$$
\begin{aligned}
&\min_{\beta_1, \beta_2} L \\
&\leftrightarrow 

\begin{cases}
\frac{dL}{d \beta_1} =0 \qquad \text{Call this }(a) \\

\frac{dL}{d \beta_2} =0 \qquad \text{Call this }(b)
\end{cases} \\

&\leftrightarrow \begin{cases}
\sum_{i=1}^n(\frac{d(y_i-\beta_1-\beta_2x_i)^2}{d \beta_1}) =0 \qquad \qquad \text{derivative of a sum}\\
(b)\end{cases} \\

&\leftrightarrow \begin{cases}\sum_{i=1}^n-2(y_i-\beta_1-\beta_2x_i) =0 \\

(b)\end{cases}\\&\leftrightarrow \begin{cases}\beta_1 = \bar{y} - \beta_2\bar{x} \\

(b)\end{cases}\\\\ \\

&\leftrightarrow \begin{cases}(a) \\

 \sum_{i=1}^n(\frac{d(y_i-\beta_1-\beta_2x_i)^2}{d \beta_2}) =0 \qquad \qquad \text{derivative of a sum}\end{cases} \\

 &\leftrightarrow \begin{cases}(a)\\\sum_{i=1}^n-2x_i(y_i-\beta_1-\beta_2x_i) =0\end{cases} \\

 &\leftrightarrow \begin{cases}(a)\\\sum_{i=1}^n-2x_i(y_i-\bar{y}+\beta_2\bar{x}-\beta_2x_i) =0 \qquad \qquad \text{substitute }\beta_1
 
 \end{cases} \\
 
  &\leftrightarrow \begin{cases}(a)\\\sum_{i=1}^n x_i(y_i-\bar{y}+\beta_2\bar{x}-\beta_2x_i) =0\qquad \qquad \text{divide by -2}\end{cases} \\

 &\leftrightarrow \begin{cases}(a) \\

   \sum_{i=1}^n x_i(y_i-\bar{y}) +\sum_{i=1}^n \beta_2 x_i(\bar{x} - x_i) =0 \qquad \qquad \text{rearrange}\end{cases} \\
 
 &\leftrightarrow \begin{cases}(a) \\

   \sum_{i=1}^n x_i(y_i-\bar{y}) =\sum_{i=1}^n \beta_2 x_i(x_i - \bar{x}) \qquad \qquad \text{rearrange}\end{cases} \\

 &\leftrightarrow \begin{cases}(a) \\

   \sum_{i=1}^n (x_i-\bar{x})(y_i-\bar{y}) =\sum_{i=1}^n \beta_2 (x_i - \bar{x})^2 \qquad \qquad \text{by fact A} \end{cases} \\

 &\leftrightarrow \begin{cases}(a) \\

           \beta_2  = \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2} \qquad \qquad \text{rearrange}\end{cases}


          \\ \\

          &\leftrightarrow \begin{cases}\beta_1 = \bar{y} - \beta_2\bar{x} \\

           \beta_2  = \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2} \end{cases}
\end{aligned}
$$

Thus we write:

$$
\begin{aligned} \hat{\beta_1} &= \bar{y} - \hat{\beta_2}\bar{x} \\

 \hat{\beta_2}  &= \frac{\sum_{i=1}^n(y_i-\bar{y})(x_i- \bar{x})}{\sum_{i=1}^n  (x_i- \bar{x})^2} \ \ \blacksquare \end{aligned}
$$

Fact A is proven here:

$$
\begin{aligned}
\sum_{i=1}^n (x_i-\bar{x})(y_i-\bar{y}) &= 
\sum_{i=1}^n(x_iy_i - x_i\bar{y} -\bar{x}y_i +\bar{x}\bar{y})  \\
&= \sum_{i=1}^n(x_iy_i) -\bar{y}\sum_{i=1}^n(x_i) -  \bar{x}\sum_{i=1}^n(y_i) + n\bar{x}\bar{y} \\
&= \sum_{i=1}^n(x_iy_i) -n\bar{y}\bar{x} - n\bar{y}\bar{x} + n\bar{x}\bar{y} \\
&= \sum_{i=1}^n(x_iy_i) -n\bar{y}\bar{x}  \\

&= \sum_{i=1}^n(x_iy_i) -\sum_{i=1}^ny_i\bar{x} & &= \sum_{i=1}^n(x_iy_i) -\sum_{i=1}^nx_i\bar{y}  \\

&= \sum_{i=1}^n y_i(x_i-\bar{x}) \qquad\text{factorise } y_i & &= \sum_{i=1}^n x_i(y_i-\bar{y}) \qquad\text{factorise } x_i
\end{aligned}
$$

A special case of fact A is:

$$
\sum_{i=1}^n (x_i-\bar{x})^2 =\sum_{i=1}^n x_i(x_i-\bar{x})
$$

# Appendix C
Proof that

$$
\begin{aligned}
\min_{\beta} U'U
& \leftrightarrow \beta = (X'X)^{-1} X'Y \\
\end{aligned}
$$

Where $$ Y=X\beta+U $$

and where

$$
Y = \begin{bmatrix}
  y_1 \\
  y_2 \\
  \vdots \\
  y_n
\end{bmatrix}
\qquad
X = \begin{bmatrix}
  1& x_{1,1} & x_{2,1} & \cdots & x_{K,1}\\
  1& x_{1,2} & x_{2,2} & \cdots & x_{K,2}\\
  \vdots &\vdots & \vdots & \ddots & \vdots \\
  1& x_{1,n} & x_{2,n} & \cdots & x_{K,n}
\end{bmatrix}
$$

$$
\beta= \begin{bmatrix}  \beta_0 & \beta_1 & \cdots & \beta_K \end{bmatrix}^T=\begin{bmatrix}
  \beta_0 \\
  \beta_1  \\
  \vdots \\
  \beta_K 
\end{bmatrix}

\qquad

U=\begin{bmatrix}
  u_1 \\
  u_2 \\
  \vdots \\
  u_n
\end{bmatrix}
$$

$$\square$$ Then
$$
U'U = \begin{bmatrix}  \sum_{i=1}^n u_i u_i
      \end{bmatrix} = SSR
$$

We can also write:

$$
\begin{aligned}
U'U &= (Y-X\beta)'(Y-X\beta) \\
&= (Y' -(X\beta)')(Y-X\beta) \\
&= Y'Y - Y'X\beta -(X\beta)'Y  +(X\beta)'(X\beta) \\
&= Y'Y - ((X\beta)'Y)' -(X\beta)'Y + \beta'X'X\beta \\
\end{aligned}
$$

Since $$(X\beta)'Y$$ is a scalar, it is equal to its transpose $$Y'X\beta$$. Thus:

$$
\begin{aligned}
U'U&= Y'Y -2Y'X\beta + \beta'X'X\beta
\end{aligned}
$$


We then solve:

$$
\begin{aligned}
\min_{\beta} U'U &\leftrightarrow 

\frac{dU'U}{d\beta}=0\\
& \leftrightarrow

\frac{dY'Y }{d\beta} -2\frac{d\ Y'X\beta}{d\beta}+ \frac{d\beta'X'X\beta}{d\beta} =0 \\
& \leftrightarrow 
0 -2(Y'X)' + (X'X+(X'X)')\beta =0 \\
& \leftrightarrow 
-2X'Y + 2X'X\beta =0 \\


& \leftrightarrow 
X'X\beta = X'Y \\
\end{aligned}
$$

Assuming that $$X'X$$ is invertible (since it's a square matrix, this is equivalent to $$det(X'X)\neq0$$), we have:

$$
\begin{aligned}
\min_{\beta} U'U
& \leftrightarrow \beta = (X'X)^{-1} X'Y  \ \ \blacksquare \\
\end{aligned} 
$$


<hr> <!-- hr to be added before footnotes--> 