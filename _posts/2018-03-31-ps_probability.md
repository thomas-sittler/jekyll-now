---
layout: post
title: "Philosophy success story IV: the formalisation of probability"
date: 2018-03-31 12:01:00
---

> Thus, joining the rigour of demonstrations in mathematics with the uncertainty of chance, and conciliating these apparently contradictory matters, it can, taking its name from both of them, with justice arrogate the stupefying name: The Mathematics of Chance (Aleae Geometria).

<p style="text-align:right;"> — Blaise Pascal, in an address to the Académie Parisienne de Mathématiques, 1654 </p>


> Researchers in the field have wondered why the development of probability theory was so slow—especially why the apparently quite simple mathematical theory of dice throwing did not appear until the 1650s. The main part of the answer lies in appreciating just how diffi- cult it is to make concepts precise.

<p style="text-align:right;"> — James Franklin, The Science of Conjecture </p> 


> Wherefore in all great works are Clerkes so much desired? Wherefore are Auditors so richly fed? What causeth Geometricians so highly to be enhaunsed? Why are Astronomers so greatly advanced? Because that by number such things they finde, which else would farre excell mans minde.

<p style="text-align:right;"> — Robert Recorde, Arithmetic (1543) </p>

_This is part of my series on success stories in philosophy. See [this page](/ps) for an explanation of the project and links to other items in the series._

# Contents
{: .no_toc}
1. toc
{:toc}

# How people were confused
## Degrees of belief
The first way to get uncertainty spectacularly wrong is given to us by Plato, who outright rejects non-certain reasoning (_The Science of Conjecture_: Evidence and Probability Before Pascal, James Franklin):
> Plato has Socrates say to Theaetetus, “You are not offering any argument or proof, but relying on likelihood (_eikoti_). If Theodorus, or any other geometer, were prepared to rely on likelihood when doing geometry, he would be worth nothing. So you and Theodorus must consider whether, in matters as important as these, you are going to accept arguments from plausibility and likelihood (_pithanologia te kai eikosi_).”

## Probability as a binary property
One step in the right direction would be to accept that statements can fail to be definite truths, yet be in some sense be "more likely" than definite falsehoods. On this view, such statements have the property of being "probable". [SEP](https://plato.stanford.edu/entries/probability-medieval-renaissance/) writes:
> Pre-modern probability was not a number or ratio, but mainly a binary property which a proposition either had or did not have.

In this vein, Circeo wrote:
> That is probable which for the most part usually comes to pass, or which is a part of the ordinary beliefs of mankind, or which contains in itself some resemblance to these qualities, whether such resemblance be true or false. (Cicero, _De inventione_, I.29.46)

The quote not only displays the error of thinking of probability as binary. It also shows that Cicero mixed the most promising notion of probability (that which "for the most part usually comes to pass") with the completely different notions of ordinary belief and opinion, resulting in a general mess of confusion. According to SEP: "Until the thirteenth century, the definitions of “probable” by Cicero and Boethius very much shaped the medieval understanding of probability".

## Ordinal probability
Going further, one might realise that there are degrees of probability. With a solid helping of the principle of charity, Aristotle can be read as saying this:
> Therefore it is not enough for the defendant to refute the accusation by proving that the charge is not bound to be true; he must do so by showing that it is not likely to be true. For this purpose his objection must state what is more usually true than the statement attacked.

Here is another quote:
> Hence, in this proposal we have men and women, who at age 25 buy a life-long annuity for a price which they recover within eight years and although they can die within these eight years it is more probable that they live twice the time. In this way what happens more frequently and is more probable is to the advantage of the buyer. (Alexander of Alessandria, _Tractatus de usuris_, c. 72, Y f. 146r)

Aristotle did not realise that probabilities could be applied to chancy events, and nor did his medieval followers. According to A. Hall:
> According to van Brake (1976) and Schneider (1980), Aristotle classified events into three types: (1) certain events that happen necessarily; (2) probable events that happen in most cases; and (3) unpredictable or unknowable events that happen by pure chance. Furthermore, he considered the outcomes of games of chance to belong to the third category and therefore not accessible to scientific investigation, and he did not apply the term probability to games of chance.

The cardinal notion of probability did not emerge before the seventeenth century.

## Stakes-sensitivity
One can find throughout history people grasping at the intuition that when the stakes are high, unlikely things can be important. In many cases, legal scholars were interested in what to do if no definite proof of innocence or guilt can be given. Unfortunately, they invariably get the details wrong. James Franklin writes:
> In the Talmud itself, the demand for a high standard of evidence in criminal cases developed into a prohibition of any uncertainty in evidence: 
> > Witnesses in capital charges were brought in and warned: perhaps what you say is based only on conjecture, or hearsay, or is evidence from the mouth of another witness, or even from the mouth of an untrustworthy person: perhaps you are unaware that ultimately we shall scrutinize your evidence by cross-examination and inquiry? Know then that capital cases are not like monetary cases. In civil suits, one can make restitution in money, and thereby make his atonement; but in capital cases one is held responsible for his blood and the blood of his descendants till the end of the world . . . whoever destroys a single soul of Israel, scripture imputes to him as though he had destroyed a whole world . . . Our Rabbis taught: What is meant by “based only on conjecture”?—He [the judge] says to them: Perhaps you saw him running after his fellow into a ruin, you pursued him, and found him sword in hand with blood dripping from it, whilst the murdered man was writhing. If this is what you saw, you saw nothing.


Thomas Aquinas wrote:
> And yet the fact that in so many it is not possible to have certitude without fear of error is no reason why we should reject the certitude which can probably be had [quae probabiliter haberi potest] through two or three witnesses … (Thomas Aquinas, Summa theologiae, II-II, q. 70, 2, 1488)

James Franklin writes:
> Further reflection on the kinds of evidence short of certainty led to a word that expressed the most significant and original idea of the Glossators for probabilistic argument: half-proof (semiplena probatio). In the 1190s, this word was invented for the class of items of evidence that were neither null nor full proof. The word expresses the natural thought that, if two witnesses are in theory full proof, then one witness must be half.

## The problem of points
By the renaissance, thinkers had sharpened these intuitions into a concrete problem. It took centuries of fallacies to arrive at the correct answer to this problem.

The problem of points concerns a game of chance with two players who have equal chances of winning each round. The players contribute equally to a prize pot, and agree in advance that the first player to have won a certain number of rounds $$s$$ will collect the entire prize. Now suppose that the game is interrupted by external circumstances before either player has achieved victory. Player 1 has won $$s_1<s$$ rounds and player 2 has won $$s_2<s$$ rounds. How does one then divide the pot fairly? (Wikipedia, _The problem of points_)

Before Pascal formalised the now-obvious concept of _expected value_, this problem was a matter of debate. The problem of points is especially clear-cut evidence that people were confused about probability, since they arrived at different numerical answers.

Anders Hald writes (Section 4.2, p. 35ff):
> The division problem is presumably very old. It is first found in print by Pacioli (1494) for $$s$$ = 6, $$s_1 = 5$$, and $$s_2 = 2$$. Pacioli considers it as a problem in proportion and proposes to divide the stakes as $$s_1$$ to $$s_2$$. [...]
> The next attempt to solve the problem is by Cardano (1539). He shows by example that Pacioli’s proposal is ridiculous [in a game interrupted after only one round, Pacioli's method would award the entire pot to the player with the single point, even though the outcome would be far from certain] and proceeds to give a deeper analysis of the problem. We shall return to this after a discussion of some other, more primitive, proposals. 
> Tartaglia (1556) criticizes Pacioli and is sceptical of the possibility of finding a mathematical solution. He thinks that the problem is a juridical one. Nevertheless, he proposes that if $$s_1$$ is larger than $$s_2$$, A should have his own stake plus the fraction $$(s_l - s_2)/s$$ of B’s stake. Assuming that the stakes are equal, the division will be as $$s + s_1 - s_2$$ to $$s - s_1 + s_2$$. 
> Forestani (1603) formulates the following rule: First A and B should each get a portion of the total stake determined by the number of games they have won in relation to the maximum duration of the play, i.e., the proportions $$s_1/(2s- 1)$$ and $$s_2/(2s- 1)$$, as also proposed by Pacioli. But then Forestani adds that the remainder should be divided equally between them, because Fortune in the next play may reverse the results. Hence the division will be as $$2s - 1 + s_1 - s_2$$ to $$2s - 1 - s_1 + s_2$$. Comparison with Tartaglia’s rule will show that $$s$$ has been replaced by $$2s - 1$$. 
> Cardano (1539) is the first to realize that the division rule should not
depend on $$(s,s_1,s_2)$$ but only on the number of games each player lacks in
winning, $$a = s - s_1$$ and $$b = s - s_2$$, say. He introduces a new play where A, starting from scratch, is the winner if he wins $$a$$ games before B wins $$b$$ games, and he asks what the stakes should be for the play to be fair. He then takes for a fair division rule in the stopped play the ratio of the stakes in this new play and concludes that the division should be as $$b(b + 1)$$ to $$a(a + 1)$$. His reasons for this result are rather obscure. Considering an example for $$a = 1$$ and $$b = 3$$ he writes:
> > He who shall win 3 games stakes 2 crowns; how much should the other stake. I say that he should stake 12 crowns for the following reasons. If he shall win only one game it would suffice that he stakes 2 crowns; and if he shall win 2 games he should stake three times as much because by winning two games he would win 4 crowns but he has had the risk of losing the second game after having won the first and therefore he ought to have a threefold compensation. And if he shall win three games his compensation should be sixfold because the difficulty is doubled, hence he should stake 12 crowns.
> It will be seen that Cardano uses an inductive argument. Setting B’s stake equal to 1, A’s stake becomes successively equal to $$1$$, $$1 +2=3$$, and $$1 + 2 + 3 = 6$$. Cardano then concludes that in general A’s stake should be $$1 + 2 + ... + b = b(b + 1)/2$$. He does not discuss how to go from the special case $$(1, b)$$ to the general case $$(a, b)$$, but presumably he has just used the symmetry between the players.[^cardano]

[^cardano]:
    More on Cardano, in Section 4.3 of Hald: 
    > [Cardano's] _De Ludo Aleae_ is a treatise on the moral, practical, and theoretical aspects of gambling, written in colorful language and containing some anecdotes on Cardano’s own experiences. Most of the theory in the book is given in the form of examples from which general principles are or may be inferred. In some cases Cardano arrives at the solution of a problem through trial and error, and the book contains both the false and the correct solutions. He also tackles some problems that he cannot solve and then tries to give approximate solutions. [...] In Chap. 14, he defines the concept of a fair games in the following terms: 
    > > So there is one general rule, namely, that we should consider the whole circuit [the total number of equally possible cases], and the number of those casts which represents in how many ways the favorable result can occur, and compare that number to the remainder of the circuit, and according to that proportion should the mutual wagers be laid so that one may contend on equal terms.

Note how different this type of disagreement is from mathematical disagreements. When people reach different solutions about a "toy" problem case, and muddle through with heursitics, they are not facing a recalcitrant mathematical puzzle. They are confused on a much deeper level. Newcomb's problem might be a good analogy.

Anders Hald also has this interesting quote:
> In view of the achievements of the Greeks in mathematics and science, it is surprising that they did not use the symmetry of games of chance or the stability of relative frequencies to create an axiomatic theory of probability analogous to their geometry. However, the symmetry and stability which is obvious to us may not have been noticed in ancient times because of the imperfections of the randomizers used. David (1955, 1962) has pointed out that instead of regular dice, astragali (heel bones of hooved animals) were normally used, and Samburski (1956) remarks that in a popular game with four astragali, a certain throw was valued higher than all the others despite the fact that other outcomes have smaller probabilities, which indicates that the Greeks had not noticed the magnitudes of the corresponding relative frequencies.

# Pascal and Fermat's solution
Pascal and Fermat's story is well known. In a [famous correspondence](https://www.york.ac.uk/depts/maths/histstat/pascal.pdf) in the 1654, they developed the basic notion of probability and expected value.

Keith Devlin (2008):

> Before we take a look at their exchange and the methods
> it contains, let’s look at a present-day solution of the simple
> version of the problem. In this version, the players, Blaise
> and Pierre, place equal bets on who will win the best of five
> tosses of a fair coin. We’ll suppose that on each round, Blaise
> chooses heads, Pierre tails. Now suppose they have to abandon
> the game after three tosses, with Blaise ahead 2 to 1.
> How do they divide the pot?
> The idea is to look at all possible ways the game might
> have turned out had they played all five rounds. Since Blaise
> is ahead 2 to 1 after round three, the first three rounds must
> have yielded two heads and one tail.
> The remaining two throws can yield
> 
> HH HT TH TT
> 
> Each of these four is equally likely. In the first (H H), the
> final outcome is four heads and one tail, so Blaise wins; in
> the second and the third (H T and T H), the final outcome is
> three heads and two tails, so again Blaise wins; in the fourth
> (T T), the final outcome is two heads and three tails, so
> Pierre wins. This means that in three of the four possible
> ways the game could have ended, Blaise wins, and in only
> one possible play does Pierre win. Blaise has a 3-to-1 advantage
> over Pierre when they abandon the game; therefore,
> the pot should be divided 3/4 for Blaise and 1/4 for Pierre.
> Many people, on seeing this solution, object, saying that
> the first two possible endings (H H and H T) are in reality
> the same one. They argue that if the fourth throw gives a
> head, then at that point, Blaise has his three heads and has
> won, so there would be no fifth throw. Accordingly, they
> argue, the correct way to think about the end of the game is
> that there are actually only three possibilities, namely
> 
> H TH TT
> 
> in which case, Blaise has a 2-to-1 advantage and the pot
> should be divided 2/3 for Blaise and 1/3 for Pierre, not 3/4 and
> 1/4. This reasoning is incorrect, but it took Pascal and Fermat
> some time to resolve this issue. Their colleagues, whom they
> consulted as they wrestled with the matter, had differing opinions.
> So if you are one of those people who finds this alternative
> argument appealing (or even compelling), take heart; you
> are in good company (though still wrong).
> 
> The issue behind the dilemma here is complex and lies at
> the heart of probability theory. The question is, What is the
> right way to think about the future (more accurately, the
> range of possible futures) and model it mathematically?


The key insight was one that Cardano had already flailingly grapsed at, but was difficult to understand even for Pascal:

> As I observed earlier in this chapter, Cardano had already
> realized that the key was to look at the number of points
> each player would need in order to win, not the points they
> had already accumulated. In the second section of his letter
> to Fermat, Pascal acknowledged the tricky point we just encountered
> ourselves, that you have to look at all possible
> ways the game could have played out, ignoring the fact that
> the players would normally stop once one person had clearly
> won. But Pascal’s words make clear that he found this hard
> to grasp, and he accepted it only because the great Fermat
> had explained it in his previous letter.

Elsewhere, Keith Devlin writes:

> Today, we would use the word probability to refer to the
> focus of Pascal and Fermat’s discussion, but that term was
> not introduced until nearly a century after the mathematicians’
> deaths. Instead, they spoke of “hazards,” or number of
> chances. Much of their difficulty was that they did not yet
> have the notion of mathematical probability—because they
> were in the process of inventing it.
> 
> From our perspective, it is hard to understand just why they
> found it so difficult. But that reflects the massive change in
> human thinking that their work led to. Today, it is part of our
> very worldview that we see things in terms of probabilities.


# Extensions
## Handing over to mathematics
Solving a philosophical problem is to take it out of the realm of philosophy. Once the fundamental methodology is agreed upon, the question can be spun off into its own independent field.

The development of probability is often considered part of Pascal's mathematical rather than philosophical work. But I think the mathematisation of probability is in an important sense philosophical. In [another post](/ps_looks-like), I write much more about why successful philosophy often looks like mathematics in retrospect.

After Pascal and Fermat's breakthrough, things developed very fast, highlighting once again the specificity of that ititial step.

Keith Devlin writes:
> In 1654, Pascal had struggled hard to understand why
> Fermat counted endings of the unfinished game that would
> never have arisen in practice (“it is not a general method
> and it is good only in the case where it is necessary to play
> exactly a certain number of times”). Just fifteen years later,
> in 1669, Christiaan Huygens was using axiom-based abstract
> mathematics on top of statistically processed data tables to
> determine the probability that a sixteen-year-old young man
> would die before he reached thirty-six.

After the crucial first step for formalisation, probability was ripe to be handed over to mathematicians. SEP writes:
> These early calculations [of Pascal, Fermay and Huygens] were considerably refined in the eighteenth century by the Bernoullis, Montmort, De Moivre, Laplace, Bayes, and others (Daston 1988; Hacking 2006; Hald 2003). 

For example, the crucial idea of _conditional probability_ was developed. According to [MathOverflow](https://mathoverflow.net/questions/163582/what-is-the-early-history-of-the-concepts-of-probabilistic-independence-and-cond), in the 1738 second edition of _The Doctrine of Chances_, de Moivre writes,
> The Probability of the happening of two Events dependent, is the product of the Probability of the happening of one of them, by the Probability which the other will have of happening, when the first shall be consider'd as having happened; and the same Rule will extend to the happening of as many Events as may be assigned.

People began to _get it_, philosophically speaking. We begin to see quotes that, unlike those of Circeo, sound decidedly modern. In his book Ars conjectandi (The Art of Conjecture, 1713), Jakob Bernoulli wrote:
> To conjecture about something is to measure its probability.
> The Art of Conjecturing or the Stochastic Art is therefore
> defined as the art of measuring as exactly as possible the
> probabilities of things so that in our judgments and actions
> we can always choose or follow that which seems to be better,
> more satisfactory, safer and more considered.

Keth Devlin writes:
> Within a hundred years of Pascal’s letter, life-expectancy
tables formed the basis for the sale of life annuities in England,
and London was the center of a flourishing marine insurance
business, without which sea transportation would
have remained a domain only for those who could afford to
assume the enormous risks it entailed. 

## Axiomatisation
Much later, probability theory was put on an unshakeable footing, with [Kolomogorov's axioms](https://en.wikipedia.org/wiki/Probability_axioms). 


# Counter-intuitive implications of probability theory
I've given many examples of how people used to be confused about probability. In case you find it hard to empathise with these past thinkers, I should remind you that even today probability theory can be hard to grasp intuitively.
## The conjunction fallacy
[Wikipedia](https://en.wikipedia.org/wiki/Conjunction_fallacy):
> The most often-cited example of this fallacy originated with Amos Tversky and Daniel Kahneman. Although the description and person depicted are fictitious, Amos Tversky's secretary at Stanford was named Linda Covington, and he named the famous character in the puzzle after her.
> 
> > Linda is 31 years old, single, outspoken, and very bright. She majored in philosophy. As a student, she was deeply concerned with issues of discrimination and social justice, and also participated in anti-nuclear demonstrations.
> >
> > Which is more probable?
> >
> >1. Linda is a bank teller.
> >2. Linda is a bank teller and is active in the feminist movement.
> 
> The majority of those asked chose option 2. However, the probability of two events occurring together (in "conjunction") is always less than or equal to the probability of either one occurring alone.

## The monty hall problem
[Wikipedia](https://en.wikipedia.org/wiki/Monty_Hall_problem):
> > Suppose you're on a game show, and you're given the choice of three doors: Behind one door is a car; behind the others, goats. You pick a door, say No. 1, and the host, who knows what's behind the doors, opens another door, say No. 3, which has a goat. He then says to you, "Do you want to pick door No. 2?" Is it to your advantage to switch your choice?
> 
> Vos Savant's response was that the contestant should switch to the other door (vos Savant 1990a). Under the standard assumptions, contestants who switch have 2/3 chance of winning the car, while contestants who stick to their initial choice have only a 1/3 chance.
> 
> The given probabilities depend on specific assumptions about how the host and contestant choose their doors. A key insight is that, under these standard conditions, there is more information about doors 2 and 3 that was not available at the beginning of the game, when the door 1 was chosen by the player: the host's deliberate action adds value to the door he did not choose to eliminate, but not to the one chosen by the contestant originally.

## The mammography problem
Yudkowsky:

> > 1% of women at age forty who participate in routine screening have breast cancer.  80% of women with breast cancer will get positive mammographies.  9.6% of women without breast cancer will also get positive mammographies.  A woman in this age group had a positive mammography in a routine screening.  What is the probability that she actually has breast cancer?
> 
> What do you think the answer is?  If you haven't encountered this kind of problem before, please take a moment to come up with your own answer before continuing.
> 
> Next, suppose I told you that most doctors get the same wrong answer on this problem - usually, only around 15% of doctors get it right.  ("Really?  15%?  Is that a real number, or an urban legend based on an Internet poll?"  It's a real number.  See Casscells, Schoenberger, and Grayboys 1978; Eddy 1982; Gigerenzer and Hoffrage 1995; and many other studies.  It's a surprising result which is easy to replicate, so it's been extensively replicated.)

Most doctors estimate the probability to be between 70% and 80%. The correct answer is 7.8%.

<hr> <!-- hr to be added before footnotes--> 