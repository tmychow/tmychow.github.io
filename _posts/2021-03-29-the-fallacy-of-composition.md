---
layout: post
title: "The Fallacy of Composition"
date: 2021-03-29
tags: economics effortposts
---

**Description**: Hopefully in a single post this will bring you up to speed from knowing nothing about business cycle macroeconomics till you know everything you want to know about it at an intermediate macro level. We'll mess around with the notion of goods and money market equilibrium to see where it takes us, borrowing generously from [Miles Kimball](https://blog.supplysideliberal.com/) and [Nick Rowe](https://worthwhile.typepad.com/worthwhile_canadian_initi/nick-rowe/). This is probably, even more than [my growth series](https://tmychow.com/blog/2020/07/02/growth-a-primer-in-three-parts), the hardest I've tried at making things accessible and clear, so please do get in touch if you think there are things which are underexplained or could be rewritten.

**Table of Contents**

1. [Macro Isn't Bigger Micro](#macro-isnt-bigger-micro)
2. [Stories of the Supply Side](#stories-of-the-supply-side)
3. [Stories of the Demand Side](#stories-of-the-demand-side)
4. [Designing Monetary Regimes](#designing-monetary-regimes)
5. [The Neomonetarists Strike Back](#the-neomonetarists-strike-back)
6. [Parsimonious Models](#parsimonious-models)

#### Macro Isn't Bigger Micro

Consider a simple supply and demand diagram in microeconomics as below. We have an upwards-sloping supply curve and downwards-sloping demand curve in the (quantity, price) space. What are the "microfoundations" for this? Verbally, it goes as follows. Sellers try to maximise profit, which is the price minus the cost of production. When the price rises, the profit-maximising level of output is higher and they want to sell more. Meanwhile, buyers try to maximise the utility they get from buying stuff, subject to a budget constraint. A higher price means that the bang-per-buck for that good is lower, so they want to buy less of it.

![Supply and Demand Diagram](/assets/supplydemand.png){:width="675px"}

But this same logic doesn't work when we think about aggregate supply and aggregate demand diagrams in macroeconomics, which is in the (output, price level) space. If the overall price level in the economy went up as a whole, that just means the price of every single good went up - there's no story here for why sellers would want to supply more. Indeed, the classical dichotomy suggests that the amount of stuff that suppliers can produce in the economy is entirely unrelated to nominal quantities like prices. Likewise, if prices on everything went up, it's not obvious that people would want to buy more stuff. So we cannot just bring these microeconomic intuitions over to macroeconomics, and to do so would commit a fallacy of composition.

Instead, the reason we have upwards-sloping AS curves and downwards-sloping AD curves has to do with the fact that we live in a monetary exchange economy where money plays a role in transactions, as opposed to some sort of barter system or Walrasian auctioneer. In this post, I want to carefully explore the stories behind why we get the three curves from the very beginning and unravel why some of the usual explanations we tell might be uncompelling.

#### Stories of the Supply Side

The supply side consists of two curves. In the long run, the amount of stuff that the economy can supply has everything to do with its productive potential and nothing to do with the price level. So the long run aggregate supply curve is just a vertical line. But in the short run, money is non-neutral with respect to output, and so the short run aggregate supply curve slopes upwards in the (output, price level) space. What are the "microfoundations" for this?

The traditional Keynesian story is about nominal wage rigidity. Because people engage in wage contracts that are denominated in nominal terms and because these contracts last a while, nominal wages are sticky. If the price level rises, this means that real wages will fall since nominal wages stay the same. Because firms care about the real costs they face, they will be willing to hire more workers to produce more. The New Keynesian story is about nominal price rigidity. Firms may be loathe to change prices unless other firms do so as well, since their relationships with customers may be hurt - this combination of a coordination failure and implicit contracts with buyers means firms will adjust on other margins instead of changing prices. If the price level rises but their own prices are sticky, this means that they will supply more of their good. The New Classical story is about imperfect information. If prices rise for their goods, they have to conduct a form of signal extraction in order to determine whether or not this is a change in the relative price of their good or a rise in the overall price level. If it is the former, we know from our story about the single market supply-and-demand diagram that suppliers will produce more. If it is the latter, we know from our story about the LRAS that they should not change their output due to a purely nominal change. Their inability to tell which it is immediately means they have to attach a probability to both - as such, they will produce more if the price level rises. So we have three stories for why there is a positive relationship between output and the price level. Crucially, all three stories are about the short run - over time, all three frictions of wages, prices and information will adjust until we return to the level implied by the LRAS. But nonetheless, we have plausible "microfoundations" for an upwards-sloping SRAS curve but a vertical LRAS curve.

#### Stories of the Demand Side

If we move on to the aggregate demand curve, we again have three "microfoundations" for why it might slope downwards in the (output, price level) space.

**Old Keynesian Explanation**

The Old Keynesian explanation is the traditionally taught approach and focuses on the IS-LM model. This model reconciles equilibrium in the market for goods with equilibrium in the market for money. Consider the three components of planned expenditure $E$ as consumption $C$, investment $I$ and government spending $G$. We will assume that people consume more with a higher income i.e. consumption is an increasing function of income $C=C(Y)$. We will assume that firms invest more when there is a lower real interest rate, since borrowing is cheaper and saving is less worthwhile i.e. investment is a decreasing function of real interest rates $I=I(r)$. And we will assume that government spending is set at an exogenous and predetermined level of $G=\bar{G}$. In order for the goods market to be in equilibrium, the amount of actual expenditure $A$ which equals output $Y$ must also be the same as planned expenditure. We can draw these two out in the Keynesian cross.

$$ E = C(Y) + I(r) + \bar{G} $$

$$ A = Y $$

![Normal Keynesian Cross](/assets/keynesian.png){:width="675px"}

The point at which they intersect is where the goods market is in equilibrium. If we are to the left of the intersection, output is less than the planned expenditure, resulting in firms raising production and using up inventories. This brings us in the direction where the two equalise. A similar process operates vice versa when actual output is greater than planned expenditure, with firms building up inventory and cutting output. We can see that the IS curve below describes the equilibrium condition when $A=E$.

$$ Y = C(Y) + I(r) + \bar{G} $$

We can also think of the IS curve graphically. Suppose there is a lower real interest rate $r$. This will increase $I$ and shift $E$ upwards. As such, the point at which it intersects $A$ will be at a higher $Y$. Consequently, we get a downwards-sloping IS curve in $\{Y,r\}$ space. The slope of the IS curve will depend on the interest elasticity of investment demand and the multiplier effect. This can be easily illustrated by considering a simple functional form for our IS curve, where $C=cY$ and $I=-br$, producing the following expressions based off of $Y=cY-br+\bar{G}$.

$$ Y = -\frac{br}{1-c} + \frac{\bar{G}}{1-c} $$

$$ r = - \frac{(1-c)Y}{b} + \frac{\bar{G}}{b} $$

If investment is more interest elastic i.e. $b$ is larger, a fall in $r$ will cause a larger increase in $Y$ via a rise in $I$, causing the IS curve to be flatter. If the multiplier effect $\frac{1}{1-c}$ is larger, a given fall in $r$ and rise in $I$ will cause a larger increase in $Y$, causing the IS curve to be flatter.

The market for money can be considered in a similar fashion. The supply of real money balances is the amount of money in the economy divided by the price level $\frac{M}{P}$. The demand for real money balances is greater if the amount of output is larger, since you will want to hold more money to buy things. However, it is lower as the nominal interest rate rises, since the interest foregone on holding money instead of financial assets is greater. That means we can think of the desire for liquidity $L(Y,i)$ as an increasing function of output and decreasing function of the nominal interest rate. The LM curve describes the equilibrium condition when the supply of money equals the demand for money.

$$ \frac{M}{P}=L(Y,i) $$

Suppose a fixed amount of real money balances $\frac{M}{P}$. If there is an increase in the level of output, the increased demand for real money balances will lead to people selling off financial assets for money. This reduces the price of these assets, raising their interest rate until the supply and demand for real money balances are back in equilibrium. That is, the LM curve slopes upwards in $\{Y,i\}$ space.

The slope of the LM curve will depend on the interest elasticity of money demand and the income elasticity of money demand. Again, we can provide a functional form by taking the LM curve as follows.

$$ \frac{M}{P} = gY - hi $$

$$ i = \frac{gY}{h} - \frac{1}{h} \frac{M}{P} $$

If money demand is more interest elastic i.e. $h$ is higher, a rise in $Y$ is associated with a smaller rise in $i$ and the LM curve is flatter. If money demand is less income elastic i.e. $g$ is lower, a rise in $Y$ is associated with a smaller rise in $i$ and the LM curve is flatter.

Right now, we have a problem - the IS curve is in real terms, while the LM curve is in nominal terms. We can resolve this by appealing to the Fisher equation $i=r+\pi$, which tells us that the nominal interest rate is approximately equal to the real interest rate plus the inflation rate. Within the IS-LM model, we assume that prices are fixed, meaning that inflation is 0. As such, we can replace $i$ with $r$ in the LM curve, producing the following IS-LM diagram in $\{Y,r\}$ space.

![IS-LM diagram](/assets/islmnorm.png){:width="675px"}

From this IS-LM model, we can derive an AD curve which represents the locus of points in $\{Y,P\}$ space where both the goods and money markets are in equilibrium. Consider a fall in $P$ - this will mean a higher level of real money balances $\frac{M}{P}$ when we hold the money supply $M$ constant, resulting in an outwards shift in the LM curve. This means it intersects the IS curve at a higher level of output $Y$. Thus we have an AD curve as a downwards-sloping relationship in $\{Y,P\}$ space.

![IS-LM into AD diagram](/assets/islmtoad.png){:width="675px"}

**The New Keynesian Explanation**

The New Keynesian explanation is the modern take, focusing on the behaviour of households and central banks. I won't write out the full New Keynesian model and derive it from the beginning, because the maths is frankly a bit excessive for our purposes - instead, I'll sketch out a stripped down version in the spirit of Clarida, Gali and Gertler's 3-equation model and you'll have to take me at my word that I didn't miss anything essential.

With respect to the goods market, we have a New Keynesian IS curve which is simply an Euler equation derived from the intertemporal optimisation of households. In effect, it relates output with expected output and the deviation of the real interest rate from its natural level. If people expect future output to be higher, they'll want more now. If the interest rate is above its natural level, firms will invest less for a similar reason as in the IS-LM model.

$$ Y = E(Y) - b(r-r^\ast) $$

For the money market, we have a monetary policy rule rather than assuming a fixed money suply - this produces a New Keynesian MP curve where the interest rate is set based on the natural rate of interest and the deviation of inflation from the central bank's inflation target. If inflation is above target, the central bank will set a higher interest rate relative to the natural rate to reduce output till inflation is back at target.

$$ r = r^\ast + h(\pi-\pi^\ast) $$

As with the IS-LM model, we endogenise $r$ in this IS-MP model to produce an AD curve. It is clear that this will slope downwards in $\{ Y,\pi \}$ space rather than the usual $\{ Y,P \}$ space.

$$ Y = E(Y) - bh(\pi-\pi^\ast) $$

**The Monetarist Explanation**

Finally, the monetarist explanation focuses on the equation of exchange, which says that the volume of nominal expenditure equals the amount of money in the economy $M$ multiplied by the velocity of money $V$ i.e. number of times a piece of money is spent. Since nominal expenditure also equals the amount of output in the economy $Y$ multiplied by the price level $P$, we get the equation of exchange $MV=PY$. If we assume a fixed level of nominal expenditure $MV$, we can see that $P=\frac{MV}{Y}$ implies a downwards-sloping hyperbola in $\{Y,P\}$ space.

![MV=PY AD diagram](/assets/monetaristad.png){:width="675px"}

And so these are the three usual ways of producing some sort of AD curve. All of them implicitly combine a process of household behaviour in the goods market with central bank behaviour in the money market. For the Old Keynesian "microfoundation", this involves people and firms following certain behavioural rules given monetary policy which holds the money supply constant. For the New Keynesian "microfoundation", this involves consumers optimising given monetary policy which follows an inflation-targeting interest rate rule. For the monetarist "microfoundation", this involves people engaging in monetary exchange given monetary policy which holds nominal output constant.

#### Designing Monetary Regimes

It should be clear from the derivations that the AD curve only slopes downwards by design and not by nature. That means we can think about how differently shaped AD curves can arise from different monetary regimes. The conventional LM curve hold $M$ and $P$ constant - although the latter is necessary as a way of squeezing a dynamic model into a static representation by assuming that prices don't change, the former is less applicable nowadays because central banks do not target monetary aggregates. Regardless, this conventional approach produces an upwards-sloping LM curve - combined with the downwards-sloping IS curve, we get our previous downwards-sloping AD curve. Given an upwards-sloping SRAS curve, we get a unique equilibrium in $\{ Y,P \}$ space. At the full-employment level of output $Y^\ast$, this will be on the economy's long-run productive potential i.e. the LRAS curve.

![AD AS LRAS diagram](/assets/lrasasad.png){:width="675px"}

Now suppose that we are off $Y^\ast$ due to some sort of demand-side shock that shifts the AD curve. This means the economy will be at the intersection between the new AD curve and the SRAS curve - as wages, prices or information all adjust, the SRAS curve will shift outwards until the AD-SRAS intersection is back on the LRAS. It is clear that even without the central bank adjusting the money supply, the economy will eventually return to $Y^\ast$.

![AD shock adjustment](/assets/adshock.png){:width="675px"}

**Indeterminacy and the Length of the Short Run**

But why are we holding the money supply constant? If the level of output is what matters to people, shouldn't monetary policy try to pin that down instead of waiting for the SRAS to adjust, which may take a while? And within the IS-LM model, that means setting a fixed real interest rate. This produces a horizontal LM curve. As before, we can produce the requisite AD curve by thinking about the LM curve as $P$ changes - because the monetary policy rule is for a fixed real interest rate, it just doesn't move. As such, we get a vertical AD curve i.e. there is only one level of output accommodated at all price levels. It is clear that there is no equilibrium price level. Suppose the AD curve is to the left of the LRAS curve - if we think through the SRAS adjustment process we described before, it is clear that it will keep shifting downwards until it intersects AD at a price level of 0. Meanwhile, if the AD curve is to the right of the LRAS curve, the SRAS will keep shifting upwards and the price level will be infinite.

![Vertical AD adjustment](/assets/verticalad.png){:width="675px"}

 Notice this is exactly what Milton Friedman said in his 1968 [*The Role of Monetary Policy*](https://www.jstor.org/stable/1831652) i.e. monetary policy "cannot peg interest rates for more than very limited periods". Even when $r$ is set so that the AD curve perfectly coincides with the LRAS curve, the price level will be indeterminate. And in a general sense, this approach of trying to target real output is a bit problematic, because it is impossible to get it exactly correct in reality.

Let's add another twist to our IS-LM model. Consider the demand for liquidity - we have talked about the transactions motive i.e. when there's more output you want more money to buy stuff, as well as the opportunity cost motive i.e. when there's a higher nominal interest rate, the interest foregone on holding money is greater. But what happens when the nominal interest rate reaches zero? In that case, holding money strictly dominates holding financial assets and the LM curve becomes flat. What does this mean for the AD curve? As $P$ falls and the LM curve gets pushed outwards, it continues to intersect the IS curve at the same point - in other words, we are left in a liquidity trap. That means the AD curve turns vertical and we run into the problem as before.

![IS-LM at ZLB](/assets/islmatzlb.png){:width="675px"}

But in fact, we can get an even worse outcome than a vertical AD curve. Suppose we revisit the way in which we produced the IS-LM, where we sneakily equivocated $i$ and $r$. If we reintroduce this wedge between the two, we realise that we need to worry about inflation expectations. And when $P$ falls, there is deflation - this raises the real interest rate $r=i-\pi$, causing the IS curve to shift inwards because of less investment. If we are already at the zero lower bound of interest rates, this means that a falling $P$ can actually result in falling $Y$. In other words, the AD curve slopes the wrong way entirely. And when drawn with the AS curves, we see that the SRAS falling as prices adjust downwards actually reduces output. (Of course, you should also notice that as soon as we introduce inflation, it might be possible to use monetary policy to leave the liquidity trap even when the nominal interest rate is at 0, because inflation expectations will shift the IS curve.)

![Debt deflation IS-LM into AD-AS](/assets/debtislmad.png){:width="675px"}

Hopefully these two cases have disabused you of the notion that economies are necessarily self-equilibrating. They aren't. Instead, the question of whether we get to $Y^\ast$ is a question of the monetary regime, and it is perfectly possible to draw up a world in which we never get there. And perhaps even more importantly, it should be clear from the second case in particular that the short run doesn't just mean when prices adjust. In fact, the short run can last forever, even as prices adjust.

**Build Back Better**

So what do better monetary regimes look like? Following the stagflation of the 1970s where central banks basically pushed output beyond the LRAS and caused the rise in the price level we predicted in our first case, they decided to adopt a new monetary regime of targeting inflation. We can look at a similar target with IS-LM, which is of targeting the price level. In that case, the AD curve will be horizontal. Or we could target nominal output, in which case we have a rectangular hyperbola for an AD curve, as we saw at the very beginning with the monetarist version.

![Price level and nGDP targeting AD](/assets/pricengdptarget.png){:width="675px"}

So which is better? It is immediately obvious that we are indifferent between the two if we face an adverse demand-side shock, because the central bank will respond in both cases by expansionary policy till we are back where the AD curve intersects the SRAS curve on the LRAS curve. Instead we can consider an adverse supply-side shock which shifts the LRAS and SRAS curves inwards by the same amount. Insofar as we want to stay on the LRAS curve, price level targeting is superior. Now suppose it is an adverse supply-side shock which only moves the SRAS inwards but leaves the LRAS where it is i.e. it doesn't affect the long-run full-employment level of output, but does affect the economy's potential in the short run due to some sort of price rigidity. Price level targeting is worse, because it forces the entire burden of this shock to be placed on output instead of on the price level.

It seems plausible that most shocks come from shocks onto the rigid relative prices of the SRAS rather than real business cycle-theoretic LRAS shocks. In that case, the divine coincidence that stabilising prices stabilises output as well doesn't hold, because the LRAS and SRAS move by different amounts. This is corroborated by [Blanchard and Gali (2007)](https://www.jstor.org/stable/4123055), who find that real rigidities render this divine coincidence moot. So this is a reason for believing in nominal output targeting might be nice! Or at least flexible inflation targeting where output and inflation both count.

At this point you might be wondering the following: "Sure, flexible inflation targeting seems great. And most central practice follow some sort of Taylor Rule i.e. they weigh both prices and output, so this broadly tracks reality. But central banks do actually conduct monetary policy by setting an interest rate, even if their broader target isn't that - so why did you say it was impossible earlier?"

Here the distinction of time period matters - it is true that it is impossible to set real interest rates at a certain level forever. But it is perfectly possible to do so for a short interval and keep on moving it around, which is what central banks do. To better understand central banks in real life, it is helpful to move to $\{ Y,\pi \}$ space, because it's a bit awkward to keep talking about price levels when central banks look at inflation. Given a certain nominal interest rate, a rise in inflation means the real interest rate is lower and output is higher i.e. we have an upwards-sloping AD curve. This intersects with the LRAS, which we shall call the Long Run Phillips Curve for reasons of convention when discussing inflation instead of the price level. So we have an equilibrium - but it is an unstable one, because if we are above the equilibrium, the excess demand for goods means prices will rise even further, resulting in more inflation. This is why the Taylor principle exists, and it says that central banks should raise the interest rate by more than one-for-one when inflation increases to ensure stability.

![Indeterminacy in output inflation space](/assets/oldindetinpi.png){:width="675px"}

#### The Neomonetarists Strike Back

Ignoring this aside, so far everything is fine and dandy. We've managed to go from a few nice stories about the supply side and the demand side into a well-behaved model with an upwards-sloping SRAS curve and a downwards-sloping AD curve in either $\{ Y,P \}$ space or in $\{ Y,\pi \}$ space. There is a unique and stable equilibrium the economy converges to if central banks do their jobs. And we've alluded to why central banks might act the way they do, targeting inflation flexibly and following the Taylor principle. The world is good. Let's see if we can mess it up again. To do so, we need to reconsider the IS curve, which has remained unscathed so far due to our focus on the money market side of things.

For one, does the IS curve actually slope downwards? If we think back to our version of the IS curve $r = - \frac{(1-c)Y}{b} + \frac{\bar{G}}{b}$, we can look at its slope by differentiating with respect to $Y$. Normally, we suppose that because $0<c<1$ and $b>0$, we have a downwards-sloping IS curve based on the derivative below.

$$ \frac{dr}{dY} = -\frac{1-c}{b} $$

However, consider the following story. Firms invest in capital based on the marginal revenue product of capital i.e. the amount of extra revenue an additional piece of capital provides. In a recession, it is either the case that labour or capital are unemployed. If labour is unemployed, this means the capital-to-labour ratio for any given firm is higher than usual. This means it will want to have a lower capital stock - in other words, it won't want to invest much. If capital is unemployed, this means that the MRP of capital must be 0 - otherwise the marginal unit of capital would be used as opposed to lying there unused. Again, the firm won't want to invest much. Empirically, the level of investment is indeed very pro-cyclical. In either case, there is a lower demand for capital at a lower level of output - this means people save instead of investing, resulting in a lower real interest rate.

And this is why it is important that we sketch out our "microfoundations" for the IS curve. If we now flesh out our functional form by recognising that investment depends positively on output, we can take $c$ not as the marginal propensity to consume an extra unit of output, but as the marginal propensity to consume plus the marginal propensity to invest given an extra unit of output. But how can this combined number be greater than 1?

Consider what happens when a change in output means the desired capital stock is above the current level. The desired investment would be infinitely large if there were no costs of adjustment. Now in reality there are these costs, but it is therefore nonetheless plausible we have $c>1$ and an upwards-sloping IS curve. To be clear, this doesn't mean that a rise in the interest rate causes output to rise - I'm not a neo-Fisherite after all. Rather, it means that a rise in output causes a greater rise in desired investment than desired savings, hence increasing the interest rate needed to equilibrate the two. Alternatively, we could describe a rise in the interest rate, not as resulting in a slightly lower level of output consistent with a downwards-sloping IS curve, but as causing output to keep falling i.e. there isn't a lower level of output that is consistent with the higher interest rate remaining higher.

This shouldn't be that implausible if we think back to our story earlier about pegging the real interest rate. If we set the real interest rate above its natural level, the immediate effect is to reduce output as per the downwards-sloping IS curve. But notice that this lower level of output is consistent with a lower real interest rate, not the higher one we induced. So it is impossible to keep the real interest rate at that higher level perpetually without getting ever increasing deflation and ever falling output, as we pointed out earlier. Now you might think that the conventional IS curve is focusing on the short-run liquidity effects of a fall in interest rates i.e. the fact that to lower interest rates you have to increase the money supply, and this is associated with a higher level of output at a lower interest rate. By contrast, this upwards-sloping IS curve seems to be looking at a slightly longer run, where the increased money supply leads to income and inflation effects i.e. this monetary growth will lead to more spending, raising output and inflation and therefore the equilibrium interest rate. But insofar as investment doesn't respond immediately to changes in the interest rate anyways and insofar as the effects of the latter dominate over time, there's a plausible case for an upwards-sloping IS curve. And it isn't just me - economists like [Miles Kimball](https://blog.supplysideliberal.com/post/56311827170/the-medium-run-natural-interest-rate-and-the), [Nick Rowe](https://worthwhile.typepad.com/worthwhile_canadian_initi/2011/08/the-macroeconomics-of-double-pole-dancing.html), [Tom Sargent](https://conservancy.umn.edu/bitstream/handle/11299/54808/1975-56.pdf), [James Tobin](https://www.jstor.org/stable/1827046), [William Silber](https://www.jstor.org/stable/2326084), [Paul Burrows](https://www.jstor.org/stable/2978602), [Earl Thompson](http://www.econ.ucla.edu/workingpapers/wp091.pdf) have all argued for this too.

Now for those who have been paying attention, you may notice that this is very screwy for the Keynesian Cross "microfoundation" of the IS curve. Previously, we had an equilibrium level of output which the model converged to, because $A$ was steeper than $E$. But with $c>1$, the slope of planned expenditure would be steeper than the slope of actual output. If actual output is greater than planned, firms will reduce output and it will keep diverging away i.e. this creates an unstable equilibrium - but that doesn't make this wrong. After all, we saw these exact unstable disequilibrium dynamics coming out earlier and necessitating the Taylor principle.

#### Parsimonious Models

In many ways, this post is a mea culpa for me having been too dismissive of IS-LM as a tool in the past. Macroeconomics is itself quite difficult, because even in the simplest business cycle models we are interested in all sorts of things: output, consumption, investment, the real interest rate, the nominal interest rate, prices, the money supply and inflation. Squeezing all of this into a static model is nigh impossible. Although I do think the canonical IS-LM model can be a bit deceptive with respect to interest rates, the idea of reconciling the goods and money markets is a useful approach. And by putting the IS-LM model through its paces, we've already illustrated some important ideas:

1. That the short run is a monetary question and not one of price adjustment
2. That there can be indeterminacy or unstable equilibria with bad monetary regimes
3. That liquidity traps and debt deflation can cause problems, but liquidity traps are really expectations traps
4. That there are good reasons for the Taylor rule and the Taylor principle

But perhaps the most important insight out of all of this is in getting the KE-MP model as proposed by Miles Kimball (where he calls his IS curve KE and his LM curve MP). We have an upwards-sloping IS curve for the previously specified reasons regarding capital and investment - there's a risk-adjusted version to reflect the risk inherent in any investment, but especially when output in the economy is less. We have an LM curve which represents the central bank setting interest rates via the Taylor principle i.e. it is steeper than the IS curve because it has to adjust by more than one-for-one. And unlike before when we assumed prices were static, we allow inflation to occur i.e. the LM curve flattens out at $r=-\pi$, because the zero lower bound binds on the nominal rather than real interest rate.

![KE-MP model](/assets/kempmodel.png){:width="675px"}

From this point on we will only look at the risk-adjusted version. There are two points of note: the natural equilibrium level of output $Y_n$, the unstable equilibrium $Y_u$ and the depression equilibrium $Y_d$. Most adverse shocks on the IS curve will put output between $Y_n$ and $Y_u$. The central bank will set their interest rate below the interest rate consistent with that level of output, causing output and the interest rate to rise back to $Y_n$. And the converse happens if output is a bit higher. So this is a locally stable equilibrium. But if there is a seismic collapse of the IS curve (perhaps due to increased financial frictions raising risk), the IS curve may fall so far as to be entirely below the LM curve. The problem is that if this is not ameliorated quickly, output will fall below $Y_u$. In that case, the zero lower bound binds on the central bank. As such, it is forced to set the real interest rate above the equilibrium interest rate at that level of output, causing output to fall further. Of course, there is a point $Y_d$ when this stops i.e. when the only output comes via consumption and government spending which is interest insensitive. Even if the IS curve is eventually brought back up, the economy will remain at this depression equilibrium. In this circumstance, conventional monetary policy is ineffective unless we manage to eliminate the zero lower bound. Absent that, one option might be to engage in unconventional policy which raises inflation expectations, pushing the IS curve up sufficiently that $Y_u$ is to the left of the current level of output. Another option would be to shift output mechanically past $Y_u$ via fiscal policy. In practice, we saw attempts at both of these after major crises, such as the Great Recession.

![KE-MP model in 2008](/assets/kemp2008.png){:width="675px"}

So at the very least this model can do the trick for the analysis we've discussed previously with traditional IS-LM, such as by illustrating the role of financial stress and liquidity traps. But more crucially, this model avoids two misconceptions IS-LM does not.

1. The downwards-sloping IS curve means we can easily make the mistake of associating low interest rates with representing easy money. But as Milton Friedman and Scott Sumner have constantly espoused: "low interest rates are generally a sign that money has been tight". The upwards-sloping IS curve is a helpful reminder that the income and inflation effects dominate in equilibrium.
2. The downwards-sloping IS curve means we have no clue how to parse what neo-Fisherites mean when they say that higher interest rates will raise inflation and output. With the upwards-sloping IS curve, it is clear where the confusion lies i.e. it becomes clear that they are thinking about a possible equilibrium, but it is also apparent that the disequilibrium dynamics just don't get us there. This insight is useful, because it means neo-Fisherism can be acknowledged for what they is: a quirk of equilibrium selection in New Keynesian models via perfect foresight. Furthermore, it is helpful as a reminder not to reason from a price change i.e. I have no idea what is meant by "raising interest rates". You can raise interest rates in the short run by tightening monetary policy, but the equilibrium level would end up lower. Or you can get higher interest rates by monetary expansion.

And so after all of this, we get a reasonably nice parsimonious model of short-run macro!
