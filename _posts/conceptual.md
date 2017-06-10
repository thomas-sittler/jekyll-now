---
title: 'Successful conceptual analyses: language returned from holiday'
---

We start with some intuitions about whether particular objects are instances of a concept. Conceptual analysis is the attempt to find necessary and sufficient conditions that pick out all and only the objects which are intuitive instances of the concept. Via [Luke Muehlhauser](http://commonsenseatheism.com/?p=16103), De Paul and Ramsey (1999) write:

> Anyone familiar with Plato’s dialogues knows how [conceptual analysis] is conducted. We see Socrates encounter someone who claims to have figured out the true essence of some abstract notion… the person puts forward a definition or analysis of the notion in the form of necessary and sufficient conditions that are thought to capture all and only instances of the concept in question. Socrates then refutes his interlocutor’s definition of the concept by pointing out various counterexamples… For example, in Book I of the _Republic_, when Cephalus defines justice in a way that requires the returning of property and total honesty, Socrates responds by pointing out that it would be unjust to return weapons to a person who had gone mad or to tell the whole truth to such a person…. [The] proposed analysis is rejected because it fails to capture our intuitive judgments about the nature of justice. After a proposed analysis or definition is overturned by an intuitive counterexample, the idea is to revise or replace the analysis with one that is not subject to the counterexample. Counterexamples to the new analysis are sought, the analysis revised if any counterexamples are found, and so on…

At first glance, formalising our intuitions in this way seems useful. But conceptual analysis has rightly been the subject of much derision, the canonical example being the lack of progress in the [conceptual analysis of knowledge](https://plato.stanford.edu/entries/knowledge-analysis/). As Muehlhauser writes,

> A cottage industry sprung up around these “Gettier problems,” with philosophers proposing new sets of necessary and sufficient conditions for knowledge, and other philosophers raising counter-examples to them. Weatherson (2003) described this circus as “the analysis of knowledge merry-go-round.”

So is conceptual analysis bunk? Must we give up on the exciting project of formalising our intuitions? Must we be content with using stipulated definitions to clarify our utterances?

To express my view on this, I need to make some distinctions. 

Let's call the _domain_ of a conceptual analysis the set of allowed examples and counter-examples. 

A conceptual analysis is _successful_ on a domain if it furnishes conditions that are co-extensional with our intuitions about every element in the domain. 

# Unrestricted-domain conceptual analysis cannot be successful
Suppose we start with an unrestricted domain. Then it seems that no conceptual analysis can be succesful. I can always come up with a counter-example to any analysis you propose. [Waismann (1951)](http://www.ditext.com/waismann/verifiability.html) writes:

> Suppose I have to verify a statement such as 'There is a cat next door'; suppose I go over to the next room, open the door, look into it and actually see a cat. Is this enough to prove my statement? Or must I, in addition to it, touch the cat, pat him and induce him to purr? And supposing that I had done all these things, can I then be absolutely certain that my statement was true? Instantly we come up against the well-known battery of sceptical arguments mustered since ancient times. What, for instance, should I say when that creature later on grew to a gigantic size? Or if it showed some queer behaviour usually not to be found with cats, say, if, under certain conditions, it could be revived from death whereas normal cats could not? Shall I, in such a case, say that a new species has come into being? Or that it was a cat with extraordinary properties? Again, suppose I say 'There is my friend over there'. What if on drawing closer in order to shake hands with him he suddenly disappeared? 'Therefore it was not my friend but some delusion or other.' But suppose a few seconds later I saw him again, could grasp his hand, etc. What then? 'Therefore my friend was nevertheless there and his disappearance was some delusion or other.' But imagine after a while he disappeared again, or seemed to disappear -- what shall I say now? Have we rules ready for all imaginable possibilities?

Suppose your conceptual analysis of "cat" is "a thing with fur, and purrs when patted". As long as the domain is that of everyday quadrupeds, your conceptual analysis will do quite well. But with an unrestricted domain, I can raise the counter-example of an animal that has fur, purrs when patted, but later grows to a gigantic size. The same goes for apparently rock-solid concepts like elements of the periodic table:

> 'But are there not exact definitions at least in science?' Let's see. The notion of gold seems to be defined with absolute precision, say by the spectrum of gold with its characteristic lines. Now what would you say if a substance was discovered that looked like gold, satisfied all the chemical tests for gold, whilst it emitted a new sort of radiation? 'But such things do not happen.' Quite so; but they might happen, and that is enough to show that we can never exclude altogether the possibility of some unforeseen situation arising in which we shall have to modify our definition.

So far we have only dealt with non-mathematical concepts, like "justice", "gold", or "cat". But, surely, analyses of our mathematical concepts do not admit of counter-examples, however large the domain. 

Suppose we conceptually analyse "the shortest distance between two points" as "the straight line that passes through both points". <!-- Then counterexample = non-euclidean geometry-->.

The picture so far: some non-mathematical concepts resist conceptual analysis even when the domain is kept small. There have already been many cats who were revived after their heart stopped beating (see "[How to perform CPR on a cat](http://www.adventurecats.org/gear-safety/how-to-perform-cpr-on-a-cat/)"). Analysis of other non-mathematical concepts, typically ones used in science like gold, can be defeated by appealing to unprecedented but perfectly conceivable occurences. And even mathematical conceptual analyses only succeed on the domain of examples that humans can conceive of.

Thus it's useful to think of the space of logically possible examples as a series of nested domains (as shown below). On the smallest domain, even everyday empirical concepts can be successfully analysed, the larger the domain, the fewer the concepts that are analysable on this domain. Mathematical concepts allow for the analyses that are closest to unrestricted. But no concepts are successfully analysable on the unrestricted domain of logically possible examples.

* _all examples_
  * P ^ ¬P
  * Jack is taller than Jane and Jane is taller than Jack 
  * _logically possible examples_
    * a straight line that is not the shortest distance between two points
    * a triangle whose angles do not sum to 180
    * _conceivable examples_
      * talking dog
      * cat growing to a gignatic size
      * _examples allowed by our current understanding of physics_
        * black swan
        * three-legged dog
        * ten-time lottery winner
        * _examples we are likely to encounter in everyday life_
          * white swan
          * purring cat
          * lottery winner

# Brains don't store concepts as necessary and sufficient conditions
Why is it the case that a conceptual analysis over an unrestricted domain of (empirical) examples cannot be successful? It's because of how concepts, or rather our intuitions about concept-membership, are stored in the human brain. If our intuitions about concepts were stored in terms of necessary and sufficient conditions, we would find nothing puzzling about the cat that grows to a gigantic size. If "cat" was stored as" a thing with fur, and purrs when patted", we would say that, of course, the gigantic cat is a cat, because it satisfies the conditions. I'll just quote Luke here:

> > Think of a fish, any fish. Did you think of something like a trout or a shark, or did you think of an eel or a flounder? Most people would admit to thinking of something like the first: a torpedo-shaped object with small fins, bilaterally symmetrical, which swims in the water by moving its tail from side to side. Eels are much longer, and they slither; flounders are also differently shaped, aren’t symmetrical, and move by waving their body in the vertical dimension. Although all of these things are technically fish, they do not all seem to be equally good examples of fish. The _typical_ category members are the good examples — what you normally think of when you think of the category. The _atypical_ objects are ones that are known to be members but that are unusual in some way… The classical view does not have any way of distinguishing typical and atypical category members. Since all the items in the category have met the definition’s criteria, all are category members. …The simplest way to demonstrate this phenomenon is simply to ask people to rate items on how typical they think each item is of a category. So, you could give people a list of fish and ask them to rate how typical each one is of the category fish. Rosch (1975) did this task for 10 categories and looked to see how much subjects agreed with one another. She discovered that the reliability of typicality ratings was an extremely high .97 (where 1.0 would be perfect agreement)… In short, people agree that a trout is a typical fish and an eel is an atypical one. (Mills 2002, p. 22)
>
> So people agree that some items are more typical category members than others, but do these typicality effects manifest in normal cognition and behavior? Yes, they do.
>
> > Rips, Shoben, and Smith (1973) found that the ease with which people judged category membership depended on typicality. For example, people find it very easy to affirm that a robin is a bird but are much slower to affirm that a chicken (a less typical item) is a bird. This finding has also been found with visual stimuli: Identifying a picture of a chicken as a bird takes longer than identifying a pictured robin (Murphy and Brownell 1985; Smith, Balzano, and Walker 1978). The influence of typicality is not just in identifying items as category members — it also occurs with the production of items from a category. Battig and Montague (1969) performed a very large norming study in which subjects were given category names, like furniture or precious stone and had to produce examples of these categories. These data are still used today in choosing stimuli for experiments (though they are limited, as a number of common categories were not included). Mervis, Catlin and Rosch (1976) showed that the items that were most often produced in response to the category names were the ones rated as typical (by other subjects). In fact, the average correlation of typicality and production frequency across categories was .63, which is quite high given all the other variables that affect production. When people learn artificial categories, they tend to learn the typical items before the atypical ones (Rosch, Simpson, and Miller 1976). Furthermore, learning is faster if subjects are taught on mostly typical items than if they are taught on atypical items (Mervis and Pani 1980; Posner and Keele 1968). Thus, typicality is not just a feeling that people have about some items (“trout good; eels bad”) — it is important to the initial learning of the category in a number of respects… Learning is not the end of the influence, however. Typical items are more useful for inferences about category members. For example, imagine that you heard that eagles had caught some disease. How likely do you think it would be to spread to other birds? Now suppose that it turned out to be larks or robins who caught the disease. Rips (1975) found that people were more likely to infer that other birds would catch the disease when a typical bird, like robins, had it than when an atypical one, like eagles, had it… (Murphy 2002, p. 23)

So, in our brains, category membership is a matter of degree, and with some typical members, some atypical members, and some fringe items for which our membership-intuition fluctuates. But, crucially, this is **not** the fudamental reason conceptual analysis cannot be unrestrictedly successful. To deal with degrees of category membership, we simply need a more sophisticated notion of conceptual analysis, one that admits of degree. 

Rather than looking for necessary and sufficient conditions, this would involve a formalisation of our typicality judgements. In other words, we are looking for an algorithm that takes as input various characteristics of an object (it is a torpedo-shaped to degree _n, _its fins are of size _m_, it is symmetrical to degree _k_)and outputs a level of typicality of this object for various categories (it is a fish to typicality _j, _a flower to typicality _i_). The more closely the output matches our intuitive typicality-judgement, the better the conceptual analysis. Now, this is quite different from what philosophers have actually been doing when conducting conceptual analysis. But I am less concerned with the merit or lack thereof in the past work of analysts, than I am interested in the method of conceptual analysis itself. Additionally, one might be charitable to the philosophers and say that they have been focusing on conceptual analysis without degrees as a sort of first approximation, but that they do in principle recognise that it is a special subset of the more generally valid method of conceptual analysis admitting of degrees.

# Language gone on holiday
However, my real point is that even this more sophisticated approach cannot be successful if we are to have unrestricted domains. This is what Waismann shows. Given any formalisation of my typicality-judgements, there is always a logically possible object that counts as very typical under the formalisation but that we nonetheless find either intuitively atypical or at the very least an object that breaks our intuitions, because it is so strange. Suppose I give you the following conceptual analysis of fish: "If an object is torpedo-shaped to degree _n, _its fins are of size _m_, and it is symmetrical to degree _k, _then it is a fish to typicality f(n,m,k)=n+m+k." Then you can reply: "what about a perfectly torpedo-shaped object, with typical fins, and high symmetry, that reproduces asexually". I can make my analysis more sophisticated, but there will always be some conceivable counter-example. We might arrive at some very strange beasts, like a dog that is typical in every thinkable way except that on January 1, 2018 it suddenly gains the ability to talk. You might then rightly tell me to bugger off, because you just don't have a typicality judgement about this object, and what could possibly come from querying you about it? I would have to agree. But it would still be true that the attempted formalisation would be a failure, because it would output "highly typical" while you outputted "get lost!".

The key point here is that the binary nature of necessary and sufficient conditions is only one of the problems of conceptual analysis. The more fundamental problem is that we only store concepts for use on a limited domain. Outside of philosophical thought experiments, there are no radiating gold lumps or gigantic cats. So it wouldn't be useful to store the information to deal with these cases. When we discuss counter-examples from an unusual domain, our concepts break down. Language, and along with it, our intuitions, go on holiday outside of their domain.

# Language returned from its holiday
So conceptual analysis is bunk in so far as it is conducted on an unrestricted or inappropriately large domain. That is chasing shadows. Much philosophical work has been in this category.

But a humble conceptual analysis, one that only aims for a domain as large as can reasonably be hoped for, is a very useful tool. It is equivalent to coming up with good defintions. A definition is stipulative, so in what sense can it be good? In the sense that it captures many of our intuitions while remaining concise and clear.

## type ("species") of animal = can mate to produce fertile offspring
pretty good, but there are many problem cases where folk taxonomy differs from scientific taxonomy.

<!-- 
https://en.wikipedia.org/wiki/Folk_biology
https://mitpress.mit.edu/books/folkbiology
-->

## temperature = mean molecular kinetic energy
works pretty well: hot iron, cold ice, etc...
does not always work: chili peppers on your skin are "hot"
## magnets
> “In one sense people knew what magnets were — they were things that attracted iron — long before science told them what magnets were. A child learns what the word ‘magnet’ means not, typically, by learning an explicit definition, but by learning the ‘folk physics’ of magnets, in which the ordinary term ‘magnet’ is embedded or implicitly defined as a theoretical term.”

Daniel Dennett, The Intentional Stance, Chap. 3, “Three Kinds of Intentional Psychology”

<!--
https://geopolicraticus.wordpress.com/2015/08/02/folk-concepts-and-scientific-progress/
-->

## the limit-definition of a derivative
## the definition of a limit
## speed and accelaration
## effective calculability
## countability