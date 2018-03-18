---
layout: post
title: "Games and solution concepts"
---

The basic notion of strategic game can be extended in two directions: adding imperfect information, and adding sequential moves. This gives nice matryoshka dolls of types of games, depicted below with page numbers in Osborne and Rubinstein (OR) in brackets.

[![games](../images/games.png)](../images/games.png)

Each type of game has a solution concept that is arguably natural to it. 


| **Game**                                                         | **Natural solution concept**                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Extensive game                      | Sequential equilibrium [225.1]|
| Bayesian extensive game with observable actions              | Perfect Bayesian equilibrium [231.1]                         |
| Extensive game with perfect information (and simultaneous moves) | Subgame perfect equilibrium [97.2]                           |
| Bayesian Game                                                | Bayesian-Nash equilibrium [26.1]                             |
| Strategic game                                               | Mixed-strategy Nash equilibrium [32.3] or Nash equilibrium [14.1] |

[Is everything correct up to here?]

Applying the solution concept of a more general game to a more specific game can always be done, but it is uninteresting. For example, all Nash equilibria of a strategic game are trivially subgame perfect, and trivially Bayesian. 

We can always [sometimes?] apply the solution concept of a more specific game to a more general game. For example:
* We can find the Nash equilibria of a game with sequential moves; some of these will not be subgame perfect.
* We can find the Bayesian Nash equilibria of a Bayesian extensive game with observable actions; some of these will not be subgame perfect.
* We can find the perfect Bayesian equilibria of an extensive game; in some of these the off-equilibrium-path beliefs will not be consistent [Lecture 8]
* [This is the part I'm not sure about. Seems non-standard but makes sense to me] We can find the Nash equilibria [in the sense of 14.1] of a Bayesian game. (Terminological note: OR call 26.1 simply the "Nash equilibrium" of a Bayesian Game. I want to call it the Bayesian-Nash equilibrium of a Bayesian game.) Picture the players before they receive their signals. They have some prior over the signals they and their opponents will receive. They can average over this uncertainty and decide on a strategy. If these unconditional strategies are best responses to each other, we have a Nash equilibrium. Some of these equilibria will be such that once the signal is received, some player-types are not best-responding. [The players cannot “commit” to playing non-optimally after receiving the signal. The situation is somewhat analogous to non-subgame-perfect equilibrium].


This would give us this diagram: 

[![all-solution-concepts](../images/all-solution-concepts.png)](/images/all-solution-concepts.png)

If I'm wrong about the last point, i.e. if there is no meaningful way of applying a perfect-information solution concept to a game of imperfect information, then, to compare solution concepts, we need to separate games of imperfect information and games of perfect information, as below. 

[![separate-solution-concepts](../images/separate-solution-concepts.png)](../images/separate-solution-concepts.png)

I also depict Harsanyi's purification result:

[![separate-solution-concepts-purification](../images/separate-solution-concepts-purification.png)](../images/separate-solution-concepts-purification.png)

Sources:
* By proposition 45.3, the set of correlated equilibria of G contains the set of mixed strategy Nash equilibria of G.
* By definition 32.3 of a mixed strategy Nash equilibrium, the set of mixed strategy Nash equilibria of G contains the set of Nash equilibria of G.
* Lemma 56.2 states that every strategy used with positive probability by some player in a correlated equilibrium of a finite strategic game is rationalizable.


<hr> <!-- hr to be added before footnotes-->