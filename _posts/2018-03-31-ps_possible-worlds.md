---
layout: post
title: "Philosophy success story III: possible words semantics"
date: 2018-03-31 12:00:00
---

_This is part of my series on success stories in philosophy. See [this page](/ps) for an explanation of the project and links to other items in the series._

# Contents
{: .no_toc}
1. toc
{:toc}

# Intensions rescued from darkness
Grant that “animals with a kidney” and “animals with a heart” designate the same set. They have the same extension. Yet their meaning is clearly different.[^2d] In _On Sense and Reference_, ("Über Sinn und Bedeutung", 1892) Frege had already noticed this.

[^2d]: Ordinary-language predicates can be ambiguous between sense and reference. Ordinary-language names can also be ambiguous in the same way, as with "Hesperus = Phosoporus". But Kripke himself (!) didn't appear to see this, and it took the development of two-dimensional semantics ([Stanford](https://plato.stanford.edu/entries/two-dimensional-semantics/), see also Sider's _Logic for Philosophy_, chapter 10, and [Chalmers](https://philpapers.org/rec/CHATS)). I don't count this as a success story because 2D semantics has yet to gain consensus approval. 

Classical predicate logic's achievement was to give a precise and universal account of how the designation of a sentence depends on the designation of its parts. It was a powerful tool for both deduction and clarification, revealing the ambiguity of ordinary language. I discuss this in detail in the [first success story](/ps_predicate).

Classical logic was developed to model the reasoning needed in mathematics, where the difference between meaning and designation is unimportant. Outside of mathematics, where meaning and designation can come apart, classical logic was inadequate. A formal account of _meaning_ was lacking. Frege called it sense ("Sinn"). According to [Sam Cumming](https://plato.stanford.edu/entries/names/), "Frege left his notion of sense somewhat obscure". Frege appeared to endorse the _criterion of difference for senses_: 

> Two sentences S and S* differ in sense if and only if some rational agent who understood both could, on reflection, judge that S is true without judging that S* is true.

This is not adequately formal. Letting meaning depend on the conclusions of some "rational agent" leaves it at the level of intuition. The criterion does not even attempt to give a formal model of meaning; it simply gives a condition for meanings to differ.

Meaning began to seem metaphysically suspect, like a ghostly "extra" property tacked on to every predicate. [SEP](https://plato.stanford.edu/entries/possible-worlds/) tells us:
> Intensional entities have of course featured prominently in the history of philosophy since Plato and, in particular, have played natural explanatory roles in the analysis of intentional attitudes like belief and mental content. For all their prominence and importance, however, the nature of these entities has often been obscure and controversial and, indeed, as a consequence, they were easily dismissed as ill-understood and metaphysically suspect “creatures of darkness”[^quine] (Quine 1956, 180) by the naturalistically oriented philosophers of the early- to mid-20th century. 

[^quine]: In _Quantifiers and Propositional Attitudes_ (1956) Quine wrote: "Intensions are creatures of darkness, and I shall rejoice with the reader when they are exorcised, but first I want to make certain points with help of them." My understanding is that Quine had a pre-possible worlds understanding of "intensions", equivalent to Frege's senses and hence still informal. So in today's usage the quote would be rendered as "Meanings are creatures of darkness". Quine was writing in 1956. Kripke published _Semantical Considerations on Modal Logic_ in 1963.

The contribution of possible worlds semantics was to give a precise formal description of these "creatures of darkness", bringing them into the realm of respectability.

Simply: intensions are extensions across possible worlds. 

Sider (_Logic for Philosophy_ p.290) writes: 

> we relativize the interpretation of predicates to possible worlds. The interpretation of a two-place predicate, for example, was in nonmodal predicate logic a set of ordered pairs of members of the domain; now it is a set of ordered triples, two members of which are in the domain, and one member of which is a possible world. When $$\langle u_1 ,u_2 ,w \rangle$$ is in the interpretation of a two-place predicate $$R$$, that represents $$R$$’s applying to $$u_1$$ and $$u_2$$ in possible world $$w$$. This relativization makes intuitive sense: a predicate can apply to some objects in one possible world but fail to apply to those same objects in some other possible world. These predicate-interpretations are known as “intensions”. The name emphasizes the analogy with extensions, which are the interpretations of predicates in nonmodal predicate logic. The analogy is this: the intension of a predicate predicate can be thought of as determining an extension within each possible world".


# Applications
## Future contingents
Aristotle famously used the case of a sea-battle to (seemingly) argue against the law of the excluded middle:

> Let me illustrate. A sea-fight must either take place to-morrow or not, but it is not necessary that it should take place to-morrow, neither is it necessary that it should not take place, yet it is necessary that it either should or should not take place to-morrow. Since propositions correspond with facts, it is evident that when in future events there is a real alternative, and a potentiality in contrary directions, the corresponding affirmation and denial have the same character.
> 
> This is the case with regard to that which is not always existent or not always nonexistent. One of the two propositions in such instances must be true and the other false, but we cannot say determinately that this or that is false, but must leave the alternative undecided. One may indeed be more likely to be true than the other, but it cannot be either actually true or actually false. It is therefore plain that it is not necessary that of an affirmation and a denial one should be true and the other false. For in the case of that which exists potentially, but not actually, the rule which applies to that which exists actually does not hold good. The case is rather as we have indicated.

People appear to have been confused about this for many centuries. It doesn't help that Aristotle wrote very ambiguously. Colin Strang (1960) tells us:

> VERY briefly, what Aristotle is saying in De Interpretatione, chapter ix is this: if of two contradictory propositions it is necessary that one should be true and the other false, then it follows that everything happens of necessity; but in fact not everything happens of necessity; therefore it is not the case that of two contradictory propositions it is necessary that one should be true and the other false; the propositions for which this does not hold are certain particular propositions about the future.
>  
> The reader is warned that what Aristotle is saying is ambiguous (cf. Miss Anscombe, loc. cit. p. 1).

SEP [tells us](https://plato.stanford.edu/entries/future-contingents/): 

> The interpretative problems regarding Aristotle's logical problem about the sea-battle tomorrow are by no means simple. Over the centuries, many philosophers and logicians have formulated their interpretations of the Aristotelian text (see Øhrstrøm and Hasle 1995, p. 10 ff.).

The SEP article is very long, and features Leibniz and some pretty funky-looking graphs. I recommend it if you want to experience some confusion.

Aristole's could be taken to reason thus:
1. If Battle, then it cannot be that No Battle
2. If if cannot be that no Battle, then necessarily Battle
3. If Battle, then Necessarily Battle

But this is an obvious modal fallacy, drawing on the ambiguity of (1) between
* The true statement $$\Box (B \lor \neg B)$$ which implies $$\Box(B \rightarrow \neg\neg B)$$ 
* The false statement $$(B \rightarrow \Box \neg\neg B) \iff (B \rightarrow \Box B)$$

Philosophy is littered with variations on this confusion between necessity of the consequence and necessity of the consequent.

## Modality de dicto vs modality de re
As the SEP page on [Medieval theories of modality](https://plato.stanford.edu/entries/modality-medieval/) will amply demonstrate, confusion reigned long after Aristotle's day. Quine (_Word and Object_) was baffled by talk of a difference between necessary and contingent attributes of an object, but used some quite fallacious arguments in attacking that difference:
> Perhaps I can evoke the appropriate sense of bewilderment as
follows. Mathematicians may conceivably be said to be necessarily
rational and not necessarily two-legged; and cyclists
necessarily two-legged and not necessarily rational. But what
of an individual who counts among his eccentricities both
mathematics and cycling? Is this concrete individual necessarily
rational and contingently two-legged or vice versa?
Just insofar as we are talking referentially of the object, with
no special bias towards a background grouping of mathematicians
as against cyclists or vice versa, there is no semblance
of sense in rating some of his attributes as necessary and others
as contingent. Some of his attributes count as important and
others as unimportant, yes, some as enduring and others as
fleeting; but none as necessary or contingent.

SEP [writes](https://plato.stanford.edu/entries/metaphysics/): 
"Most philosophers are now convinced, however, that Quine's “mathematical cyclist” argument has been adequately answered by Saul Kripke (1972), Alvin Plantinga (1974) and various other defenders of modality de re."

And [elsewhere](https://plato.stanford.edu/entries/possible-worlds/):

> (15) Algol is a dog essentially: $$\Box (\exists a  \rightarrow Da)$$
> 
> Sentences like (15) in which properties are ascribed to a specific individual in a modal context are said to exhibit modality de re (modality of the thing). Modal sentences that do not, like
> > Necessarily, all dogs are mammals: $$\Box \forall x (Dx \rightarrow Mx)$$
> are said to exhibit modality de dicto (roughly, modality of the proposition). 

As Plantiga writes Quine has us confused:
> The essentialist, Quine thinks, will presumably accept
> (35) Mathematicians are necessarily rational but not necessarily
> bipedal
> and
> (36) Cyclists are necessarily bipedal but not necessarily rational.
> 
> But now suppose that
> (37) Paul J. Swiers is both a cyclist and a mathematician.
> From these we may infer both
> (38) Swiers is necessarily rational but not necessarily bipedal
> and
> (39) Swiers is necessarily bipedal but not necessarily rational
> 
> which appear to contradict each other twice over.
> This argument is unsuccessful as a refutation of the essentialist.
> For clearly enough the inference of (39) from (36) and (37) is
> sound only if (36) is read de re; but, read de re, there is not so much
> as a ghost of a reason for thinking that the essentialist will accept it.

But possible worlds semantics also illuminates the intuition that was likely behind Quine's dismissal of _de re_ modality. SEP:

> Possible world semantics provides an illuminating analysis of the key difference between [modality _de re_ and modality _de dicto_]: The truth conditions for both modalities involve a commitment to possible worlds; however, the truth conditions for sentences exhibiting modality _de re_ involve in addition a commitment to the meaningfulness of transworld identity, the thesis that, necessarily, every individual (typically, at any rate) exists and exemplifies (often very different) properties in many different possible worlds.

Beautiful.

<hr> <!-- hr to be added before footnotes--> 