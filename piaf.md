---
layout: post
title:
---
# CDT is underspecified
Standard causal decision theory is underspecified. It needs a theory of counterfactual reasoning. 

Suppose we are given the set of possible actions an agent could take in a situation. The agent will in fact choose only one of those actions. What would have happened under each of the other possible actions? We can think of the answer to this question as a list of counterfactuals.

Let's call such a list K of counterfactuals a "causal situation" (Arntzenius 2008). The list will have n elements when there are n possible actions. Start by figuring out what all the possible lists of counterfactuals K are. They form a set P which we can call the "causal situation partition". Once you have determined P, then for each possible K, figure out what the expected utility: 

$$E[U_K(A)]= \sum_{j}Cr(O_j | A \land K)*U(O_j)$$

of each of your n acts $$\{A_1,A_2,...,A_n\}$$ is. Then, take the average of these expected utilities, weighted by your credence in each causal situation:

$$E[U(A)]=\sum_{K} Cr(K) * E[U_K(A)]$$

Perform the act with the highest $$E[U(A)]$$.

What will turn out to be crucial for our purposes is that there is more than one causal situation partition P one can consistently use. So it's not just a matter of figuring out "the" possible Ks that form "the" P. We also need to choose a P among a variety of possible Ps.

In other words, there is the following hierarchy:
* Choose a causal situation partition P out of the set of possible partitions $$\{P_1,P_2,...,P_k\}$$ (the causal situation superpartition?).
* This partition defines a list of possible causal situations: $$P = \{K_1,K_2,...,K_j\}$$. 
* Each causal situation K defines a list of counterfactuals of length n: $$K = \{C_1,C_2,...,C_n\}$$. Where each counterfactual $$C_i$$ is of the form "$$A_i \boxright X$$". You have a credence distribution over Ks.

# Sox-Yankees
Now let's consider the following case, also from Arntzenius (2008):
> Harry is going to bet on the outcome of a Yankees versus Red Sox game. Harry’s credence that the Yankees will win is 0.9. He is offered the following two bets, of which he must pick one: 
>
> (1) A bet on the Yankees: Harry wins $1 if the Yankees win, loses $2 if the Red
Sox win
>
> (2) A bet on the Red Rox: Harry wins $2 if the Red Sox win, loses $1 if
the Yankees win.

What are the possible Ps? According to Arntzenius, they are:

P1: Yankees Win, Red Sox Win

P2: I win my bet, I lose my bet

To make this very explicit using the language I describe above, we can write that the set of causal situations (the "superpartition") is:

$$\{ P_b , P_w\}$$

($$P_b$$ for "baseball" and $$P_w$$ for "win/lose")

**Let's first deal with the baseball partition:**
$$P_b= \{K_y,K_s\}$$ 

($$K_y$$ for "Yankees win" and $$K_s$$ for "Sox win")

$$K_y = \{C_1,C_2     \}$$
$$K_s = \{C_3,C_4     \}$$

$$C_1 = \text{Harry bets on the Yankees} \boxright \text{Harry +1$}$$
$$C_2 = \text{Harry bets on the Sox} \boxright \text{Harry -1$}$$

$$C_3 = \text{Harry bets on the Yankees} \boxright \text{Harry -2$}$$
$$C_4 = \text{Harry bets on the Sox} \boxright \text{Harry +2$}$$

And Harry has the following credences[^cred]:
[^cred]: This isn't fully rigorous, since Ks are lists of (counterfactual) propositions, so you can't have a credence in a K. What I mean by $$Cr(K_y)=0.9$$ is that Harry has credence 0.9 in every C in K, and (importantly) he also has credence 0.9 in in their conjunction $$C_1 \land C_2$$. But I drop this formalism in the body of the post, which I feel already suffers from an excess of pedantry as it stands!

$$Cr(K_y)=0.9$$

$$Cr(K_s)=0.1$$

**And now for the win/lose partition:**
$$P_w= \{K_w,K_l\}$$ 

($$K_w$$ for "Harry wins his bet" and $$K_l$$ for "Harry loses his bet")

$$K_w = \{C_5,C_6     \}$$
$$K_l = \{C_7,C_8     \}$$

$$C_5 = \text{Harry bets on the Yankees} \boxright \text{Harry +1$}$$
$$C_6 = \text{Harry bets on the Sox} \boxright \text{Harry +2$}$$

$$C_7 = \text{Harry bets on the Yankees} \boxright \text{Harry -2$}$$
$$C_8 = \text{Harry bets on the Sox} \boxright \text{Harry -1$}$$

Now we come to the tricky question of what Harry's credences are in $$K_w$$ and $$K_l$$. Arntzenius writes: "It immediately follows that no matter what $$Cr(K_w)$$ and $$Cr(K_l)$$ are the expected utility of betting on the red sox is always higher". So Harry should bet on the red sox regardless of his credences. 

Suppose Harry reasons thus and bets on the Sox. But now, given that the Yankees win 90% of the time, Harry will immediately infer that $$Cr(K_l)=0.9$$. In other words, after he's made the decision, he immediately regrets it since doing so puts him in the postion of knowing he will lose money. So Harry violates what Arntzenius calls "weak desire reflection" if he uses the win/lose partition. 

# Sox/Yankees with a predictor
Now:
> [...] on each occasion before she chooses which bet to place, a perfect predictor of her choices and of the outcomes of the game announces to her whether she will win her bet or lose it.

Arntzenius crafts this thought experiment as a case where, purportedly:
* An evidential decision theories predictably loses money.[^ahmed]
* A causal decision theorist using the baseball partition predictably wins money. 

[^ahmed]:This is denied by Ahmed and Price

I'll leave both of these claims undefended for now, taking them for granted. The dialectical state of play is now: "EDT does predictably better than CDT in _Newcomb_. But CDT does predictably better than EDT in _Sox/Yankees with predictor_, provided that it uses the appropriate partition."

The problem is that so far we have not been given a general rule for how to choose one's partition from among the superpartition. A fully specified CDT needs to tell you which partition to use. And in order for the _Sox/Yankees with predictor_ case to have dialectical weight in favour of CDT, we need general rule for choosing partitions that determines that the correct partition is the baseball partition.

Here is Arntzenius' proposed rule:
> he diagnosis is that {C,D} is a bad
partition because its elements C and D are correlated to the acts that one is choosing
between, while the elements of the {A,B} partition are not. Here is what I mean.
Let’s suppose that we have a large population of causal decision theorists, that 50%
of them use the {A,B} partition, and 50% of them use the {C,D} partition. So 50%
will bet on the Yankees all the time, 50% will bet on the Red Sox all the time.
Suppose that the Yankees win 90% of the time. Then there will be no correlation
between the elements of the act partition (‘Bet on Yankees’, ‘Bet on Red Sox’) and
the elements of the {A,B} partition. But there will be a correlation between the
elements of the act partition (‘Bet on Yankees’, ‘Bet on Red Sox’) and the elements
of {C,D} partition. For, among all the bets that are placed on the Yankees, 90% of
them are placed in cases in which the Yankees win, and among all the bets that are
placed on the Red Sox, also 90% of them are placed in cases in which the Yankees
win. So there is no correlation between the act partition and the {A,B} partition.
However, among of all the bets that are placed on the Yankees 90% are cases in
which that bet wins, while among all the bets that are placed on the Red Sox,
only10% are cases in which that bet wins. This is why the {C,D} partition is a bad
partition.

He gives explains why the rule gives a good result the Yankees/Sox case. But what is crucial here is that the rule give a good result for the _Sox/Yankees with predictor_ case. At first I thought there was a flaw in the reasoning and that the rule would not be applicable to the latter case. But now I think Arntzenius is correct.

The rule in Newcomb cases: the predictor forces there to be a correlation. So the rule does not identify a partition to chose.

Thus, it seems right that neither EDT nor CDT has a clear dialectical upper hand. But we already knew this from the classic Smoking lesion case. So I don't know why the hell Frank bothered with the whole Sox/Yankees case!

# the value of WAYR arguments
Some people say that in Newcomb cases, rational people predictably lose money. They are using the word "rational" in a way I find unhelpful. The reason I am interested in decision theory is so that I can get rich, not so that I can satisfy some platonic notion of rationality. Another way to see this: if we were programming an artificial intelligence, we would want to give it a decision theory that will allow it to get rich. A "rational" artificial intelligence that loses me money would be of little interest to me. 

So WAYR arguments are good, _contra_ Arntzenius. 

But this raises a problem: suppose god zaps you with an electric shock every time you use decision theory X on a Tuesday. So you should not use X, because bad things will happen. Instead, you should use the decision theory X*, which says "Use X from Wednesday to Monday. On Tuesday, use some other decision theory". 

But suppose that god now says he will zap you every time you use X* on a Tuesday. In this case, it would be better to use CDT instead of X*. 

Since X can be any decision theory, this shows that there exists no decision theory which works well in all cases. So we need to be pragmatic and choose the decision theory that works best given the cases we expect to face. But this just means using the meta-decision theory that tells you to do that.  