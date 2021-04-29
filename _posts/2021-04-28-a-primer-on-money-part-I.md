---
layout: post
title: "A Primer on Money: Part I - The Fluttering Veil"
date: 2021-04-23
tags: economics effortposts
---

This is Part I of my primer on [money in macroeconomics](https://tmychow.com/blog/2021/04/23/money-a-primer-in-five-parts). In order to begin to discuss its role, we need to understand the following four questions.

1. What is money and how does it affect the nominal world?
2. Why and how does money affect the real world?
3. What should the goal of monetary policy be in theory?
4. How is monetary policy conducted in practice?

**Money and the Nominal World**

If we want to talk about the nominal world, we need to talk about money - this is the defining feature of the monetary exchange economy in which we live. And it is because we engage in monetary exchange that money exists - instead of relying on a double coincidence of wants where two people want each other's stuff and barter, money gives us a medium of exchange to avoid that in our transactions. Usually, textbooks talk about three purposes of money: as a medium of exchange, as a unit of account and as a store of value. But the last isn't essential to money, with basically every single thing in the world storing some sort of value. To the extent to which it is a store of value, this can be understood by considering why fiat currency i.e. money that isn't backed by anything, can hold any value at all. In many ways, the reason it has value is because people expect it to have value i.e. because it is taken as a Schelling point where everyone accepts it in transactions and believe it is implicitly backed by the government. So the extent to which it holds value depends on the fact that it is used and expected to be used as a medium of exchange.

Having established what money does, what is the value of money? Slightly facetiously, the nominal value of $1 is just $1, as it says on the tin. But its real value is what you can buy with it i.e. its purchasing power. As with any other good, this value is determined by the supply and demand of money. If we think of central banks as having a monopoly over the money supply, it can set any quantity $M$. Meanwhile, people's demand for money depends on its role as the medium of exchange - if the amount of nominal output $PY$ in the economy is higher, people will want more money to buy things. Of course, people don't hold all their wealth in the form of money, because doing so means that they forgo the earnings from putting it in interest-bearing assets. So we might think that the fraction of money they're willing to hold is a decreasing function of the interest rate as $k(i)$. That means the equilibrium when the supply of money equals the demand is $M = PYk(i)$. If we think that the velocity at which people spend money is the inverse of the fraction of money they want to hold i.e. $V=\frac{1}{k(i)}$, we get the following equation of exchange.

$$ MV = PY $$

Consider what happens when there is a one-off doubling of the money supply from the central bank. Although individuals may choose the amount of money they want to hold based on the money demand described above, this clearly isn't possible in aggregate given that is controlled by the central bank. How is this resolved? When we see this doubling, the real value of the money people hold will be too much for what they want - consequently, they will get rid of the money they hold by buying things. This bids up the price level and it adjusts by doubling, until the purchasing power of money they hold is back to the level they want. In other words, people determine the real value of money they hold while the central bank determines the nominal value of money. This is the quantity theory of money, which says that the price level is directly proportional to the money supply in the long run. This is the long-run neutrality of money i.e. the money supply only affects the price level, as opposed to real variables like output.

However, consider what would happen if a central bank doubled the money supply today and promised to halve it tomorrow, as soon as inflation occurred. Would there still be the same effect on the price level? Probably not. So there is a difference between a temporary and permanent injection of money. And similarly, it seems likely that prices would rise immediately if people were told that the money supply would double tomorrow. Expectations matter. Another useful consideration is to think about what happens if the rate of money growth increases - this will lead to an increase in inflation $\pi$. Since the nominal interest rate $i$ is approximately the real interest rate $r$ plus the inflation rate $\pi$, this will raise the nominal interest rate and the velocity of money. So in this way, it is clear that a one-off rise in the money supply will raise nominal output by causing a rise in $M$, while a rise in the money growth rate will raise nominal output both via $M$ and $V$.

So this is the nominal world - here, the quantity theory and neutrality of money holds, and monetary changes affect nominal output. Yet as interesting as this is, the reason we care about money is because its changes have effects on real variables.

**Money and the Disequilibrium Sticky World**

So how does money affect the real world? To understand this, we have to go back to the reason why fluctuations from the full-employment level do not occur in the real world without money. We know from Walras's Law that if there is an excess supply of goods in one market, it must be the case that there is an excess demand for goods in another market. In a world with a perfect barter system, any deviations from equilibrium would represent opportunities for mutually beneficial trade. People would simply negotiate and trade away these inefficiencies. In other words, Say's Law would hold and supply would create its own demand.

Why does money change this? As it turns out, the introduction of money as a medium of exchange means that every market goes from being a goods-goods market to a goods-money market. And so if the money markets are out of equilibrium, the goods markets will be too. But how can the money market be out of equilibrium? This is because it is often the case that the exchange rate between money and a good is not easily changed i.e. the unit of account is sticky. So when there is suddenly an excess demand for money, the price of money would need to rise i.e. the price of everything else would need to fall. Because some prices for goods are sticky, those goods markets will go out of equilibrium - and when it is difficult to sell goods for money due to the price of goods being too high, people stop selling money for goods too i.e. the volume of trade falls. And so even a few sticky prices will result in all sorts of markets going out of whack. As Jack Gurley put it, “money is a veil, but when the veil flutters, real output sputters”.

This is best illustrated by looking at some real world examples. For example, some of the largest shocks did not produce biggest downturns, because the change in money demand was offset. The 1987 financial crisis saw the single largest one-day percentage fall in the Dow Jones Industrial Average, and yet output barely budged. The prelude to the Great Recession saw housing construction falling by half between early 2006 and mid-2008, and yet employment didn't get affected till later in 2008. By many accounts, the Treasury market in March 2020 froze up in a way that wasn't even seen during the Global Financial Crisis of 2008, and yet this never propagated into a wide scale financial crisis. And that's because in those cases, monetary policy provided speedy, substantial and sustained access to money and liquidity. By contrast, all of these pale in comparison to the size of the business cycle fluctuations during the Great Depression or the Great Recession - that's because monetary policy was not there to accommodate these shocks. So although real problems matter, they only become huge issues because of nominal problems. What does this mean for monetary policy?

**Goal of Monetary Policy in Theory**

Implicitly, we've already identified the role of monetary policy: it is to look at changes in money demand and offset it with the money supply - that is, to ensure that $M$ adjusts when $V$ fluctuates, because rapid fluctuations in $MV$ cause problems by forcing the money market (i.e. all markets) out of equilibrium. In other words, the idea is to stabilise the expected future path of nominal GDP. And this isn't terribly surprising - insofar as people make decisions about employment contracts, debt contracts and all sorts of purchases based on the expected level of nominal GDP, changes off that path can cause problems.

There are three important notes on this approach. The first is about the word "expected" - this means looking forward at forecasts, and because it's generally not a good idea given the Efficient Market Hypothesis to assume you can always outpredict the market, targeting market forecasts is particularly appealing. This has the additional advantage of reducing the "long and variable lags" associated with policy changes, since asset markets react quickly and will tell you if you're on track. The second is about the word "future" - people are to some degree forward looking, and if they expect future nGDP to fall, they will start spending less and cause current nGDP to fall. Meanwhile, if future nGDP remains on target, people have far less incentive to spend less now and so it is hard for current nGDP to fall much. As such, monetary policy should be concerned with all future levels of nGDP, not just what it is right now. The third is about the word "path" - since people's expectations of future nGDP matter, it is even better to commit to targeting a level rather than just an annual growth rate. In practice what this means is that any shortfalls in nGDP growth in a particular year are made up for in future years, rather than simply letting bygones be bygones. This commitment to correct for deviations means people have well-anchored expectations of the future level of nGDP, since a failure to hit the goal in any single year won't drag it down.

How does this compare with the status quo? In many ways, this is very similar to how many economies like the US, UK, Canada, Australia, New Zealand and Israel conduct their monetary policy right now. They have some sort of dual mandate where the central bank cares about inflation and output, they are ostensibly forward-looking and target the forecast, they place a significant premium on affecting future expectations and in the case of the US with its new regime of average inflation targeting, will make up for shortfalls. But the difference is that nGDP level targeting treats nominal GDP as one thing, whereas most central banks currently treat the components of real output and inflation separately. Inevitably, this reduces some of the flexibility central banks can have, because it forces them to only care about real output and inflation as well as treating their deviations as equally important.

But the advantage of not splitting this into a flexible dual mandate comes in several ways. Firstly, it is just a lot easier to sell a central bank's policy as one of raising nominal incomes than of raising inflation during a crisis, because many people associate the latter with a higher cost of living. Secondly, the measurement of inflation is notoriously difficult and arbitrary, whether this is in the use of hedonic adjustments or the imputing of rental equivalents for housing. It is a testament to this confusion that there are so many different price indices, not to mention different variants on each e.g. core inflation versus headline inflation, where the former excludes food and energy prices. Thirdly, inflation can be deceptive - insofar as prices change slowly, inflation will lag behind shocks to nGDP. And in fact, it may go the other way if there is a supply-side shock hitting the economy at the same time. The most obvious example of this causing a misdiagnosis is in mid-2008, when the rise in oil prices meant the Federal Reserve was too concerned about inflation and failed to arrest the fall in nGDP.

The other main disparity between nGDP level targeting and what we do right now comes down to how we measure the stance of monetary policy. In the past, economists often looked at monetary aggregates, though we now commonly look at interest rates. The danger with this is that interest rates fall for many reasons - one reason interest rates fall is due to monetary expansion i.e. a liquidity effect from an increase in the money supply. But over time, an increase in the money supply translates into more nGDP growth, raising the interest rate. So when the Fed lowered interest rates during the Great Recession, it seemed on the surface that they had an easy monetary stance. But in reality, the equilibrium interest rate had fallen even further due to low nGDP expectations, so their easing of policy still left them at an overall tight monetary stance. And although in theory a good measure would be the deviation of the interest rate from its equilibrium level, the difficulty of doing so in real time means a much better alternative is just to look at nGDP expectations, since it will be apparent if the monetary expansion is enough to offset the increased demand for money. And by doing so, we can infer the monetary stance with reference to the expected value of our policy goal and relative to our policy target. But how does this all work in practice?

**Conduct of Monetary Policy In Practice**

To understand the actual mechanisms of monetary policy, we need to look at the plumbing of how central banks operate. For the sake of simplicity, I'll only look at the Federal Reserve[^1]. We begin by considering the tools of the Fed in the pre-2008 world. Prior to the Global Financial Crisis, the main instrument of Fed policy was based on the federal funds market. This had several components which the Fed could control.

[^1]: [Ihrig, Meade and Weinbach 2015](https://pubs.aeaweb.org/doi/pdfplus/10.1257/jep.29.4.177)

1. The Fed sets reserve requirements for depository institutions i.e. certain financial institutions have to hold a certain amount of money which can't be lent out.
2. The Fed sets the discount rate, which is the interest rate at which it lends to banks who provide collateral.
3. The Fed sets the supply of reserves by engaging in open market operations.

Because banks could not earn any returns on reserves, they had an incentive to keep their reserves to the minimum requirements and not hold excess reserves. As such, this created an interbank lending market where banks lent to each other overnight in order to fulfill their reserve requirements. This is the federal funds market. The Fed set the federal funds rate, which is the market-determined interest rate at which banks borrowed and lent on this overnight interbank market. In turn, this would affect the rate at which consumers and firms could borrow from those commercial banks, influencing broader economic activity.

Consider the demand curve for reserves. This is downwards-sloping for the standard reasons i.e. if it is cheaper to borrow, banks will demand more reserves. However, it is kinked and plateaus on either side. After all, no one is going to borrow at above the discount rate, since they could just borrow from the Fed. Equally, everyone will borrow if there is no cost to borrowing. As for the supply curve for reserves, this is set by the Fed as a monopolistic supplier. It controls the supply of reserves via open market operations. This is where it buys or sells government securities in exchange for reserves. Securities are just government debt, with Treasury bills being those that have a maturity of a year or less, Treasury notes being those between 2 to 10 years, Treasury bonds being those with 30-year maturities and Treasury Inflation-Protected Securities being 5, 10 and 30-year debts which are indexed to inflation.

![Corridor System](/assets/corridor.png){:width="675px"}

These OMOs are done at the Trading Desk of the New York Fed. The desk buys a portfolio of Treasury securities which it holds, to ensure a baseline level of reserves. Then it adjusts this quantity via repurchase agreements with primary dealers. A repurchase agreement is a deal where one side sells an asset and promises to buy it back soon afterwards at a higher price - in effect, this is a way of doing collateralised lending i.e. lending where there is some sort of asset to back up the loan in case of default. It's a bit like taking out a mortgage, where your house is used as collateral and can be seized by the bank if you fail to repay your mortgage on time. A primary dealer is a government securities dealer who has a trading relationship with the Fed. So if the Fed wants to increase the supply of reserves, it will ask the desk to engage in repo agreements, by buying a Treasury security overnight and selling it back to the primary dealer the next day. Although this initially operates in the collateralised lending market rather than the uncollateralised lending market that is the federal funds market, primary dealers will deposit the money they receive at banks. Since they operate within the federal funds market, this will increase the supply of reserves there. Via these OMOs, the Fed enacted monetary policy via this "corridor system", where the intersection of the supply and demand curves determined the prevailing FFR.

However, this changed during the financial crisis. The incredible volume of emergency bank lending from the Fed massively expanded the supply of reserves. According to Chairman Bernanke in "The Courage to Act", this could have led "short-term interest rates to fall below our federal funds target and thereby cause us to lose control of monetary policy". Although this was briefly offset by sterilisation i.e. contractionary OMOs where Treasury bonds were sold, this was not a long-term solution because the Fed did not have an indefinite amount of Treasuries to sell. Consequently, the Fed introduced an additional tool: interest on reserves - this meant that it now paid banks on the reserves it held. Banks would have no incentive to lend at less than that, since they could earn those returns risk-free just by letting the reserves sit there. As such, the discount rate and IOR rate set a ceiling and a floor on the FFR. And since 2008, the supply of reserves is so ample that it intersects the demand curve at the IOR rate. This is the "floor system", where the FFR is determined not within a corridor of values but by the level at which the floor is set, allowing the Fed control even with an oversaturation of reserves.

![Floor System](/assets/floor.png){:width="675px"}

In practice, it's a little more complicated than the description above. Firstly, there are actually three discount rates. The primary credit rate is the rate at which financially sound institutions can borrow. The secondary credit rate is slightly higher, and is for institutions which may be smaller and less sound. The seasonal credit rate even higher, and is for institutions which face seasonally-variant cash flows. And sometimes banks do borrow at a rate above all the discount rates, because there is a stigma associated with needing to borrow at the discount window from the Fed i.e. it signals that you are unable to get private counterparty banks to lend to you. Secondly, there are IOR rates: there is an interest rate paid on required reserves and an interest rate paid on excess reserves. However, this has been rendered redundant right now because the reserves requirement has been set to 0 since the covid-19 crisis, equalising the IORR and IOER. And in fact, this doesn't act as an exact floor either, because not every financial institution in the federal funds market has access to IOR. So they could potentially be willing to lend at even below the IOR rate, pushing the FFR below this floor. This is why the Fed introduced overnight reverse repurchase agreements to this broader set of institutions. These are the reverse of the repo agreements discussed previously, allowing financial institutions to deposit reserves overnight and receive Treasuries as collateral, with the Fed buying back the Treasuries the next day for slightly more than the reserves deposited i.e. in effect lending to the Fed at the ON RRP rate. In practice, the federal funds rate has been somewhere in between the IOR and the ON RRP rate since this introduction.

It is true that the implementation of this leaky floor has given the Fed a more direct way of controlling the FFR via simply adjusting the IOR and ON RRP rates instead of through OMOs, allowing for emergency lending not to cause the FFR to plummet. But this is not costless. In particular, the fact that the FFR is at or below the IOR is unhelpful, because it means that the creation of extra reserves does not necessarily increase bank lending. Instead, commercial banks may decide that they can hoard these reserves instead of using it for more bank loan creation. So it becomes easy for monetary policy to be too tight[^2]. Not only does this neuter the effectiveness of monetary policy, it also reduces the volume of lending in the federal funds market - this is especially problematic, because it reduces the incentive to monitor interbank risks[^3].

[^2]: [Beckworth 2018](https://www.mercatus.org/system/files/beckworth-great-divorce-mercatus-research-v6.pdf)
[^3]: [Selgin 2018](https://www.cato.org/sites/cato.org/files/pubs/pdf/working-paper-50-updated-3.pdf)

So far, we've seen how the Fed can use reserve requirements, the discount rates, IOR rates, ON RRP rates and temporary OMOs via repo to influence the FFR. But beyond just changing the manner in which the FFR is determined through these tools, the Fed has also expanded its range of options since the GFC in three main ways.

1. Large-scale asset purchases of quantitative easing and credit easing.
2. Forward guidance and conditional commitment.
3. Emergency lending facilities and credit swap lines.

Large-scale asset purchases are similar in principle to OMOs as a form of monetary policy i.e. they involve the Fed buying up assets, raising their prices and lowering their yields. The result of this wealth effect and cheaper borrowing costs bolster economic activity. However, there are a few differences in practice. Firstly, this is done on a far larger scale than the usual OMOs - hence the name. Secondly, LSAPs involve a much wider range of assets - rather than just buying the usual government securities, the Fed also bought up longer-term government securities, mortgage-backed securities and corporate bonds. This means that the effect is expanded beyond the very short-run. Thirdly, there are different sorts of LSAPs. Quantitative easing is aimed at increasing the money supply, while credit easing is aimed at reducing long-term interest rates by specifically considering the composition of assets it is buying up.

For forward guidance and conditional commitment, these terms refer to "open mouth operations" conducted by the Fed i.e. the use of words as a tool of monetary policy. Because agents in the economy are forward-looking, the Fed's words regarding what it plans to do and the conditions upon which it is going to engage in easing or tightening set expectations which affect their behaviour. In practice, the effectiveness of this sort of talk depends on its credibility. On the one end is Delphic forward guidance, where the Fed simply alludes to the likely state of the world in the future, as though it were the Oracle of Delphi. On the other end is Odyssean forward guidance, where the Fed binds itself to future policy actions conditional upon certain indicators, much as Odysseus bound himself to the mast of his ship. A particularly profound level of commitment is the Fed's recent shift in its policy regime. In the past, it had looked at its dual mandate of 2% inflation and full employment as one where the Fed targeted 2% inflation every year. If it missed the target, it would still be targeting 2% inflation the next year. The problem with this is that if the target is missed again and again (as it has been since 2008), people's inflationary expectations will fall and so actual inflation will too, resulting in further misses. The new regime of average inflation targeting ensures that the Fed is committed to making up for shortfalls, such that inflation averages 2% over time. Suppose there is a demand-side shock that pushes down output and inflation - the advantage of this approach is that even when nominal interest rates are near 0, the credible expectations of future inflation will reduce longer-run real interest rates too, making monetary policy more potent.

And finally, emergency lending facilities are essentially programs the Fed can set up to support specific lending and funding markets in "unusual and exigent circumstances" under Section 13(3) of the Federal Reserve Act. Since the passing of the Dodd-Frank Act in 2010, the Fed's ability to engage in these programs has been vastly limited, only to be available with the consent of the Treasury and only for programs with "broad-based eligibility".  These facilities ensure that key financial markets which the broader financial ecosystem depends upon do not fail. For example, the market for Treasury securities is important, because the interest rates on Treasuries act as a baseline benchmark for many other interest rates. When the market is illiquid in its market liquidity i.e. it is difficult to buy and sell those assets, this means the transactions necessary for financial markets to accurately be used for risk management and investment is disrupted. Now in the case of Treasuries, OMOs are already used for this purpose - but there are plenty of other asset markets where it is necessary for the Fed to set up ad hoc lending liquidity and credit facilities. The Fed also engages in emergency liquidity provision at an international scale via dollar swap lines - in effect, the Fed lets foreign central banks exchange their currency for dollars. This is important due to the global role the dollar has, as it ensures other central banks can support dollar-denominated markets in their own countries.

In the aftermath of the 2008 crisis, the Fed engaged in all of these policies. It engaged in three rounds of LSAPs (2008-2010, 2010-2011 and 2012-2014)[^4]. It also conducted the Maturity Extension Program - commonly known as Operation Twist, this kept the size of the Fed balance sheet the same but changed the composition of Treasuries to those with longer maturities. In effect, this was a way of committing to a lower-for-longer approach, in conjunction with the language of its public statements[^5]. And of course, it deployed a whole host of emergency 13(3) facilities. In the covid-19 crisis, the Fed once again engaged in all of these policies[^6].

[^4]: [New York Fed 2017](https://www.newyorkfed.org/markets/programs-archive/large-scale-asset-purchases)
[^5]: [Federal Reserve Board 2019](https://www.federalreserve.gov/monetarypolicy/timeline-forward-guidance-about-the-federal-funds-rate.htm)
[^6]: [Federal Reserve Board 2020](https://www.federalreserve.gov/newsevents/pressreleases/monetary20200323b.htm)

**Going Forward**

We can see clearly that money is crucial in our modern economy. In the long run, the effects are nominal, but in the short run, they are very real. And the consequence of that is the need for monetary policy to help alleviate these fluctuations. In practice, this looks like what the Fed has done, using a range of tools to meet its dual mandate. Of course, much of this has been quite focused on the intuition and the historical context. In Part II, we'll look at some of the empirical data demonstrating the key notions in monetary theory: the quantity theory of money, the long-run neutrality of money and the short-run non-neutrality of money.