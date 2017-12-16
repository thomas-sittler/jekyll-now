---
layout: post
title: "Philosophy success story II: the analysis of computability"
---

<p style="text-align:right;"> a computing machine is really a logic machine. Its circuits embody
the distilled insights of a remarkable collection of logicians, developed
over centuries.<br>
-- Martin Davis (2000) </p>

*This is part of my series on success stories in philosophy. See [this page](/ps) for an explanation of the project and links to other items in the series.*

# Contents
{: .no_toc}
1. toc
{:toc} 

The analysis of computability was one of the most successful conceptual analyses in history. Some might want to quibble that computer science or mathematics rather than philosophy deserves the credit for it. I'm not interested in which artificial faction of academy should lay claim to the spoils of war. The search for, proposal of, and eventual vindication of a formalisation of an everyday concept is philosophical in method, that is my point. If you wish to conclude from this that computer scientists produce better philosophy than philosophers, so be it.

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

> In the 1930’s, well before there were computers, various mathematicians from around the world invented precise, independent definitions of what it means to be computable. Alonzo Church defined the Lambda calculus, Kurt Gödel defined Recursive functions, Stephen Kleene defined Formal systems, Markov defined what became known as Markov algorithms, Emil Post and Alan Turing defined abstract machines now known as Post machines and Turing machines.
>
> Surprisingly, all of these models are exactly equivalent: anything computable in the lambda calculus is computable by a Turing machine and similarly for any other pairs of the above computational systems. After this was proved, Church expressed the belief that the intuitive notion of “computable in principle” is identical to the above precise notions. This belief, now called the “Church-Turing Thesis”, is uniformly accepted by mathematicians.

# Computability theory applied

## The halting problem

Given Pascal's and Leibnitz's machines, one might have thought it natural that any function (set $$F​$$ of ordered pairs such that if  $$\langle a,b \rangle \in F​$$ and $$\langle a,c \rangle \in F​$$ then $$b=c​$$ ) which can be precisely specified can be computed in the inuitive sense. But Turing showed that this is not true. For example, the halting problem is not computable; and the *Entscheidungsproblem* (Turing's original motivation for developing his formalism) cannot be solved. Here are some [nice examples](https://mathoverflow.net/questions/29197/non-computable-but-easily-described-arithmetical-functions) of non-computable functions. 

There is an analogy here, by the way, to the previous success story: many people thought it natural that any continuous function must be differentiable, the [discovery](https://en.wikipedia.org/wiki/Weierstrass_function) of a function that is everywhere continuous and nowhere differentiable seemed problematic, and the formalisation of the concept of continuity solved the problem.

## Other applications?

What are some other examples of confusions caused by the informal notion of computability, which  disappeared when the formal notion became available? I suspect there are many, but I'm too ignorant of history to find good examples.

# Epilogue: the long reach of the algorithm

The following is an example of progress in philosophy which, while quite clear-cut in my view, hasn't  achieved consensus in the discipline, so I wouln't count it as a success story quite yet. It also has more to do with the developement of advanced computers and subsequent philosophical work than with the conceptual analysis of computability. But Turing, as the father of the algorithm, does deserve a nod of acknowledgement for it, so I included it here.

Peter Millican an excellent, concise summary of the point (Turing Lectures, HT16, University of Oxford):
> Information processing, and informationally sensitive processes, can be understood in terms of symbolic inputs and outputs, governed by explicit and automatic processes. So information processing need not presuppose an "understanding" mind, and it therefore becomes possible in principle to have processes that involved sophisticated information processing without concious purpose, in much the same way as Darwin brought us sophisticated adaptation without intentional design. 

On the idea of natural selection as an algorithm, see [Dennett](https://en.wikipedia.org/wiki/Darwin%27s_Dangerous_Idea). 
