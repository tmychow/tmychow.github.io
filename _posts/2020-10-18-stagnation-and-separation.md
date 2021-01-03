---
layout: post
title: "Stagnation and Separation: Where Has All the Money Gone?"
date: 2020-10-18
tags: economics effortposts
---

Watching the presidential and vice-presidential debates was a rather lackluster experience and in the words of Dana Bash, a "shitshow" - so this isn't about that. But the debates were important in reminding me of what Biden has said for a long time, which is that this election is a battle for America's soul. I'm not religious, nor particularly spiritual nor even an American, so I have no clue what America's soul is. But as an economist, a reasonable approximation seems to be the aspirational economic ideals of the American dream. One of the cornerstones of this American Dream is the idea that people's living standards will keep rising and will rise as people work harder.

While it may seem obvious why we want people's earnings to keep growing, why should labour compensation and productivity be inherently linked? Consider an economy described by a Cobb-Douglas production function with constant returns to scale. If we live in a world of perfect competition, the representative firm will set the cost of their marginal worker to be equal to what they get out of that worker - that is, the wage will equal the price times the marginal product of labour. The price of the good in this one-good economy is the price level of the economy, making the real wage the marginal product of labour.

$$Y=A K^\alpha L^{1-\alpha}$$

$$MPL=\frac{\partial Y}{\partial L}=(1-\alpha) A K^{\alpha} L^{-\alpha}$$

$$W = P \times MPL$$

$$ \text{real} \ W = MPL = (1-\alpha) \frac{Y}{L} $$

The coefficients $\alpha$ and $1-\alpha$ represent capital and labour's shares of output in this perfectly competitive world. And so we can see that real wages are determined by labour's share of output and labour productivity, and ceteris paribus, an increase in productivity should increase real wages. This is the benchmark model we can compare the real world to. 

So how does the real world compare to these two goals? One of the most prominent critiques against the current labour market is by the Economic Policy Institute, which famously published the following graphs. It would seem apparent that hourly compensation has stagnated since the 1970s. It would also seem that the previously tightly nit variables of productivity and compensation have decoupled since 1973. In other words, people's incomes are not growing as quickly as before and people's incomes are not growing alongside how hard they work. So is the American Dream dead?

![By groups](/assets/separategroups.png){:width="675px"}
![Since 1973](/assets/1973onwards.jpg){:width="675px"}

**Income stagnation**

Let's first consider the stagnation of incomes. The EPI diagram makes it look rather dire, and somewhat incongruous with the macroeconomic time series below of average real hourly compensation in the non-farm business sector. How can we reconcile the two? As it turns out, measurement matters when it comes to looking at labour market data.

[^1]: [FRED 2020](https://fred.stlouisfed.org/series/COMPRNFB)

![Nonfarm Compensation](/assets/COMPRNFB19792020.png){:width="675px"}[^1]

Firstly, the EPI data uses a Consumer Price Index as its price deflator to adjust into real terms, while the FRED series uses the Personal Consumption Expenditures index. Across long time horizons, these differences in measurement decisions make a difference - the result is that the CPI is consistently larger than PCE, resulting in a seemingly lower real wage[^2]. Secondly, the EPI data looks at hourly wages - this ignores non-wage benefits which are included in labour compensation, and are becoming an increasingly large component of compensation as seen below[^3]. Correcting for these two issues alone brings the data much closer together, and at least till 2007, changes the data from a small decline to a modest increase, including for middle America[^4].

![Inflation Measures](/assets/pcecpi.png){:width="675px"}[^5]
![Compensation Wages](/assets/compensationwage.png){:width="675px"}[^6]

[^2]: [Sacerdote 2017](https://www.nber.org/papers/w23292)
[^3]: [Fitzgerald 2007](https://www.minneapolisfed.org/article/2007/has-middle-america-stagnated)
[^4]: [Fitzgerald 2008](https://www.minneapolisfed.org/article/2008/where-has-all-the-income-gone)
[^5]: [Bullard 2013](https://www.stlouisfed.org/~/media/Files/PDFs/publications/pub_assets/pdf/re/2013/c/pres_mes.pdf)
[^6]: [Zimmermann 2016](https://fredblog.stlouisfed.org/2016/09/wages-with-benefits/)

But there remains a disparity between the mean and the median - this is likely because of the growth of the top end, which EPI allude to by having three time series for the 10th percentile, 50th percentile and 95th percentile. But unlike what EPI suggest, this isn't necessarily a bad thing. This is because taking cross-sectional snapshots at various points in time instead of following the same people over time means that we may miss out on the changing composition of groups, as per Simpson's paradox. Suppose an immigrant comes from a poorer country, creating a new business where they are earning more but less than the national average. Although everyone's life has improved, GDP per capita will fall. Similarly, it is very possible that everyone has gotten richer while new entrants with lower earning potentials have entered the workforce[^7]. So what we really need is panel data, which follows the same people over time. And the panel data that we do have suggests there have been improvements across the last few decades.

[^7]: [Daly and Pedtke 2018](https://www.frbsf.org/our-district/about/sf-fed-blog/revisiting-wage-growth-august-2018/)

![Panel Quintile](/assets/panelquintile.jpg){:width="675px"}[^8]

[^8]: [Roberts 2018](https://medium.com/@russroberts/do-the-rich-capture-all-the-gains-from-economic-growth-c96d93101f9c)

But even this sort of panel data doesn't tell us everything, because it captures a specific set of people over time. If we want to understand stagnation, we need to look at several generations of people with panel data. And this is where the single most defining paper on income stagnation for me comes into play[^9]. By looking at lifetime incomes for 27 cohorts across over 60 years, it finds that median real lifetime income has stagnated for cohorts joining the labour market following 1967, robust to different measures of inflation. The fact that this has been driven by lowering early career incomes, coupled with the rise in inequality within each gender, represents a worrying sign for income inequality going forward. So both income stagnation and inequality remain real and present dangers, even if the EPI portrayal is rather disingenous.

[^9]: [Guvenen et al. 2017](https://www.nber.org/papers/w23371)

**Productivity and Compensation**

Here's the thing - a natural response to the idea of not earning enough might be to work harder. EPI suggests that this isn't possible, because productivity has not grown in line with compensation. As before, it is worth taking a look at the nitty-gritty of measurement first. As it turns out, EPI's measurement is once again imperfect. It takes the productivity of the entire economy, while its calculation of real hourly compensation only looks at production and non-supervisory workers. In doing so, it not only ignores possibly the fastest growing 20% of the workforce, it is also comparing apples to oranges. Another issue arises due to the choice of price deflator - as the comparison is being made to productivity (which is measured with the business sector price deflator), it might behove us to do the same for real compensation. Doing all of this yields a much closer link between the two variables of productivity and real product(-deflator) compensation, as seen below.

![Adjusted Disparity](/assets/adjusteddisparity.png){:width="675px"}

This is corroborated by other studies[^10], including those that look abroad to the UK[^11]. The bottom line is that there are two sorts of decouplings - the "net decoupling" between productivity and average real product-deflated compensation and the "gross decoupling" between productivity and median real CPI-deflated wages. In both cases, the linkage with respect to productivity remains[^12]. In the former, the strength of the relationship has not really shifted much, with a possible weakening in the 21st century due to labour's share of output[^13] - and as for the latter, there has been a weakened wage gain from productivity improvements[^14]. So while we can be reasonably assured that labour as a factor of production is receiving the payments it ought to be based on its productivity, workers may nonetheless not be doing very well with respect to living standards. In particular, the disparity between the two types of decoupling relate to the average vs the median, the role of non-wage compensation and the price deflator. The first suggests that the top end is seeing compensation rise faster than most, possibly due to sectoral differences[^15]. The second says that employers are having to spend more on non-wage compensation, perhaps due to rising healthcare and pension costs. The third says that the bundle of goods being consumed is diverging from the bundle of goods being produced. Combined together, these make up the gap between the two measurements.

[^10]: [Feldstein 2008](https://www.nber.org/papers/w13953)
[^11]: [Pessoa and van Reenen 2012](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.360.9511&rep=rep1&type=pdf)
[^12]: [Stansbury and Summers 2017](https://www.piie.com/system/files/documents/summers20171109paper.pdf)
[^13]: [Fleck, Glaser and Sprague 2011](https://www.bls.gov/opub/mlr/2011/01/art3full.pdf)
[^14]: [Strain 2019](https://www.aei.org/wp-content/uploads/2019/02/The-Link-Between-Wages-and-Productivity-is-Strong.pdf)
[^15]: [Brill et al. 2017](https://www.bls.gov/opub/btn/volume-6/pdf/understanding-the-labor-productivity-and-compensation-gap.pdf)

**Doom and Gloom?**

We began with EPI's rather depressing set of portrayals. And after a lot of messy measurement issues and analysis, we seem to have ended back at a similar picture, just with better statistics. What does this all mean for how we think about the labour market? A few things stand out.

1. Incomes have not stagnated entirely, but they are growing slower than before for younger generations. This is due to the early stages of labour market entry.
2. Real compensation and wages remain as sensitive as before to productivity, but the magnitude of the effect may have diminished.
3. The "net decoupling" has been limited and only present since the 2000s, likely due to declining worker power[^16].
4. The "gross decoupling" has been significant, representing increased skill-based income inequality and rising living costs that have depressed compensation.

[^16]: [Stansbury and Summers 2020](https://www.brookings.edu/wp-content/uploads/2020/03/Stansbury-Summers-Conference-Draft.pdf)

So despite the methodological issues associated with EPI, the conclusions remain, and they remain stark. Labour markets are flawed, and they are flawed in deeply pernicious and dangerous ways, threatening the American Dream and the socio-economic prosperity associated with that integral ideal.
