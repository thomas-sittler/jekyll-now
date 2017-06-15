# CDT is underspecified
Standard causal decision theory is underspecified. It needs a theory of counterfactuals reasoning. 

Suppose we are given the set of possible actions an agent could take in a situation. The agent will in fact choose only one of those actions. What would have happened under each of the other possible actions? We can think of the answer to this question as a list of counterfactuals.

One attempt, modelled on Arntzenius (2008):

Start by figuruing out what all the possible lists of counterfactuals K are. Then for each possible K, figure out what the expected utility: 

$$E[U_K(A)]= \sum_{j}Cr(O_j | A \land K)*U(O_j)$$

of each of your acts A is. Then, take the average of these expected utilities, weighted by your credence in each list of counterfactuals:

$$E[U(A)]=\sum_{K} Cr(K) * E[U_K(A)]$$

# Sox-Yankees
Now let's consider the following case, also from Arntzenius (2008):
> Harry is going to bet on the outcome of a Yankees versus Red Sox game. Harry’s credence that the Yankees will win is 0.9. He is offered the following two bets, of which he must pick one: 
>
> (1) A bet on the Yankees: Harry wins $1 if the Yankees win, loses $2 if the Red
Sox win
>
> (2) A bet on the Red Rox: Harry wins $2 if the Red Sox win, loses $1 if
the Yankees win.

What are the possible Ks? According to Arntzenius, they are:

(A,B): Yankees Win, Red Sox Win
(C,D): I win my bet, I lose my bet

But these are not lists of counterfactuals. How can we sharpen this? 

K_1:

$$(p=0.9)(u=+1)$$Harry bets on the Yankees $$\boxright$$ the Yankees win.

$$(p=0.1)(u=-2)$$Harry bets on the Yankees $$\boxright$$ the Sox win.

$$(p=0.9)(u=-1)$$Harry bets on the Sox $$\boxright$$ the Yankees win.

$$(p=0.1)(u=+2)$$Harry bets on the Sox $$\boxright$$ the Sox win.

--> bet on the Yankees

K_2:

$$(p=0.9)(u=+1)$$Harry bets on the Yankees $$\boxright$$ he wins his bet.
$$(p=0.1)(u=-2)$$Harry bets on the Yankees $$\boxright$$ he loses his bet.
$$(p=0.9)(u=-1)$$Harry bets on the Sox $$\boxright$$ he loses his bet.
$$(p=0.1)(u=+2)$$Harry bets on the Sox $$\boxright$$ he wins his bet.

--> bet on the yankees

So: I do not understand the claim that the causal decision theorist using K_2 will bet on the Sox and lose money.

# Sox/Yankees with a predictor
Now:
> [...] on each occasion before she chooses which bet to place, a perfect predictor of her choices and of the outcomes of the game announces to her whether she will win her bet or lose it.

According to Arntzenius, in this case EDT predictably loses money. This is denied by Ahmed and Price.

According to Arntzenius, in this case CDT (with the appropriate partition) predictably wins money. 

# the value of WAYR arguments
Some people say that in Newcomb cases, rational people predictably lose money. They are using the word "rational" in a way I find unhelpful. The reason I am interested in decision theory is so that I can get rich, not so that I can satisfy some platonic notion of rationality. Another way to see this: if we were programming an artificial intelligence, we would want to give it a decision theory that will allow it to get rich. A "rational" artificial intelligence that loses me money would be of little interest to me. 

So WAYR arguments are good, _contra_ Arntzenius. 

But this raises a problem: suppose god zaps you with an electric shock every time you use decision theory X on a Tuesday. So you should not use X, because bad things will happen. Instead, you should use the decision theory X*, which says "Use X from Wednesday to Monday. On Tuesday, use some other decision theory". 

But suppose that god now says he will zap you every time you use X* on a Tuesday. In this case, it would be better to use CDT instead of X*. 

Since X can be any decision theory, this shows that there exists no decision theory which works well in all cases. So we need to be pragmatic and choose the decision theory that works best given the cases we expect to face. But this just means using the meta-decision theory that tells you to do that. 