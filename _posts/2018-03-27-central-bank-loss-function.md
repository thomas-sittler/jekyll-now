---
layout: post
title: "Understanding central bank loss functions"
---

_Note: this post is unlikely to be of interest if you haven't done a basic undergraduate course in macroeconomics._

I use notation and terminology from Carlin and Soskice (2015).

What is the central bank (CB) trying to achieve? In discussing the CB's goals, it's important to distinguish _rates of change_ in inflation from _levels_ of inflation.

# Costs of high rates of change in inflation
## 1
The CB wants to avoid runaway inflation or deflation. If inflation is high (or low) because the labour market (WS-PS model) is out of equilibrium, then inflation may increase (or decrease) without bound. The CB wants to set employment and output to the level consistent with a WS-PS equilibrium, where inflation will be constant.

The goal of constant inflation could in theory be achieved at any level of inflation.

## 2
There is another, conceptually distinct cost of volatile inflation. Volatile inflation interferes with the ability of prices to convey information. It masks relative price changes. 

# Levels of inflation, and their costs and benefits
## 1
There are costs to high absolute values of $$\pi$$:
* Increased menu costs
* High inflation incentivises making purchases quickly and holding no cash, while large deflation incentivises delaying purchases and holding cash.

## 2
There are also benefits to higher levels of inflation. Workers are particularly resistant to nominal wage cuts. So inflation oils the wheels of the labour market.

# Which level?
As we said above, the bank's primary concern is to avoid runaway inflation or delfation. But what level of inflation should the CB target? Inflation has costs and benefits. So it might not seem unreasonable to target $$\pi=0$$ or even $$\pi<0$$. But there is a good reason to aim for a positive level of inflation. Because of the zero lower bound on $$i$$, it’s more prudent to stay away from low or negative $$\pi$$. Suppose aggregate demand falls when $$\pi = -x$$. Then $$r=i-\pi$$ has a lower bound of $$x$$ and cannot be lowered enough to bring the WS-PS market into equilibrium. The result is a deflationary spiral. 

This argument works for both positive $$x$$ and $$x=0$$. 

Even if $$i$$ is not currently at the ZLB, there could be measurement error or forecasting failures, so that $$i$$ could unexpectedly hit the ZLB. The CB uses a target $$\pi>0$$ to stay safely away from the ZLB.

In fact, the target rate of $$\pi^T=2\%$$ is typically used. Why 2%? We have seen that the ZLB provides a good reason to avoid levels of inflation very close to zero. But why not target higher inflation? The qualitative considerations discussed above could go either way, and provide no particular justification for the specific choice of $$\pi^T=2\%$$. Choosing the optimal level of inflation is a very difficult empirical and moral question.

# A typical loss function
The CB is conventionally taken to be minimising, at each time $$t$$:

$$L=(y_t - y_e)^2 + \beta(\pi_t - \pi^T)^2$$

This loss function makes no sense from the point of view of the considerations we discussed above. 

First, the loss function tells us that the CB does not care about rates of change in inflation at all. It is perfectly myopic, and never looks beyond the current period. But runaway inflation and deflation are catastrophic, and avoiding them should arguably by the CB's primary goal.

Second, when $$y_t>y_e$$, the loss function penalises higher output. But getting richer is usually taken to be a good thing.

I think there's a confusion here between final and instrumental goals. Minimising $$L$$ makes no sense as a final goal. But in practise, $$L$$ is a good rule of thumb for avoiding runaway inflation or deflation. Penalising output above $$y_e$$ while ignoring future inflation may lead to policies which approximate the CB's true final goals. 

Carlin and Soskice write: "The policy maker is modelled as an inflation-targeting central bank not because this is necessarily the best policy-making arrangement, but because it most closely resembles hoe modern stabilisation policy is undertaken". They also say: "Note that this loss function [...] assumes a symmetrical attitude to positive and negative deviations [...] from the equilibrium level of output. The most straightforward way of thinking about this is that the central bank understands the model and realises that inflation is only constant at $$y_t=y_e$$. If $$y_t<y_e$$ then this represents unnecessary unemployment that should be eliminated. If $$y_t> y_e$$, this is unsustainable and will require costly increases in unemployment to bring the associated inflation back down".

Unfortunately, I think this confuses rather than clarifies matters. According to the WS-PS model, $$y_t < y_e$$ will lead to runaway deflation, and $$y_t>y_e$$ will lead to runaway inflation. In the same breath, the authors mix instrumental goals ("If $$y_t > y_e$$, this is unsustainable and will require costly increases in unemployment...") and final goals ("If $$y_t<y_e$$ then this represents unnecessary unemployment"). 

Instead, I think the (final) loss function of the CB should be something like:

$$L = \sum_{t=0}^\infty \delta^t (\beta y_t - \gamma(\pi_t-\pi^T)^2 -\theta(\pi_t - \pi_{t-1})^2) $$, 

where $$\delta$$ is the discount factor, $$\beta y_t$$ represents the fact that more output is good, $$\gamma(\pi_t-\pi^T)^2$$ reflects the fact that inflation has costs and benefits, so we want to aim for an optimal rate $$\pi^T$$, and $$\theta(\pi_t - \pi_{t-1})^2$$ is present because volatile inflation is costly.


<hr> <!-- hr to be added before footnotes--> 