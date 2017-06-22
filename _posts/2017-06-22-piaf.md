---
layout: post
title:  "Why ain't causal decision theorists rich? Some speculations"
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
* Each causal situation K defines a list of counterfactuals of length n: $$K = \{C_1,C_2,...,C_n\}$$. Where each counterfactual $$C_i$$ is of the form "$$A_i \mathbin{\square\!\mathord\to} X$$". You have a credence distribution over Ks.

# Sox-Yankees
Now let's consider the following case, _Game_ also from Arntzenius (2008):
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

$$C_1 = \text{Harry bets on the Yankees} \mathbin{\square\!\mathord\to} \text{Harry +1\$}$$
$$C_2 = \text{Harry bets on the Sox} \mathbin{\square\!\mathord\to} \text{Harry -1\$}$$

$$C_3 = \text{Harry bets on the Yankees} \mathbin{\square\!\mathord\to} \text{Harry -2\$}$$
$$C_4 = \text{Harry bets on the Sox} \mathbin{\square\!\mathord\to} \text{Harry +2\$}$$

And Harry has the following credences[^cred]:

[^cred]: This isn't fully rigorous, since Ks are lists of (counterfactual) propositions, so you can't have a credence in a K. What I mean by $$Cr(K_y)=0.9$$ is that Harry has credence 0.9 in every C in K, and (importantly) he also has credence 0.9 in in their conjunction $$C_1 \land C_2$$. But I drop this formalism in the body of the post, which I feel already suffers from an excess of pedantry as it stands!

$$Cr(K_y)=0.9$$

$$Cr(K_s)=0.1$$

**And now for the win/lose partition:**
$$P_w= \{K_w,K_l\}$$ 

($$K_w$$ for "Harry wins his bet" and $$K_l$$ for "Harry loses his bet")

$$K_w = \{C_5,C_6     \}$$

$$K_l = \{C_7,C_8     \}$$

$$C_5 = \text{Harry bets on the Yankees} \mathbin{\square\!\mathord\to} \text{Harry +1\$}$$
$$C_6 = \text{Harry bets on the Sox} \mathbin{\square\!\mathord\to} \text{Harry +2\$}$$

$$C_7 = \text{Harry bets on the Yankees} \mathbin{\square\!\mathord\to} \text{Harry -2\$}$$
$$C_8 = \text{Harry bets on the Sox} \mathbin{\square\!\mathord\to} \text{Harry -1\$}$$

Now we come to the tricky question of what Harry's credences are in $$K_w$$ and $$K_l$$. Arntzenius writes: "It immediately follows that no matter what $$Cr(K_w)$$ and $$Cr(K_l)$$ are the expected utility of betting on the red sox is always higher". So Harry should bet on the red sox regardless of his credences. 

Suppose Harry reasons thus and bets on the Sox. But now, given that the Yankees win 90% of the time, Harry will immediately infer that $$Cr(K_l)=0.9$$. In other words, after he's made the decision, he immediately regrets it since doing so puts him in the postion of knowing he will lose money. So Harry violates what Arntzenius calls "weak desire reflection" if he uses the win/lose partition. 

# Sox/Yankees with a predictor
Now consider the case _Predictor_:
> [...] on each occasion before she chooses which bet to place, a perfect predictor of her choices and of the outcomes of the game announces to her whether she will win her bet or lose it.

Arntzenius crafts this thought experiment as a case where, purportedly:
* An evidential decision theories predictably loses money.[^ahmed]
* A causal decision theorist using the baseball partition predictably wins money. 

[^ahmed]:This is denied by Ahmed and Price

I'll leave both of these claims undefended for now, taking them for granted. I'll also skip over how one is supposed to systematically determine which partition is the "correct" one[^sec6].  What is the point of proposing _Predictor_? We know that EDT does predictably better than CDT in _Newcomb_. _Predictor_ is a case where CDT does predictably better than EDT, provided that it uses the appropriate partition. But we already knew this from more mundane cases like _Smoking lesion_ ([Egan 2007](http://www.jstor.org/stable/20446939)). 

[^sec6]: Arntzenius provides an answer in section 6, "Good and Bad Partitions".


# the value of WAYR arguments
Arntzenius' view appears to be that "Why ain'cha rich?"-style arguments (henceforth WAYRs) give us no reason to choose _any_ decision theory over another. 

One way to think of decision theory is as a conceptual analysis of the word "rational", i.e. a theory of rationality. Some causal decision theorists say that in _Newcomb_, rational people predictably lose money. But this, they say, is not an argument against CDT, for in _Newcomb_, the riches were reserved for the irrational: "if someone is very good at predicting behavior and rewards predicted irrationality richly, then irrationality will be richly rewarded" (Gibbard and Harper 1978). 

This line of reasoning appearts particularly compelling in Arntzenius' _Insane Newcomb_:
> Consider again a Newcomb situation. Now
suppose that the situation is that one makes a choice after one has seen the contents of
the boxes, but that the predictor still rewards people who, insanely, choose only box
A even after they have seen the contents of the boxes. What will happen? Evidential
decision theorists and causal decision theorists will always see nothing in box A and
will always pick both boxes. Insane people will see $10 in box A and $1 in box B and
pick box A only. So insane people will end up richer than causal decision theorists
and evidential decision theorists, and all hands can foresee that insanity will be
rewarded. This hardly seems an argument that insane people are more rational than
either of them are.

But, others will reply: "The reason I am interested in decision theory is so that I can get rich, not so that I can satisfy some platonic notion of rationality."

What is happening? The disputants are using the word "rational" in different ways. When language goes on holiday to the strange land of Newcomb, the word "rational" loses its everyday usefulness. This shows the limits of conceptual analysis.

Instead, we should use different words depending on what we are interested in. For instance one could say that _act-decision theory_ is the theory that tells you how to get rich if you find yourself in a particular situation and are not bound by any decision rule. _Rule-decision theory_ would be the theory that tells you which rules are best for getting rich. Inspired by [Ord (2009)](http://www.amirrorclear.net/academic/papers/beyond-action.html), we could even define _global decision theory_ as the theory which, for any X, tells you which X will make you the most money.

Which X to choose will depend on the context. If you are choosing a decision rule, for example by programming an AI, you should use rule-decision theory. (If you want to think of "choosing a rule for the AI" as an act, act-decision theory will tell you to choose the rule that will be best. That's a mere verbal issue.)

Kenny Easwaran has [similar thoughts](http://rationallyspeakingpodcast.org/show/rs140-kenny-easwaran-on-newcombs-paradox-and-the-tragedy-of.html):
> Perhaps there just is a notion of rational action, and a notion of rational character, and they disagree with each other. That the rational character is being the sort of person that would one-box, but the rational action is two-boxing, and it's just a shame that the rational, virtuous character doesn't give rise to the rational action. I think that this is a thought that we might be led to by thinking about rationality in terms of what are the effects of these various types of intervention that we can have.
> [...]
> I think one way to think about this is [...] trying to understand causation through what they call these causal graphs. They say if you consider all the possible things that might have effects on each other, then we can draw an arrow from anything to the things that it directly affects. Then they say, well, we can fill in these arrows by doing enough controlled experiments on the world, we can fill in the probabilities behind all these arrows. And we can understand how one of these variables, as we might call it, contributes causally to another, by changing the probabilities of these outcomes.
> 
> The only way, they say, that we can understand these probabilities, is when we can do controlled experiments. When we can sort of break the causal structure and intervene on some things. This is what scientists are trying to do when they do controlled experiments. They say, "If you want to know if smoking causes cancer, well, the first thing you can do is look at smokers and look at whether they have cancer and look at non-smokers and look at whether they have cancer." But then you're still susceptible to the issues that Fisher was worrying about. What you should actually do if you wanted to figure out whether smoking causes cancer, is not observe smokers and observe non-smokers, but take a bunch of people, break whatever causes would have made them smoke or made them not smoke, and you either force some people to smoke or force some people not to smoke.
> 
> Obviously this experiment would never get ethical approval, but if you can do that -- if you can break the causal arrows coming in, and just intervene on this variable and force some people to be smokers and force others to not be smokers, and then look at the probabilities -- then we can understand what are the downstream effects of smoking.
> 
> In some sense, these causal graphs only make sense to the extent that we can break certain arrows, intervene on certain variables and observe downstream effects. Then, I think, in all these Newcomb type problems, it looks like there's several different levels at which one might imagine intervening. You can intervene on your act. You can say, imagine a person who's just like you, who had the same character as you, going into the Newcomb puzzle. Now imagine that we're able to, from the outside, break the effect of that psychology and just force this person to take the one box or take the two boxes. In this case, forcing them to take the two boxes, regardless of what sort of person they were like, will make them better off. So that's a sense in which two-boxing is the rational action.
> 
> Whereas if we're intervening at the level of choosing what the character of this person is before they even go into the tent, then at that level the thing that leaves them better off is breaking any effects of their history, and making them the sort of person who's a one-boxer at this point. If we can imagine having this sort of radical intervention, then we can see, at different levels, different things are rational.

To what extent we human beings can intervene at the level our acts, or at the level of our rules, is, I suspect, an empirically and philosophically deep issue.

# A problem for any decision theory?
I think using these distinctions can solve much of the confusion about WAYRs in _Newcomb_ and analogous cases. But _Insane Newcomb_ hints at a more fundamental problem. Both EDT _and_ CDT can be made vulerable to an WAYR, for example in _Insane Newcomb_.

Moreover, any decision theory can be made vulnerable to WAYRs.

Suppose God zaps you with an electric shock every time you use decision theory X on a Tuesday. The shock is so painful that avoiding the shock outweighs every other consideration. So you should not use X, because bad things will happen on Tuesday. Instead, you might use the decision theory X*, which says "Use X from Wednesday to Monday. On Tuesday, use some other decision theory". 

But suppose that god now says he will zap you every time you use X* on a Tuesday. In this case, it would be better to use CDT or EDT instead of X*. 

Since X can be any decision theory, there exists no decision theory which will make you rich in all cases. So we need to be pragmatic and choose the decision theory that works best given the cases we expect to face. But this just means using the meta-decision theory that tells you to do that. 