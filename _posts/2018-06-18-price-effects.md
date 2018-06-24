---
layout: post
title: "Should we prioritise cash transfers to the urban poor?"
---

_Note: I owe these ideas to Rossa O'Keeffe-O'Donovan and Natalie Quinn. However, the views expressed here are solely mine._

It's well known that cash transfers have effects on prices. For instance, [Cunha, De Giorgi and Jayachandran](https://www.povertyactionlab.org/evaluation/price-effects-cash-versus-kind-transfers-mexico) (2017) write:
> [According to standard models], cash transfers increase the demand for normal goods, which will lead to price increases. This prediction holds either with perfect competition and marginal costs that are increasing in quantity, or with imperfect competition even if marginal costs are constant or decreasing [...].

It's helpful to think in terms of real goods instead of thinking in terms of money. Suppose there was a village in complete autarky: trade only occurs within the village. Say we gave everyone in the village $1,000. Nothing on the ground directly changes: they don't get better tools, or more fertile land, just because we give them fiat money. What happens to consumption depends on the income distribution prior to the transfer. If all villagers have the same income, they will keep producing the same goods as before, and exchanging them in the same way, the prices will simply be higher[^cd]. If they had different incomes, the cash transfer will make them more equal in purchasing power, while also increasing prices (imagine if the transfer was a billion dollars). This amounts to a modest transfer of real goods from richer to poorer villagers[^goods].

[^goods]: The more equal village might also shift its production and consumption towards more staples and fewer luxuries.

[^cd]: This is known as the classical dichotomy in economics.

Now suppose we only gave $1,000 to a randomly selected half of the villagers. Nothing immediately happens to the productive capacity of the village. Prices rise, which means purchasing power is transferred from non-recipients to recipients. The exact effect on consumption is a bit complicated. In an extremely simple economy where everyone consumes as much as possible of the staple good, recipients consume more, non-recipients consume less, and that's the end of it. More realistically, the recipients create some new demand for luxury goods. Regardless, the welfare effect of the purchasing power transfer seem likely to be negative. What certainly _doesn't_ happen is that real goods are transferred from the person who funded the cash transfer programme (say, a GiveDirectly donor) to anyone in the village. This is impossible since the village is in autarky.

# Even imperceptible price effects can change everything
If the village were trading with other villages, the price increases would be more spread out, and the effect would be a transfer of purchasing power to the recipients from everyone else in the trade market. More generally, a cash transfer to recipient A is a real good transfer to A, from everyone who trades with A, directly or indirectly. An interesting empirical point is the following. If the market is large, the price effects could be spread across tens of thousands of people, thus they would be very small for each person. Then extremely high statistical power is required to distinguish these price effects from zero. But imperceptible effects on large numbers of people can still be very morally important (see Parfit's _Five Mistakes in Moral Mathematics_). In this case, the imperceptible price effects reflect the fact that the cash transfer can't increase real consumption within the market. So they are everything that matters!

In the case of GiveDirectly, things aren't quite as bad as in my toy examples above. GiveDirectly targets the poorest inhabitants in a village, so even if the village were in complete autarky, GiveDirectly would cause a real goods transfer from richer inhabitants of the village to the poorer inhabitants (and a much bigger one than if the transfer was given to everyone). If all of western Kenya was in autarky, but there was costless trading within, the transfer would be from everyone in western Kenya (weighted by how much they consume) to the recipients. Notice how different this is from what we might have expected before taking into account price effects: a real transfer from the GiveDirectly donor to the recipient.

Cunha and colleagues' empirical findings corroborate this:
> In the more economically developed villages in the sample, households’ purchasing power is only modestly affected by these price effects. In the less developed villages, the price effects are much larger in magnitude, which we show is partly due to these villages being less tied to the outside economy and partly due to their having less competition among local suppliers.

Now let's take another case: you give money to your neighbour (who like you, has perfect access to the world economy). There is no price effect. You both would have spent the money on the world market. There is a real goods transfer from you to your neighbour. This is the only case where reality perfectly matches intuition. The same would happen if your neighbour were a Kenyan who has access to world markets[^clar].

[^clar]: Except for the fact that Kenya uses a different currency, so you have to take into account exchange rates, which might not be free-floating. I don't understand macroeconomics, so let's ignore that.

# The upshot
Now, to me there is an obvious policy implication here: you should transfer cash not to the poorest, but to those who score highest on some combination of low income and access to the world economy. Income being equal, you should transfer to the most globalised recipients you can find. The importance of this can be enormous. If you give to someone in an autarkic village, you transfer goods from poor Kenyans to very poor Kenyans. If you give to a globalised city-dweller, the real transfer is from yourself to the recipient.

I haven't been able to find any discussion of this policy implication in the literature. This is quite surprising for something that naturally follows from supply and demand theory.

There could be practical problems with this policy. Most obviously, people who live in globalised cities are typically rich, and those who live in isolated villages are typically poor. So the ideal recipient, say someone who lives in Mumbai but is as poor as a rural day labourer, may not exist. (It could also be harder to identify the poor in the cities. But the operation costs of a cash transfer programme could perhaps be lower.)

There is some empirical data on this, for example from the World Bank report [_Geographic Dimensions of Well-Being in Kenya: Where are the Poor?_](http://econ.worldbank.org/external/default/main?theSitePK=477894&contentMDK=20306724&menuPK=545573&pagePK=64168182&piPK=64168060) (henceforth GdWBK). GdWBK chapter 2 tells us that the "poverty line is determined based on the expenditure required to
purchase a food basket that allows minimum nutritional requirements to be met (set at 2,250 calories per adult equivalent (AE) per day) in addition to the costs of meeting basic non-food needs". The rural poverty line (Ksh 1,239) is less than half the urban poverty line (Ksh 2,648). I find it surprising that basic goods really are twice as expensive in urban areas, but let's take these estimates at face value. GdWBK doesn't directly give information about the income distribution, but it tells us about the _poverty gap index_ in different areas.

[Wikipedia](https://en.wikipedia.org/wiki/Poverty_gap_index) defines the poverty gap index as $$\frac{1}{N} \sum_{j=1}^{q} \left( \frac{z-y_j}{z} \right)$$ where $$N$$ is the total population, $$q$$ is the total population of poor who are living at or below the poverty threshold, $$z$$ is the poverty line, and $$y$$ is the income of the poor individual $$j$$. In this calculation, individuals whose income is above the poverty line have a gap of zero. Multiplying the poverty gap index by $$\frac{N}{q}$$, we get $$PG_p = \frac{1}{q} \sum_{j=1}^{q} \left( \frac{z-y_j}{z} \right)$$, the average poverty gap among the poor.

From GdWBK chapter 5, I compute $$PG_p=49\%$$ for the rural areas of the Western District of Kenya, $$PG_p=33\%$$ for the district of Nairobi, implying that the Nairobian poor live on an average of 67% of the urban poverty line and the poor in rural parts of the Western District live on an average of 51% of the rural poverty line.

<hr> <!-- hr to be added before footnotes-->
