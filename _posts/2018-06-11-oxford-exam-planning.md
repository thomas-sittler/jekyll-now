---
layout: post
title: "How I budgeted my time for Oxford final exams"
---

PPE finals are eight high-stakes examinations on two years' worth of material, composed of eight modules. Everyone dedicates at least their last term to revision, during which no new modules are added. Many PPE students even finish their eight modules two terms before exams (at the end of Michaelmas term of their third year), which theoretically leaves six months between the time they stop learning new material and the time they are examined.

How much explicit planning should go into finals revision? I am generally wary of over-planning, especially with rigid, brittle plans over long time horizons. The plan often ends up being inadequate, not following the plan causes [guilt](http://mindingourway.com/guilt/), and constantly revising it costs a lot of effort[^complice]. On the other hand, when the stakes and the risk of akrasia are both high, planning could have outsize returns.

[^complice]: That's why I like [Complice](https://complice.co/?r=tecqqc10rc), which makes you choose fresh, relevant actions every day and prohibits pile-ups of unfinished tasks.

There are many aspects of planning for exams. Here I focus on just one: budgeting time between different topics for revision. This is especially difficult to do with raw intuition: it always feels like you've got ages left until exams, until you don't. It's typical for people to take a leisurely stroll through material that they enjoy, deepening their understanding, which leaves little time for the more difficult and aversive stuff. (Given how easily I get [nerd-sniped](https://xkcd.com/356/) by my favourite topics, this is an especially worrying pitfall for me.)

To budget my time, I used this [spreadsheet](https://docs.google.com/spreadsheets/d/1epgl6FeMXGcaCC_GVUz2aVqYVnHFDS4ed3a3wKXL6C4/edit?usp=sharing), which you can copy and adapt[^fn]. I'll discuss some of its features now.

[^fn]: I've removed most of the data to protect my privacy, but I've kept the percentages for illustration in ``Sheet1_hardcoded_data``. You'll also come across some negative numbers because the beginning of exams is now in the past. Data input cells are in orange. Sheets ``2015``, ``2016``, and ``2017`` are where the data from examiner's reports is stored.

# Dividing the remaining time
The most basic feature is a simple reality check: how many days until exams? (This is calculated dynamically using ``=TODAY()``.) Dividing by eight, how many per module? This simple calculation could be enough to snap you out of the vague feeling that there is "a lot" of time left. Maybe there really is ample time. Why not find out exactly how much, so you can use it best? Maybe once you do the maths you realise there isn't. In that case this simple division provides a salutary wake-up call.

Further adjustments could be useful. I'd recommend planning some days off, like one day a week, and certainly a few full days before exams (cramming is counter-productive). If you're travelling or doing any projects, subtract those days _explicitly_ from the total.

If your modules have themselves a modular structure, like independent chapters of a textbook, you might consider further subdividing the time between them. Maybe you'll get something like 0.12 days per chapter, which at five hours a day is 36 minutes, something so close to the skin your system 1 might actually be able to process it. In my experience it's pretty rare for intellectual material to actually have such independent chunks, when you zoom in all the way, even though it might superficially be organised into discrete topics.

# Allocating time between modules in proportion to their variance
If you're trying to maximise your expected mark, allocating more time to higher-variance papers makes sense. To be precise, if your mark in each paper is the square root of time allocated times the standard deviation, the sum of the marks is maximised by allocating time in proportion to the variance.

I looked up the variance in marks for each paper since 2015, the first year this information was available in the PPE examiner's reports. I then averaged the three variances[^wt] for each paper. For a PPE student taking my eight papers, I computed how much of the total variance has historically been contributed by each paper.

[^wt]: Not weighted by number of candidates each year, too much of a hassle for something I expect would make little difference. 

The results are pretty striking. For example Game Theory contributed more than four times as much variance as Knowledge and Reality. I think these fractions are a better starting point for time budgeting than allocating time equally between the modules. 

But allocating time purely by the variance has some pretty obvious flaws. For starters, there are strong selection effects: some papers are mandatory for everyone, while others select for the most capable and interested students. For instance, if all but the nerdiest of nerds avoid econometrics, we should expect the variance to be artificially low for that paper. Then there is the fact that some modules build on each other while others do not: econometrics is basically an advanced version of quantitative economics, so there is little point doing quantitative economics-specific revision over and above what I do for econometrics. And finally you need to adjust for factors idiosyncratic to you: I basically snoozed through Macroeconomics last year while I was busy with an unrelated research project. I ended up with these target allocations:

<!-- Variances and targets -->
<iframe width="544.5" height="336.6825" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRhY1mCz4W5IUMWhUejh0pcksGm6cR5oYzRmka-NoktBRR_0HeYH20dLpHSB-VYQsbCBQs9Nnr1HGrQ/pubchart?oid=359285040&amp;format=interactive"></iframe>


# Planning for humans: built-in updating
A crucial feature of a good revision plan is that it adapts gracefully when you don't get as much done as you hoped. You shouldn't have to scramble to adjust your plan after the fact, cursing your weakness of will. It should be baked into the design from the start.

On one view of plans, they are what you _should_ do, and a feeling of guilt when you don't follow them is not only natural but appropriate. A view that I've often found more fruitful is to treat plans as just another tool of instrumental rationality. This may seem like an obvious point, but for many people, myself included, it's much harder to grasp on an intuitive level, and harder still to implement. On this topic I highly recommend reading Nate Soares' [replacing guilt series](http://mindingourway.com/guilt/).

When you fall behind your initial plan, it can be tempting to think you can accelerate to make up for lost time. But I think this is rarely realistic. When you don't work as hard as you had planned, this constitutes evidence that your plan is too ambitious for the future as well as the past. I have often ignored this evidence and paid the price for it. Accelerating is an especially bad idea when you need to allocate your effort over weeks rather than days or hours. Like many beginning endurance runners, if you run that fast you'll end up collapsing before the finish line.

I used the [Pomodoro technique](https://en.wikipedia.org/wiki/Pomodoro_Technique): 25-minute segments of focused work followed by a five-minute break. Apart from its other benefits, this technique provides a nice and tangible unit to measure time. At any point in time I want to be solving this equation:

$$\frac{PA_i+S_i}{D+ \sum_i S_i} = T_i$$

This graph shows $$A_i/S_i$$:

<!-- ![future target / historical share] -->
<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRhY1mCz4W5IUMWhUejh0pcksGm6cR5oYzRmka-NoktBRR_0HeYH20dLpHSB-VYQsbCBQs9Nnr1HGrQ/pubchart?oid=1522612418&amp;format=interactive"></iframe>

Where $$P$$ is the number of pomodoros left until exams, $$S_i$$ is the number of pomodoros spent on module $$i$$ so far, $$T_i$$ is the overall target allocation for module $$i$$, and $$A_i$$ is the allocation (out of $$P$$) to now be spent on module $$i$$. For this, I need to manually keep track of an additional variable, $$S_i$$. I do this on ``Sheet2``.

We can do interesting things with $$P$$. The simplest estimate of $$P$$ is simply a constant number of pomodoros times the number of days left until exams (running the entire marathon at the same speed). This is sufficient to give you the first feature of the equation: automatic adjustment to the passing of time. 

Tracking $$S_i$$ enables a second nice feature. By computing your average number of pomos per day ($$\sum_i S_i$$ divided by the number of days since you started revising), and extrapolating it, you obtain a realistic estimate of $$P$$. This gives you automatic adjustment for your actual capacity to do work. You needn't slavishly extrapolate this average. But it should feed into your estimate of $$P$$. If you plan to work 10 pomos a day but so far you've only done an average of 4 pomos a day, that should raise a red flag.

Diminishing returns suggest that it's best to always work on the module for which $$T_i/S_i$$ (depicted below) is largest.

<!-- Overall target / historical share -->
<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRhY1mCz4W5IUMWhUejh0pcksGm6cR5oYzRmka-NoktBRR_0HeYH20dLpHSB-VYQsbCBQs9Nnr1HGrQ/pubchart?oid=1342701044&amp;format=interactive"></iframe>

# The budget as a part of a larger decision-making procedure
I often disregarded the numbers based on hunches and intuitions, especially when I felt that my intuitions were capturing some unmodeled factor (for instance when I felt confident about a topic without having spent much time revising it, or when I postponed revision on exams which came later). 

I fully expected that I would do this. Getting up every day and following the dictates of the spreadsheet would have been an instance of Spock-like ["straw vulcan" rationality](https://www.lesswrong.com/posts/z9hfbWhRrY2Pwwrgi/summary-of-the-straw-vulcan). Instead, I viewed the model and the intuitive view as two different tools at my disposal, or as two adivsors, each with her own bias.

I thought of the division of labour in something like the following way. The whole case for making an explicit, numerical budget is that the intuitive System 1 is about as good at long-term planning as a toddler in a casino. The spreadsheet is excellent at remembering what you did, keeping track of the long-term goals, feeding historical data into your decision making process, and most importantly, it does not self-delude. However, it is a woefully simplified model of the actual task of taking eight exams while trapped in a human body with a fleshy brain. Millions of variables are boiled down to a handful. The model is computationally puny next to the awesome power of your System 1, whose inclinations are based on a great deal of contextual information which your brain constantly gobbles up. System 1 shines at taking in a huge amount of relevant information and boiling it down to an up-or-down judgement: Game Theory today, yea or nay? The spreadsheet is good at correcting some of the biases of System 1 and at giving enough weight to the data on variances, which is crucial but not at all salient.

# How useful was all this planning?
Looking back, how much did the budget actually change my decisions? I ended up using the model mostly as a guardrail, reminding me to allocate more time to a module when its ratio $$A_i/S_i$$ became something outrageous like 300%.  I didn't pay much attention to the exact numbers on a day-to-day basis. But averaging over the long run, I think the budget substantially affected my decisions. In particular, it made me spend much less time on low-variance philosophy papers and more on game theory and microeconomics. 

Another intended purpose of the spreadsheet was to help me smooth my effort more over time. Looking back, I'm a bit disappointed by how much harder I worked when finals were approaching than when they were more distant. But it probably would have been even worse with less planning. My best guess is that the spreadsheet had a minor positive impact in this respect. To be fair, effort and consumption smoothing is, in general, a very difficult task for human motivation.

My final allocations turned out to be pretty close to the targets even though I didn't strongly intend them to. 

<!-- final allocs and targets -->
<iframe width="600" height="371" seamless frameborder="0" scrolling="no" src="https://docs.google.com/spreadsheets/d/e/2PACX-1vRhY1mCz4W5IUMWhUejh0pcksGm6cR5oYzRmka-NoktBRR_0HeYH20dLpHSB-VYQsbCBQs9Nnr1HGrQ/pubchart?oid=1675380174&amp;format=interactive"></iframe>

Given the high stakes and the relatively low time cost, I think this project was amply worth it. Setting up the spreadsheet took only a few hours. The main cost was the hassle of keeping track of daily time use. The single biggest win was to do the research on the variances. For this insight I thank my friend Rune Tybirk Kvist, who completed finals one year before me.

<hr> <!-- hr to be added before footnotes--> 