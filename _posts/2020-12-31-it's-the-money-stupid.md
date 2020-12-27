---
layout: post
title: "It's the Money, Stupid"
date: 2020-12-31
tags: economics effortposts
---

To end the year, I wanted to examine the mental model by which I think about short-run macroeconomics. With the academic literature, a common approach in macroeconomics involves setting out microfoundations for various actors and solving their optimisation problems. This produces a set of aggregate relationships that describe some sort of dynamic stochastic general equilibrium model. But it would be a tedious and cumbersome process to solve the full intertemporal-maximisation problem every time we wanted to discuss a policy issue.

Consequently, it is no surprise that we often see ad hoc models which assume the aggregate relationships being used instead. Although this is ostensibly worse due to the lack of internal consistency, there are good reasons to believe that having these parsimonious models which contain the essential constraints and incentives is nonetheless useful.

1. Insofar as our microfoundations are imperfect, the size of errors from bad microfoundations may exceed the size of errors from failing the Lucas critique.
2. Given we do not know what the "true microfoundations" are, it may help to rely on aggregate relationships that are robust to heterogeneous microfoundations.
3. Microfoundations are themselves metaphors for endowments, preferences and technologies. They don't represent some higher order of truth simply because they involve optimisation.
4. It's not clear that people's tastes are invariant to policy, so microfoundations may themselves not be immune to the Lucas critique.
5. Since we have no grand unifying model right now, ad hoc models can provide a good sketch of the pertinent static properties.

So what ad hoc model should we use as a convenient scratchpad for thinking about macroeconomic phenomena? To figure this out, we need to understand what such a model would need to be able to account for. Since that is quite difficult to do in abstract, let's start with some commonly used ones.

**Old Keynesian IS-LM**

The classic choice of an ad hoc model is the Old Keynesian IS-LM model. The IS-LM model is a two-equation model in the output-interest rate space, made popular by Sir John Hicks's *Mr. Keynes and the Classics*. As David Romer describes in his Advanced Macroeconomics textbook (1996 edition), the IS-LM model can be produced by considering the market for goods and the market for money.

Consider the condition for equilibrium in the goods market. Suppose we have the output of goods as $Y$. We can look at the components of demand in the closed economy as consumption, investment and government spending. The amount people want to consume $C(Y-T)$ is an increasing function of their real disposible income, with people wanting to consume more when they earn more. The amount of firms want to invest $I(r)$ is a decreasing function of the real interest rate, where firms want to invest more when borrowing is cheap. Government spending is given exogenously as $G$. For the equilibrium to hold, we must have production equalling sales at $Y=C(Y-T)+I(r)+G$. The IS curve represents the output-interest combinations where the goods market clears.

Now let's look at equilibrium in the money market. The supply of real money balances is the nominal money supply divided by the price level as $\frac{M}{P}$. The demand for real money balances is affected by the need for liquidity and the returns foregone by holding money in lieu of interest-bearing assets. With higher real incomes, there is a greater desire for transactions and liquidity. With higher nominal interest rates, there is a larger opportunity cost to holding money. As such, it is an increasing function of real income and a decreasing function of the nominal interest rate as $L(Y,i)$. This means an equilibrium condition of $\frac{M}{P}=L(Y,i)$. The LM curve shows the output-interest combinations where the money market clears at a given price level.

Insofar as this is a static model with fixed inflationary expectations i.e. $\pi^e=0$, the nominal and real interest rates are same by the Fisher equation of $i=r+\pi$. As such, we can plot the IS and LM curves on the output-interest rate plane. They intersect at the combination of output and interest rate which clears both markets for a given price level.

![ISLM](/assets/ISLM.png){:width="675px"}

If we adjust the price level, we will be shifting the LM curve. The locus of points formed by the intersection of the IS curve and the various LM curves represents the combinations of output and price level where goods and money are both in equilibrium - in other words, the aggregate demand curve.

![ISLM to AD](/assets/ISLMAD.png){:width="675px"}

Let's specify some functional forms for our IS and LM curves. Take consumption as $C=c_0+c_y(Y-T)$, investment as $I=d_0+d_r r$ and money demand as $L= L_y Y - L_r r$. All we've added are autonomous components and coefficients. We get the following.

$$ \text{IS curve}: Y = \frac{c_0+d_0}{1-c_y} - \frac{d_r}{1-c_y} r + \frac{1}{1-c_y}G - \frac{c_y}{1-c_y} T $$
$$ \text{LM curve}: \frac{M}{P} = L_y Y - L_r r$$

These are very messy equations. Let's simplify this in a few ways as [u/Integralds does](https://old.reddit.com/r/badeconomics/comments/43i631/badeconomics_discussion_thread_31_january_2016/czjbqkm/). The key takeaway from the IS curve is that real output (and consequently log real output $y$) depends positively on some fiscal variable and negatively on the real interest rate - we can write it as $y=g-br$. The key takeaway from the LM curve is that real money balances (and consequently log real money balances $m-p$) depends positively on real output (and log real output) as well as negatively on the real interest rate - we can write it as $m-p=y-hr$, assuming that money demand is unit elastic to real income.

By eliminating the interest rate, we can get the aggregate demand curve. We can see that it is downwards sloping in the output-price level space.

$$ \text{AD curve}: y = \frac{h}{b+h}g + \frac{b}{b+h} (m-p)$$

**Adding the AS curve**

[George Akerlof describes](https://eml.berkeley.edu/~webfac/akerlof/e202_f07/lecture1.pdf) the three important questions of macroeconomics in the short run as the level of output, interest rates and prices, as well as how these are affected by the environment, fiscal policy and monetary policy. Unfortunately, an AD curve isn't enough to answer these questions, because its IS-LM foundations assume a fixed price level. We need to close out the model with a way of describing the aggregate supply of goods.

This can be done in a few ways. The traditional Keynesian approach is to have a production function of $Y=F(N)$, where $N$ is the level of employment. Money wages are set at $\bar{w}$. The production function exhibits a positive marginal product with $F'(N)>0$ and a diminishing marginal product with $F''(N)<0$. Employers will hire up till the point where the marginal product of labour equals the real wage, where $F'(N)=\frac{\bar{w}}{P}$. Hence there is some aggregate supply function $Y=Y(P,\bar{w})$. One simplified functional form for this could be $p = \bar{w} + ay$.

The result of having three equations in three variables is that we can look at the following matrix of comparative static outcomes, seeing how changes in the fiscal variable, monetary variable or wages affect output, interest rates and prices.

$$\begin{bmatrix} \frac{dy}{dg} & \frac{dy}{dm} & \frac{dy}{d\bar{w}} \\ \frac{dr}{dg} & \frac{dr}{dm} & \frac{dr}{d\bar{w}} \\ \frac{dp}{dg} & \frac{dp}{dm} & \frac{dp}{d\bar{w}} \end{bmatrix}$$

**IS-LM-AS as the Benchmark Model**

Why has IS-LM-AS been treated for such a long time as a useful first-pass way of thinking about short-run macroeconomics? After all, it remains in many intermediate textbooks to this day, over 80 years after Hicks first wrote about it.

The reason Akerlof gives for saying that "if [he] were to know one thing about macroeconomics, what [he] would want to know would be the Keynesian model" is because if you look at the "signs you get out of the Keynesian model, every one of the nine comparative static results makes intuitive sense".

The idea that it produces illustrative predictions is reiterated by [Mark Thoma](https://economistsview.typepad.com/economistsview/2009/09/who-has-all-the-answers.html), who notes that when it comes to significant fluctuations in the business cycle, the Old Keynesian model is the one designed to answer those questions. By contrast, the quantity theory is more suited for understanding inflation in the long run and the basic New Keynesian model as it stands for small business cycle fluctuations.

Indeed, [Paul Krugman](https://krugman.blogs.nytimes.com/2010/09/11/one-model-to-rule-them-all/), who is one of the biggest advocates for IS-LM, argues that the framework allowed him to make accurate predictions during the Great Recession.

[Krugman notes](https://krugman.blogs.nytimes.com/2011/10/09/is-lmentary/) that IS-LM is especially helpful in considering liquidity traps, which he believes characterised the Great Recession. Consider the LM curve - once interest rates hit zero, people would choose to hold money in lieu of interest-bearing assets, since there would be no interest foregone. As such, conventional monetary policy which changes the money supply via open market operations that swap money for bonds will have no effect. It is only fiscal policy that can have an effect by shifting the IS curve to the right.

![Liquidity Trap](/assets/ISLMTrap.png){:width="675px"}

This led [Krugman to suggest](https://krugman.blogs.nytimes.com/2014/03/28/what-i-mean-when-i-talk-about-is-lm-wonkish/) that "big deficits and huge increases in the monetary base would lead neither to soaring interest rates nor to soaring inflation".

[Krugman observes](https://krugman.blogs.nytimes.com/2009/01/27/a-dark-age-of-macroeconomics-wonkish) that it also prevents one from "interpreting an accounting identity as a behavioural relationship". This sort of fallacious reasoning leads one to believe that any government borrowing must come at the expense of investment since savings equal investment, making any fiscal policy irrelevant. This is silly, because it ignores how the two re-equilibrate, which IS-LM highlights is the change in output.

And finally, [Krugman thinks](https://krugman.blogs.nytimes.com/2013/03/19/misunderstanding-is-lm-wonkish-and-unimportant) that IS-LM conveys the essential insight that "both liquidity preference and loanable funds are true" at the same time, because there are two adjusting variables of interest rate and income. That is, it shows how things work in general equilibrium when there is both the goods and money market.

But there's a more fundamental reason for liking IS-LM, which relates to the premise of this post i.e. what you need to understand short-run macroeconomics. [Krugman posits](https://krugman.blogs.nytimes.com/2011/10/05/tis-the-gift-to-be-simple/) that at minimum, we need to have "money, bonds and economic output". How can we represent this?

Consider a three good economy of $X$,$Y$ and $Z$, where $Z$ is the numeraire. We can plot the combinations of prices for each of the markets to be in equilibrium, assuming negative own-price effects and positive cross-price effects.

![Three Goods](/assets/ThreeGoods.png){:width="675px"}

If we treat goods, bonds and money as $X$,$Y$ and $Z$ and change the vertical axis to the interest rate instead of the price of bonds, we can see Don Patinkin's full employment IS-LM from *Money, Interest and Prices*. If we add price stickiness, we get the IS-LM we've been discussing.

![Patinkin](/assets/Patinkin.png){:width="675px"}

As such, [Krugman argues](http://web.mit.edu/krugman/www/islm.html) that IS-LM is far from arbitrary - instead, it is the logical consequence of setting up a general equilibrium framework to examine short-run macroeconomics.

[Krugman acknowledges](https://krugman.blogs.nytimes.com/2011/09/13/how-much-hoc-to-add-wonkish-and-methodological/) that IS-LM tries to squeeze a dynamic economy into a static model, bypassing the fact that decisions are dependent on expectations by setting fixed prices. But insofar as the alternative is rational expectations which are themselves untrue, IS-LM can be seen as a useful first pass way of producing good static predictions that can then be checked against an intertemporal New Keynesian model.

[Brad DeLong](https://delong.typepad.com/sdj/2011/10/the-tribal-dislike-of-john-hicks-and-is-lm-history-of-economic-thought-edition.html) adds that a good approach in economics is to "start with the simplest possible model" and complicate it when you run into the constraints of its explanatory power. He argues that "the one-good one-period model simply has output: that is not terribly useful". The two-good one-period mechanical quantity theory model with output and money "struggles from the fact that the money stock is very large, but the flow of spending is not". Hence the need for the three-good one-period IS-LM model with money, output, and bonds. Indeed, [DeLong emphasises](https://www.bradford-delong.com/2009/04/is-lm.html) that basically any theory of nominal spending or real output determination will have an IS-LM representation.

**Contra IS-LM-AS**

On the surface, this seems like a strong case for using IS-LM-AS as a way of understanding the macroeconomic world. And yet there are many who do not see it as sufficient, even as a minimalist model. There are generally three sorts of critiques against it. The first relates to the curves themselves and their formulation. The second focuses on the structure of the model as a whole and how the curves come together. The third represents a more fundamental disagreement about what is needed in a stripped down macroeconomic model.

**Updating the Three Curves**

One prominent criticism of the three curves comes from [David Romer](https://eml.berkeley.edu//~dromer/papers/JEP_Spring00.pdf), who seeks to replace the LM curve with a Monetary Policy curve. For any particular LM curve, the money supply is held constant, implicitly suggesting that the central bank is targeting the money supply. In reality, modern central banks do not target such monetary aggregates - as such, Romer introduces the MP curve which focuses on a real interest rate rule.

The rule is based on the real interest rate, because central banks are ultimately interested in that, using nominal interest rates and price stickiness to get there. Helpfully, this deals with one issue that IS-LM faces, which is that investment-savings decisions depend on the real interest rate while liquidity-money decisions depend on the nominal interest rate. By contrast, this ensures that we have a consistent choice of interest rate throughout the model.

Certainly, it is important to understand how the central bank controls the real rate, and whether the occurs via the money market or interest on reserves. But that can be done later - for the purposes of a basic analysis, leaving that in the background and looking at monetary policy directly can be far clearer. As such, we have the MP curve as a horizontal line in the output-real interest rate space, since it is just an interest rate being set. The simplest monetary policy rule is one where the real interest rate is an increasing function of inflation, in the form $r=r(\pi)$.

![IS-MP](/assets/ISMP.png){:width="675px"}

An increase in inflation will lead to a shift upwards in the MP curve. As such, the locus of points formed by the intersection of the IS curve and the various MP curves will be a downwards-sloping AD curve as before. Furthermore, the basic AD curve produced previously looks at output and the price level. But most of the time, what we are interested in is the relationship between output and inflation, which this AD curve shows.

![IS-MP into AD](/assets/ISMPAD.png){:width="675px"}

Another advantage of the MP curve is clarity regarding the measure of money. The LM curve's liquidity preference suggests $M$ is a measure of high-powered money i.e. the monetary base. But the LM curve also assumes that the broader money supply $M$ is fixed, and central banks abundantly do not treat these two as equivalent, since the latter measure of the money stock is much less controllable by the central bank. By contrast, the MP curve makes it clear we are only referring to high-powered money, since it is merely a tool the central bank is using to affect interest rates. This provides consistency.

This line of argument has been echoed by [Matt Rognlie](http://mattrognlie.com/2011/10/07/why-is-lm-still-there/), who sees the LM curve as "describing a monetary policy rule that disappeared decades ago", as well as [Karl Smith](http://modeledbehavior.wordpress.com/2011/10/04/on-is-lm/), who thinks that macroeconomic discussions "should be piped through the language of monetary policy".

However, [Greg Mankiw](https://gregmankiw.blogspot.com/2006/05/is-lm-model.html) has come to IS-LM's defence, arguing that there's "no substantive difference between IS-LM and IS-MP". We can see this by rearranging the simplified LM curve from before to produce $r=\frac{p+y-m}{h}$. Notice that this is a monetary policy rule where the interest rate is set much like a Taylor rule. The only distinction is that IS-LM takes the money supply as exogenous, while IS-MP takes the monetary policy rule as exogenous. Insofar as both change in real life, exogeneity is "more of a thought experiment than it is a claim about the world", and as [Nick Rowe](https://worthwhile.typepad.com/worthwhile_canadian_initi/2013/08/is-money-exogenous-or-endogenous.html) points out, simply depends on what we are interested in.

[DeLong adds](https://delong.typepad.com/sdj/2011/10/why-lm-is-still-here.html) that even though central banks target an interest rate, monetary policy decisions still consist of making "a discrete quantitative change in the monetary base". Insofar as that is the case, it remains prudent to keep the role of the money supply front and centre.

However, the fact that the Federal Reserve now pays interest on reserves means that this quantity-theoretic approach may not be as illustrative as before, where the mechanism for controlling the interest rate was open market operations. [Smith concurs](http://modeledbehavior.wordpress.com/2011/10/07/interest-on-currency/), noting that now, "the interest rate paid on reserves and not the quantity of reserves or the dynamics of the overnight lending market" are determinate in monetary policy. Indeed, [Rowe says](https://worthwhile.typepad.com/worthwhile_canadian_initi/2015/12/questions-for-moneymacro-historians-of-thought.html) that it makes little sense to think of central banks "doing nothing" as $M$ being held constant. Combined with the many other benefits of the MP curve, it seems like a better tool for analysis - however, the process of controlling interest rates via changing the money supply a la LM ought to be remembered in the background.

Beyond the MP curve, [Smith also has](https://modeledbehavior.wordpress.com/2011/10/08/the-bl-mp-model/) a different approach for the IS curve. Instead of thinking about the investment-savings decision in the goods market in abstract, he hones in on the role of bank lending as the intermediation process. Of course, the underlying dynamics are the same - but this simply chooses to focus our attention differently.

This BL curve is especially helpful in understanding [financial crises like 2008](https://modeledbehavior.wordpress.com/2011/10/09/whats-the-minimum-needed-to-make-a-macroeconomic-model/) compared to the IS curve, because it looks at "goods, money and banks" instead of goods, money and bonds. It allows us to incorporate bank balance sheets and lending risks, by placing banks as "the gatekeepers of aggregate demand". And it [helpfully illustrates](https://modeledbehavior.wordpress.com/2011/10/08/more-on-bl-mp/) how government borrowing and raising inflation expectations can both lower the average risk of lending. Indeed, if we plot the BL curve with the MP curve, we can see the way in which liquidity traps occur due to "no worthwhile lending opportunities".

![BLMP Trap](/assets/BLMPTrap.png){:width="675px"}

And finally, if our aggregate demand curve produces a relationship between output and inflation, we ought to update our aggregate supply curve to do the same. One way of doing so is by considering inflation as a combination of some level of inflation that always exists and a function of the gap between actual output and NAIRU output. This can be written as $\pi = \bar{\pi}+\lambda(Y-\bar{Y})$.

**Old and New Keynesian Dynamics**
A second line of criticism for IS-LM-AS is that it is a static and ad hoc model. According to [Tyler Cowen](https://marginalrevolution.com/marginalrevolution/2011/10/why-i-do-not-like-the-is-lm-model.html), "you should hear a clock start ticking in your head" every time you use the model. The longer it ticks, the more you have to be concerned with prices and inflation expectations changing, driving a wedge between the nominal and the real.

This is especially an issue as [Cowen notes](https://marginalrevolution.com/marginalrevolution/2005/10/five_reasons_wh.html), because investment and savings decisions occur on the basis of the full future path of interest rates, while money market decisions are affected by the short-run interest rate. So the model fudges the distinction over the time period too.

By updating into the MP curve as we have above, we no longer obscure the distinction between nominal and real interest rates as [Simon Wren-Lewis](https://mainlymacro.blogspot.com/2012/02/why-introductory-macroeconomics-should.html) dislikes, but expectations remain absent. [Chris Sims](http://sims.princeton.edu/yftp/Bergamo/Bergamo.pdf) argues that the lack of expectations is seriously damaging for a model in the Keynesian tradition.

A corollary to this criticism is that these models fundamentally don't come from the sort of intertemporal optimisation that characterises modern macroeconomics, hence why they rely on ad hoc relationships which do not include expectations of the future. The consequence of not having people within the model is that there is no sense of where relationships come from, merely stories being told regarding how different macroeconomic variables might relate to each other.

This is problematic on a pedagogical level, insofar as it doesn't teach modelling skills, but it also undermines the validity of the model itself. Of course, as I outlined at the beginning, microfounded models aren't the be-all and end-all, so this doesn't disqualify these models. But what if we could produce a simple and tractable three equation model like IS-LM-AS, except they were based on microfoundations?

This is the New Keynesian 3 equation model of [Richard Clarida, Jordi Gali and Mark Gertler](https://www.aeaweb.org/articles?id=10.1257/jel.37.4.1661), which is gestured at in the textbooks of Charles Jones as well as David Carlin and Wendy Soskice.

Suppose we have deviations from potential output as $x_t=Y_t-\bar{Y}_t$. The New Keynesian IS curve relates this output gap to the expected future output gap, the deviation of the real interest rate from its natural level and a stochastic parameter.

$$ x_t = E_t x_{t+1} - \phi \tilde{r}_t + g_t $$

The New Keynesian Philips Curve is simply an expectations-augmented version of our previous AS curve with a stochastic parameter.

$$ \pi_t = \beta E_t \pi_{t+1} + \lambda x_t + u_t $$

And for the MP curve, we have a Taylor rule where the interest rate is set based on the deviation of inflation from target and output from its potential.

$$ r^{ff}_t = \gamma_\pi (\pi_t-\pi^T_t) + \gamma_{x} x_t $$

Thus we have our New Keynesian three equation IS-MP-PC model, which is derived from microfoundations. We can even add a wedge between the interest rate set by the central bank and the interest rate in the IS curve by having $r_t=r^{ff}_t+\bar{f}$, where $\bar{f}$ represents some exogenous risk premium that allows us to include the financial sector in this model with ease.

And by the same process as before, we get an AD curve from IS-MP and an AS curve by taking the New Keynesian Philips Curve, giving us a dynamic AD-AS model relating output and inflation that is easily accessible.

**Barter and Monetary Exchange**
It seems like all of our approaches have resulted in us using an AD-AS model eventually. But if that's the case, do we need to go through a 3 equation model every time?

[Scott Sumner](https://www.themoneyillusion.com/krugman-and-delong-mount-a-chivalrous-defense-of-is-lm/) thinks otherwise - in fact, he disagrees on the need for a minimal macroeconomic model to have "money, bonds and output". Consider a quantity theory model, which contrary to DeLong's earlier criticism, does not have to be the mechanical one with constant money velocity.

Suppose we have "a model with money and goods, plus sticky prices". The supply and demand for money sets the price level and nGDP. If we have sticky prices in the form of a Philips Curve, we can translate nGDP shocks into the components of real GDP fluctuations and price fluctuations, creating demand-side business cycles.

It's not entirely clear what interest rates add to this story. [Sumner notes](https://www.themoneyillusion.com/why-i-dont-like-is-lm-reply-to-delong/) that a doubling of the money supply ought to double the price level - the fact that this doesn't occur immediately due to nominal stickiness means that the interest rate must equilibrate the doubled money supply with the not yet doubled money demand. But that means interest rates are merely an epiphenomenon of the stickiness, and not crucial in understanding macroeconomic changes.

Indeed, the focus on interest rates within IS-LM is problematic. For example, as we saw above, it suggests that monetary policy is ineffective at the lower bound. But since [Krugman (1998)](https://www.brookings.edu/wp-content/uploads/1998/06/1998b_bpea_krugman_dominquez_rogoff.pdf), we have known that this is not the case - or rather, it is true only as [Krugman describes](https://www.princeton.edu/~pkrugman/thinking.pdf) as "an expectational issue" of central banks being unable to "credibly promise to be irresponsible". [Krugman admits](http://web.mit.edu/krugman/www/japtrap.html) that the static nature of IS-LM disguises this - indeed, it focuses one's attention improperly to interest rates, which as [Sumner warns](https://www.econlib.org/archives/2016/06/which_direction.html), can lead to one reasoning from a price change i.e. thinking low interest rates must be easier monetary policy.

Meanwhile, [Rowe sees](https://worthwhile.typepad.com/worthwhile_canadian_initi/2016/06/on-olivier-blanchard-on-islm-and-teaching-intermediate-macro.html) sees money as at the center of business cycles. Consider as [Rowe does](https://worthwhile.typepad.com/worthwhile_canadian_initi/2015/12/minimalism-and-recessions.html) a one-period pure endowment general equilibrium model with no time, uncertainty, interest rates, savings, investment, borrowing, lending, production or employment. The only salient feature of this model is monetary exchange.

Suppose three consumption goods of apples, bananas and mangoes, with mangoes as the numeraire and the price of both apples and bananas as $P$. Half of the agents have 200 apples and 100 mangoes, the other half have 200 bananas and 100 mangoes. They all have preferences given by $U=\ln{C_A}+\ln{C_B}+\ln{C_M}$.

In a barter economy, there is a market-clearing competitive equilibrium of $P=1$. Everyone consumes 100 of each fruit. But suppose we have a sticky price of $P>1$ - nothing changes, because agents can just barter apples and bananas.

Now consider a monetary exchange economy, where you cannot exchange apples and bananas directly and must use mangoes as the medium of exchange. While the situation is the same when $P=1$, as soon as $P>1$ we get a disequilibrium, because there is excess apples in the apple-mango market and excess bananas in the banana-mango market. So recessions are simply reductions in utility when monetary exchanges do not occur due to an excess demand for the medium of exchange.

This is why money is crucial in understanding business cycles, and why [Rowe emphasises](https://worthwhile.typepad.com/worthwhile_canadian_initi/2017/01/adas-a-suggested-interpretation.html) the importance of making clear that we are talking about a monetary exchange economy in our models - in a sense, every market in such an economy is a goods-money market and so [Rowe describes](https://worthwhile.typepad.com/worthwhile_canadian_initi/2014/08/money-prices-and-coordination-failures.html) recessions as monetary coordination failures.

How can we demonstrate this clearly? Well, it turns out this can be done very simply - [Sumner notes](https://www.themoneyillusion.com/the-tabarrokcowen-asad-model/) that Tyler Cowen and Alex Tabarrok have done so in their introductory textbook.

Consider the equation for exchange $MV=PY$, which describes any monetary exchange economy. Cowen and Tabarrok take the dynamic form of that as their AD curve.

Recognise that the growth rate of a variable $A$ is given by $\tilde{A} = \frac{A_{t+1}-A_t}{A_t}$, or in instantaneous form, it is given by $\frac{\dot{A}}{A}$. This can be written as $\frac{d \ln{A}}{dt}$. For some $A=BC$, we can see that $\ln{A}=\ln{B}+\ln{C}$ and so $\frac{d \ln{A}}{dt}=\frac{d \ln{B}}{dt}+\frac{d \ln{C}}{dt}$. Hence we can write their growth rates as $\tilde{A} = \tilde{B} + \tilde{C}$.

This means we can see that $\pi = \tilde{M} + \tilde{V} - \tilde{Y}$. If we hold nominal GDP growth constant, we can draw a downwards sloping AD curve in the real output growth-inflation space. We can add a Long Run Aggregate Supply curve based on the growth rate with flexible prices. And we can produce a Short Run Aggregate Supply curve, based on the ideas of sticky prices and signal extraction, to explain the split between the effect on output growth and on inflation by AD shocks in the short run.

![Short Run Model](/assets/model.png){:width="675px"}

This is a parsimonious model that is easily explained and can account for what is going on. Furthermore, [Rowe argues](https://worthwhile.typepad.com/worthwhile_canadian_initi/2013/06/in-defence-of-the-as-ad-framework.html) that "when we teach economics we are not (or should not be) just teaching about the here and now" - rather, [Rowe gestures](https://worthwhile.typepad.com/worthwhile_canadian_initi/2014/06/teaching-general-principles-of-macro.html) at general principles that apply broadly. The AD curve, by virtue of not tying itself to any particular monetary rule but instead to the idea of monetary exchange, can be useful for a range of circumstances.

**The Key Components**
Ultimately, the study of business cycle macroeconomics as a field exists because of monetary exchange. If we lived in a world with a Walrasian auctioneer or a world where barter is easy, we would not see recessions. The only fluctuations we would see are purely real shocks - but these would simply to lead to immediate adjustments in prices. Instead, we do live in a world with money. As Jack Gurley put it, "money is a veil, but when the veil flutters, real output sputters".

As such, we need to have a macroeconomic model which is cognizant of this, as well as being adaptable enough to fit varying circumstances. The dynamic AD-AS model does exactly this. It is the simplest way of accounting for goods and money in a monetary exchange economy. Consequently, we should work with that as an ad hoc model, allowing us to think about how changes in the money supply and velocity occur and how they affect output and inflation.
