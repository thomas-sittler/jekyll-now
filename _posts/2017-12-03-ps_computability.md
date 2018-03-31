---
layout: post
title: "Philosophy success story II: the analysis of computability"
date: 2017-12-03 13:30:00
---

> a computing machine is really a logic machine. Its circuits embody
the distilled insights of a remarkable collection of logicians, developed
over centuries.
<p style="text-align:right;">— Martin Davis (2000)</p>

*This is part of my series on success stories in philosophy. See [this page](/ps) for an explanation of the project and links to other items in the series. I also have a related discussion of conceptual analysis [here](/conceptual)*

# Contents
{: .no_toc}
1. toc
{:toc} 

The analysis of computability is one of the few examples in history of a non-trivial [conceptual analysis](https://philpapers.org/browse/conceptual-analysis) that has consensus support. Some might want to quibble that computer science or mathematics rather than philosophy deserves the credit for it. I'm not interested in which artificial faction of academy should lay claim to the spoils of war. The search for, proposal of, and eventual vindication of a formalisation of an everyday concept is philosophical in method, that is my point. If you wish to conclude from this that computer scientists produce better philosophy than philosophers, so be it.

To us living today, the formal idea of an algorithm is so commonsensical that it can he hard to imagine a worldview lacking this precise concept. Yet less a than a century ago, that was exactly the world people like Turing, Gödel, Russel, Hilbert, and everybody else was living in. 

The notion of algorithm, of course, is so general that people have been using them for thousands of years. The use of tally marks to count sheep is a form of algorithm. The [sieve of Eratosthenes](https://en.wikipedia.org/wiki/Sieve_of_Eratosthenes), an algorithm for finding all prime number up to a given limit, was developed in ancient Greece. The success story is therefore not the developement of algorithms, but the understand and formalisation of the concept itself. This improved understanding helped dissolve some confusions. 

# The intuitive notion of effective calculability

Soare 1996:

> In 1642 the French mathematician and scientist, Blaise Pascal, invented an adding machine which may be the first digital calculator.

Wikipedia:

> In 1673, Gottfried Leibniz demonstrated a digital mechanical calculator, called the Stepped Reckoner. [...] It could:
>
> - add or subtract an 8-digit number to / from a 16-digit number
> - multiply two 8-digit numbers to get a 16-digit result
> - divide a 16-digit number by an 8-digit divisor

These primitive calculating devices show that people in the 17th century had to have some inuitive notion of "that which can be calculated by a machine" or by a "mindless process" or "without leaps of insight". They were, at the very least, an existence proof, showing that addition and subtraction could be performed by such a process.

Wikipedia also tells us:

> Before the precise definition of computable function, mathematicians often used the informal term effectively calculable to describe functions that are computable by paper-and-pencil methods. 

And:

> In 1935 Turing and everyone else
>  used the term "computer" for an idealized human calculating with extra
>  material such as pencil and paper, or a desk calculator, a meaning very
>  different from the use of the word today.

# The Church-Turing analysis of computability

Stanford has a nice and concise [explanation](https://plato.stanford.edu/entries/computability/):

> In the 1930s, well before there were computers, various mathematicians from around the world invented precise, independent definitions of what it means to be computable. Alonzo Church defined the Lambda calculus, Kurt Gödel defined Recursive functions, Stephen Kleene defined Formal systems, Markov defined what became known as Markov algorithms, Emil Post and Alan Turing defined abstract machines now known as Post machines and Turing machines.
>
> Surprisingly, all of these models are exactly equivalent: anything computable in the lambda calculus is computable by a Turing machine and similarly for any other pairs of the above computational systems. After this was proved, Church expressed the belief that the intuitive notion of “computable in principle” is identical to the above precise notions. This belief, now called the “Church-Turing Thesis”, is uniformly accepted by mathematicians.

# Computability theory applied
I take Turing's (and his contemporaries') philosophical contribution to be the conceptual analysis of "computable" as "computable by a Turing machine", i.e. the assertion of the Church-Turing Thesis. As we will often see in this series, once we have a formalism, we can go _to town_ and start proving things left and right about the formal object. What was once a topic of speculation becomes amenable to mathematics. (For much mroe on this topics, see my [other post](/ps_looks-like) on why good philosophy often looks like mathematics.) Here are some examples.

## The halting problem
Given Pascal's and Leibnitz's machines, one might have thought it natural that any function (set $$F​$$ of ordered pairs such that if  $$\langle a,b \rangle \in F​$$ and $$\langle a,c \rangle \in F​$$ then $$b=c​$$ ) which can be precisely specified can be computed in the inuitive sense. But Turing showed that this is not true. For example, the halting problem is not computable; and the *Entscheidungsproblem* (Turing's original motivation for developing his formalism) cannot be solved. 

## Further applications in mathamtics
Here are some lists of examples of non-computable functions:
* [An example of an easy to understand undecidable problem
 — Mathematics StackExchange](https://math.stackexchange.com/questions/80745/an-example-of-an-easy-to-understand-undecidable-problem)
* [Non-computable but easily described arithmetical functions
 — MathOverflow](https://mathoverflow.net/questions/29197/non-computable-but-easily-described-arithmetical-functions)
* [What are the most attractive Turing undecidable problems in mathematics? — MathOverflow](https://mathoverflow.net/questions/11540/what-are-the-most-attractive-turing-undecidable-problems-in-mathematics)

There is an analogy here, by the way, to the previous success story: many people thought it natural that any continuous function must be differentiable, the [discovery](https://en.wikipedia.org/wiki/Weierstrass_function) of a function that is everywhere continuous and nowhere differentiable seemed problematic, and the formalisation of the concept of continuity solved the problem.

## The modern computer
The greatest practical impact of Turing's discoveries was to lay the conceptual ground for the development of modern computers. (Wikipedia has a [good summary](https://en.wikipedia.org/wiki/History_of_computing_hardware) of the history of computing.) 

In his 1936 paper _On Computable Numbers, with an Application to the Entscheidungsproblem_, once armed with his new formalism, Turing immediately proves an interesting result: the general notion of "computable by _some_ turing machine" can itself be expressed in terms of Turing machines. In particular, a [Universal Turing Machine](https://en.wikipedia.org/wiki/Universal_Turing_machine), is a Turing Machine that can simulate an arbitrary Turing machine on arbitrary input.[^utm]

[^utm]: The universal machine achieves this by reading both the description of the machine to be simulated as well as the input thereof from its own tape. Extremly basic sketch: if $$M'$$ simulates $$M$$, $$M'$$ will print out, in sequence, the complete configurations that $$M$$ would produce. It will have a record of the last complete configuration at the right of the tape, and a record of $$M$$'s rules at the left of the tape. It will shuttle back and forth, checking the latest configuration from the right, the finding the rule that it matches at the left, the moving back to build the next configuration accordingly on the right. (Peter Millican, Turing Lectures, HT16, University of Oxford)

This was the first proof that there could be a "universal" programmable machine, capable of computing anything that we know how to compute, when given the recipe. Sometimes in history, as in the case of heavier-than-air flying machines, infamously pronounced impossible by Lord Kelvin, the proof is in the pudding. With the computer, the proof preceded the pudding by several decades.

Jack Copeland (_The Essential Turing_, 2004, p.21f) writes: 
> In the years immediately following the Second World War, the Hungarian-American logician and mathematician John von Neumann—one of the most important and influential figures of twentieth-century mathematics—made the concept of the stored-programme digital computer widely known, through his writings and his charismatic public addresses [...] 
> It was during Turing’s time at Princeton that von Neumann became familiar with the ideas in ‘On Computable Numbers’. He was to become intrigued with Turing’s concept of a universal computing machine. [...]
> The Los Alamos physicist Stanley Frankel [...] has recorded von Neumann’s view of the importance of ‘On Computable Numbers’:
> > I know that in or about 1943 or ’44 von Neumann was well aware of the fundamental importance of Turing’s paper of 1936 ‘On computable numbers . . .’, which describes in principle the ‘Universal Computer’ of which every modern computer [...] is a realization. [...] Many people have acclaimed von Neumann as the ‘father of the computer’ (in a modern sense of the term) but I am sure that he would never have made that mistake himself. He might well be called the midwife, perhaps, but he firmly emphasized to me, and to others I am sure, that the fundamental conception is owing to Turing—insofar as not anticipated by Babbage, Lovelace, and others. In my view von Neumann’s essential role was in making the world aware of these fundamental concepts introduced by Turing [...].

# Epilogue: the long reach of the algorithm
The following is an example of progress in philosophy which, while quite clear-cut in my view, hasn't  achieved consensus in the discipline, so I wouldn't count it as a success story quite yet. It also has more to do with the development of advanced computers and subsequent philosophical work than with the conceptual analysis of computability. But Turing, as the father of the algorithm, does deserve a nod of acknowledgement for it, so I included it here.

Peter Millican an excellent, concise summary of the point (Turing Lectures, HT16, University of Oxford):
> Information processing, and informationally sensitive processes, can be understood in terms of symbolic inputs and outputs, governed by explicit and automatic processes. So information processing need not presuppose an "understanding" mind, and it therefore becomes possible in principle to have processes that involved sophisticated information processing without concious purpose, in much the same way as Darwin brought us sophisticated adaptation without intentional design. 

On the idea of natural selection as an algorithm, see [Dennett](https://en.wikipedia.org/wiki/Darwin%27s_Dangerous_Idea). 

<hr> <!-- <hr> to be added before footnotes-->