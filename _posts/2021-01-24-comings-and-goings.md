---
layout: post
title: "Comings and Goings: Migration as a Free Lunch"
date: 2021-01-24
tags: economics effortposts 
---

Within hours of being inaugurated, President Biden rolled back various immigration restrictions that had been put in by the Trump administration across the last 4 years, gesturing a significantly more progressive stance to the free movement of people into the US. Inevitably, this will reopen debates around the costs and benefits of more or less migration. In particular, this involves looking not just at the effects of migration on the receiving country, but also on the country which people are leaving.

**The Economics 101 of Immigration**

Normally, I would just dive right into looking at what the empirical literature says, but instead I want to consider some first-pass ways of framing the question of whether immigration is good for the receiving country. The first is just to consider a simple supply and demand model of the labour market - although this sucks as a representation of the labour market, the fact that an influx of immigrants both increases the supply of labour and by their spending increases the demand for labour means that at first blush, the effect on wages is ambiguous.

Notice this already debunks the absurdly common criticism that "basic Economics 101 principles" tells us that an outwards shift of the supply curve would *ceteris paribus* lower prices, which means lower wages for domestic workers. This lump of labour fallacy, which assumes there is a fixed amount of work that needs to be done, is silly because all else is not equal - as we noted, labour demand changes too. So if your Econ 101 class did not teach you to move more than one curve at a time, please ask for your money back.

Secondly, we can consider what happens in a Solow model with a Cobb-Douglas production function and the standard equation of capital stock change.

$$ Y = K^\alpha L^{1-\alpha} $$
$$ \dot{K} = sY - \delta K $$

We know that at the Solow model's steady state, we have $\dot{K}=0$.

$$ sK^{*\alpha} L^{1-\alpha}=\delta K^* $$
$$ K^{*1-\alpha} = \frac{s}{\delta} L^{1-\alpha} $$
$$ K^* = \left(\frac{s}{\delta}\right)^\frac{1}{1-\alpha} L $$
$$ Y^* = \left(\frac{s}{\delta}\right)^\frac{\alpha}{1-\alpha} L $$

In particular, what we are actually interested in is output per person $y$. Notice that this doesn't depend on the size of the labour force - as such, a one-off influx of immigrants will have no effect on living standards. This would suggest that the only effect of immigration (if at all) will be in the short run, where per capita output may drop temporarily, depending on how long is needed for capital to accumulate to reach its previous capital-labour ratio.

$$ y^* = \left(\frac{s}{\delta}\right)^\frac{\alpha}{1-\alpha} $$

Thirdly, we can augment this Solow model to include endogenous growth, since we know that countries do grow in real life. We can bolt on a process of Total Factor Productivity improvement onto the basic Solow setup, where this is dependent on a portion of the labour force working in research.

$$ Y = A K^\alpha L_y^{1-\alpha} $$
$$ \dot{K} = sY - \delta K $$
$$ \dot{A} = zAL_a $$
$$ L = L_y + L_a $$
$$ L_a = \ell L $$

We can write out the growth rate of the various variables to get the balanced growth path. We get the first two from their equations of change, while we take the population to be constant as before. And for $g_K$ to be constant on the balanced growth path when $s$ and $\delta$ are fixed parameters, that means $\frac{Y}{K}$ must be constant. The only way the output-capital ratio is constant is if output grows at the same rate as capital.

$$ g_Y = g_A + \alpha g_K + (1-\alpha) g_{L_y} $$
$$ g_A = \frac{\dot{A}}{A} = zL_a = z\ell L $$
$$ g_K = \frac{\dot{K}}{K} = s\frac{Y}{K} - \delta $$
$$ g_{L_y} = 0 $$
$$ g^*_Y = g^*_K $$

This gives us the balanced growth path of output - insofar as there is no population growth, this is the growth rate of output per capita too.

$$ g^*_Y = \frac{1}{1-\alpha} z\ell L $$

Although this model is by no means a perfect description of growth in practice, it does tells us that a larger population due to immigrants might have an actively positive effect on growth, because there could be scale effects on innovation in larger populations.

Fourthly, we can consider Krugman's parable about trade: a new entrepreneur uses some secret technology that converts domestic exports into consumer goods. Hailed as a magician, investigative reporters uncover the truth - it isn't a machine, it's just that entrepreneur exporting goods and buying imports. It's not entirely clear where the substantive difference is, and yet people worry a lot more about the dislocation caused once it is framed in the second way.

Likewise, we can draw parallels between immigration and the process of the population having more babies. The substantive effect is the same, and yet we don't worry about every generation being larger as potentially pushing wages or employment downwards - immigration just represents babies from elsewhere. This is why it should be a reasonable guess that the effect of immigration are fairly ambiguous.

To be entirely clear, all four of our aggregate approaches so far are approximations, and importantly they miss out a crucial component of the debate i.e. heterogeneity in labour markets. If the composition and characteristics of immigrants is identical to the native workforce, there will be no information lost from taking the aggregate approach. However, disparities could cause shifts we don't see by treating labour as homogenous. For example, an abundance of low-skilled workers might alter their relative wages within the country. Another example would be how immigrants may end up being complements rather than substitutes for native workers, due to having differing skillsets. So let's look at the empirical literature to see the sorts of effects that actually occur.

**The Empirical Literature**

Firstly, we can resolve the ambiguity mentioned previously - between 1980 and 2000, the increased demand caused by immigrants meant that each immigrant created 1.2 native jobs i.e. the effect of greater demand dominated[^1]. Secondly, even the increased labour supply can be helpful - because immigrants accept lower wages, this decreases the average labour cost and means that more jobs for natives are created[^2]. Consequently, the legalisation of more immigration can raise income for native workers, based on a model calibrated to the economies of the US and Mexico from 2000 to 2010[^3].

[^1]:[Hong and McLaren 2015](https://www.nber.org/papers/w21123)
[^2]:[Albert 2021](https://www.aeaweb.org/articles?id=10.1257/mac.20190042)
[^3]:[Chassamboulli and Peri 2015](https://www.nber.org/papers/w19932)

Notice these benefits occur even when the immigrants are low-skilled. This is because of a third mechanism, where low-skilled immigrants caused low-skilled native workers in the US to pursue careers in which they have the comparative advantage, such as those which are less manual-intensive and involve more communications[^4]. Notice that this results from the fact that even within the category of low-skilled workers, immigrants are imperfect substitutes for natives - a good example would be in California, where immigration stimulated the demand and wages of native workers between 1960 and 2004[^5]. Similarly, the wages, employment and occupational mobility of unskilled native workers in Denmark actually saw an increase as a result of low-skilled immigrants[^6]. Crucially, this effect is seen further downstream, with the net effect of a 1 percentage point increase in the share of the population from ages 11 to 64 increasing the probability of natives aged 11 to 17 completing 12 years of schooling by 0.3 percentage points[^7]. In doing so, it enhances the earning possibilities of natives.

[^4]:[Peri and Sparber 2009](https://www.aeaweb.org/articles?id=10.1257/app.1.3.135)
[^5]:[Peri 2007](https://www.nber.org/papers/w12956)
[^6]:[Foged and Peri 2016](https://www.aeaweb.org/articles?id=10.1257/app.20150114)
[^7]:[Hunt 2012](https://www.nber.org/papers/w18047)

Furthermore, even in the cases where immigrants are substitutes and cause wages to fall in the short run, these seem to be very minimal due to the ability for firms to adjust their production technologies, as seen in the US in the early 1900s[^8] as well as in the 1980s and 1990s[^9]. This has been corroborated by the 1964 *bracero* exclusion in the US, which had no effect on domestic workers despite increasing immigration barriers and reducing the labour supply[^10].

[^8]:[Lafortune, Lewis and Tessada 2019](https://www.mitpressjournals.org/doi/abs/10.1162/rest_a_00775)
[^9]:[Lewis 2011](https://academic.oup.com/qje/article/126/2/1029/1869919)
[^10]:[Clemens, Lewis and Postel 2018](https://www.aeaweb.org/articles?id=10.1257/aer.20170765)

**High-Skilled Innovation**

These are buttressed by a second sort of benefits, relating to high-skilled immigrants in particular. In the US, immigrants are twice as likely to be granted patents and to start new businesses[^11]. In fact, a 1 percentage point increase in the share of college-graduated immigrants boosts patents per capita by up to 18%[^12]. This effect was seen in citations too, with areas having more prevalent immigrant inventors between 1880 and 1940 seeing more citations from 1940 to 2000[^13].

[^11]:[Denhart 2015](http://gwbcenter.imgix.net/americas_advantage_final_pdf.pdf)
[^12]:[Hunt and Gauthier-Loiselle 2010](https://www.aeaweb.org/articles?id=10.1257/mac.2.2.31)
[^13]:[Akcigit, Grigsby and Nicholas 2017](https://www.aeaweb.org/articles?id=10.1257/aer.p20171021)

In part, this is a function of self-selection - for example, Mexican immigrants to the US are disproportionately educated compared to Mexico's average[^14]. Consequently, STEM immigrants have had a significant direct effect on increasing TFP growth in the US between 1990 and 2010, in addition to raising wages for both college-educated and non-college-educated native workers[^15]. This is augmented by the fact that cultural diversity itself also accrues benefits to productivity[^16].

[^14]:[Chiquiar and Hanson 2002](https://www.nber.org/papers/w9242)
[^15]:[Peri, Shih and Sparber 2014](https://www.nber.org/papers/w20093)
[^16]:[Ottaviano and Peri 2006](https://academic.oup.com/joeg/article/6/1/9/1056407)

The result of all of this is that more relaxed immigration restrictions were associated with innovation[^17] and within a state, an increase of employment by 1% due to immigrants led to an increase in income per worker of 0.5%[^18]. As seen in Brazil, the influx of these high-skilled immigrants has long run benefits with respect to income per capita and the level of education[^19].

[^17]:[Kerr and Lincoln 2010](https://www.journals.uchicago.edu/doi/full/10.1086/651934)
[^18]:[Peri 2009](https://www.nber.org/papers/w15507)
[^19]:[Rocha, Ferraz and Soares 2017](https://www.aeaweb.org/articles?id=10.1257/app.20150532)

**Net Effects**

The consequence of all of this is that across 22 OECD countries between 1986 and 2006, the overall impact of immigration on per capita GDP is positive, even where immigration policies are non-selective[^20]. To the extent to which there are mixed or negative effects, these are very small and very much limited to previous waves of immigrants[^21] or natives without a high school diploma[^22]. And because of the composition of immigrants in the US, coupled with the pace of production technology adjustment, the negative effects on the absolute or relative wages of even those groups have been very limited[^23].

[^20]:[Boubtane, Dumont and Rault 2016](https://academic.oup.com/oep/article/68/2/340/2364632)
[^21]:[Ottaviano and Peri 2011](https://onlinelibrary.wiley.com/doi/full/10.1111/j.1542-4774.2011.01052.x)
[^22]:[Ottaviano and Peri 2008](https://www.nber.org/papers/w12497)
[^23]:[Peri 2016](https://www.aeaweb.org/articles?id=10.1257/jep.30.4.3)

**Identification and the Mariel Boatlift**

All of the studies above involve very careful identification strategies, because as we all know, correlation does not imply causation. Immigrants may well be drawn to economically booming areas and leave economically weaker areas - as such, it is very useful if there is a natural experiment, where an exogenous shock causes immigration for non-economic reasons. The most prominent case of this is the Mariel Boatlift.

After 20 years of no immigration between Cuba and Miami, Fidel Castro lifted the ban on Cubans to emigrate in 1980. In the span of half a year, around 125,000 Cubans immigrated to Miami from the Mariel harbour in Cuba. This resulted in the Miami workforce rising by 7% that year, compared to the national average of 0.3% per annum. If there was going to be an effect on wages and employment from immigration, it would happen here. This would be especially pronounced for low-skilled workers, since most of the immigrants were low-skilled. And yet, Professor David Card found in his seminal study that there was basically no effect on low-skilled workers, even including those who had immigrated earlier[^24].

[^24]:[Card 1990](https://davidcard.berkeley.edu/papers/mariel-impact.pdf)

Importantly, this was not because the workers who faced a wage drop moved away[^25]. Rather, it involved an increased labour demand[^26] and the adoption of production technology which use more low-skilled labour[^27].

[^25]:[Card and DiNardo 2000](https://davidcard.berkeley.edu/papers/do-immig.pdf)
[^26]:[Bodvarsson, Van den Berg and Lewer 2008](https://www.sciencedirect.com/science/article/pii/S0927537108000316)
[^27]:[Lewis 2004](https://www.philadelphiafed.org/-/media/frbp/assets/working-papers/2004/wp04-3.pdf)

Famously, there was a contradictory study by Professor George Borjas, who argued that because 60% of the Marielitos did not have a high school diploma, the relevant comparison was not just those with a high school diploma or less, but only those who had dropped out of high school. By isolating only those individuals, there was a dramatic drop in wages of up to 30%[^28].

[^28]:[Borjas 2017](https://journals.sagepub.com/doi/10.1177/0019793917692945)

Unfortunately, Borjas's study looks at a very specific sample - it takes everyone with a high school diploma or less and then excludes women, Hispanics, non-prime age workers (between 19-24 and 60-65 years old) and those with a high school diploma. That results in 17 workers every year - that is, 91% of the data points have been stripped away. The problem with such a tiny statistical artifact is that it's results are not terribly representative and very sensitive to changes in methodology.

As it turns out, the way some of the data was found was changed after the boatlift, with far more black workers being included than before. Due to their lower earnings on average in that specific situation, this exaggerated the wage decline[^29]. Unfortunately, it is impossible to exclude black workers from Borjas's analysis, because that leaves us with 4 observations a year i.e. 98% of the data is gone. If the composition of those interviewed for data collection is instead adjusted for, Borjas's result is much more fragile[^30]. And if we simply took the group of all high school dropouts, the result disappears entirely[^31]. So the main takeaway from the Mariel boatlift is that the general premise from before remains true - [Noah Smith](https://noahpinion.substack.com/p/why-immigration-doesnt-reduce-wages) has a few more natural experiments for the curious.

[^29]:[Clemens and Hunt 2017](https://www.nber.org/papers/w23433)
[^30]:[Clemens 2017](https://www.cgdev.org/sites/default/files/mariel-blog-supplement.pdf)
[^31]:[Peri and Yasenov 2015](https://www.nber.org/papers/w21801)

**Inequality and Welfare**

Clearly employment and wages matter - but they aren't the be all and end all. Some have argued that there are less obvious costs of having immigrants, in the form of more inequality and larger welfare costs. By now, it should be clear that it is unlikely inequality will be significantly affected by immigration, insofar as the skill distribution of immigrants in places like the UK are very similar to the native workforce[^32]. To the extent to which they increase inequality, they do so because they are concentrated on the high-skilled and low-skilled sections of the workforce, and do not increase inequality for the native workforce[^33]. Instead, things like skill-based technology change i.e. automation[^34], housing prices[^35] and fiscal policy[^36] are much more responsible.

[^32]:[Dustmann, Fabbri and Preston 2005](https://www.ucl.ac.uk/~uctpb21/Cpapers/ecoj_1038.pdf)
[^33]:[Card 2009](https://www.aeaweb.org/articles?id=10.1257/aer.99.2.1)
[^34]:[Autor, Katz and Kearney 2008](https://scholar.harvard.edu/lkatz/publications/trends-us-wage-inequality-revising-revisionists)
[^35]:[Rognlie 2015](https://www.brookings.edu/wp-content/uploads/2016/07/2015a_rognlie.pdf)
[^36]:[Gupta 2014](https://www.imf.org/external/np/pp/eng/2014/012314.pdf)

As for public finances and welfare programs, most studies find that immigrants produce a positive net fiscal effect[^37]. In part, this is because even illegal immigrants pay taxes[^38]. It is also because poor immigrants use welfare less than comparable natives[^39]. Indeed, even undocumented immigrants contribute more than they cost the public[^40].

[^37]:[Nowrasteh 2014](https://www.cato.org/sites/cato.org/files/pubs/pdf/working-paper-21-fix.pdf)
[^38]:[Gee et al. 2017](https://itep.org/immigration/)
[^39]:[Bruen and Ku 2013](https://www.cato.org/sites/cato.org/files/pubs/pdf/edb17.pdf)
[^40]:[Lipman 2006](https://scholars.law.unlv.edu/cgi/viewcontent.cgi?article=1827&context=facpub)

To the extent to which immigrants take more than they put in, this only occurs for first-generation ones, because of the high costs of childrearing, though even this doesn't occur more so than for native parents[^41]. Furthermore, this is paid back by the second generation of immigrants, who are stronger economic contributers than even natives[^42]. By considering both the labour market effects and the impacts on government redistribution, a general equilibrium model applied across 20 OECD countries finds that immigration improves wellbeing of both high-skilled and low-skilled natives[^43].

[^41]:[Greenstone and Looney 2010](https://www.hamiltonproject.org/assets/legacy/files/downloads_and_links/09_immigration.pdf)
[^42]:[Blau and Mackie 2017](https://www.nap.edu/catalog/23550/the-economic-and-fiscal-consequences-of-immigration)
[^43]:[Battisti et al. 2017](https://academic.oup.com/jeea/article/16/4/1137/4653490)

**Assimilation, Crime and Refugees**

Another angle of opposition to immigration is about non-pecuniary factors - specifically, their ability to assimilate and not get involved with criminal activities. In general, migrant assimilate culturally - for example, the social values of Muslim immigrants are somewhere between that of their own country and that of their country of destination[^44]. Another example would be the fact that immigrants to the US are learning English at a faster rate than ever before[^45]. And this is reflected in the fact that second-generation immigrants following the 1965 Immigration Reform Act in the US have on average higher education levels and wages than children of natives, suggesting they've caught up and assimilated rather quickly[^46]. And while it is true that not every immigrant community has assimilated, a lot of this is down to a bad equilibrium - for example, this is exemplified by how French discrimination against Muslims may lead to a reluctance to assimilate, making their incongruity even more salient and causing even more discrimination[^47].

[^44]:[Norris and Inglehart 2012](https://doi.org/10.1111/j.1467-9248.2012.00951.x)
[^45]:[Waters and Pineau 2015](https://www.nap.edu/catalog/21746/the-integration-of-immigrants-into-american-society)
[^46]:[Card 2005](https://davidcard.berkeley.edu/papers/new-immig.pdf)
[^47]:[Adida, Laitin and Valfort 2012](http://ftp.iza.org/dp6953.pdf)

Certainly however, this does not mean their lack of assimilation causes crimes. A meta-analysis suggests that there is practically zero magnitude association between immigration and crime[^48]. In fact, foreign-born immigrants are less likely than the average native to commit crimes[^49], with immigrants to the US being incarcerated at a fifth of the rate of natives[^50]. As with the previous areas, being an undocumented immigrant doesn't change this finding either[^51]. Where crime does occur, this is usually for financial motives and related to poor labour market outcomes[^52].

[^48]:[Ousey and Kubrin 2018](https://www.annualreviews.org/doi/full/10.1146/annurev-criminol-032317-092026)
[^49]:[Bersani 2014](https://doi.org/10.1080/07418825.2012.659200)
[^50]:[Butcher and Piehl 2007](https://www.nber.org/papers/w13229)
[^51]:[Light and Miller 2018](https://onlinelibrary.wiley.com/doi/full/10.1111/1745-9125.12175)
[^52]:[Spenkuch 2013](https://academic.oup.com/aler/article/16/1/177/135166)

Importantly, the benefits of immigration are robust to those entering the country being refugees, who still contribute positively to the economy[^53]. Although it is true that refugees generally start out less successful and being more low-skilled, they surpass within 15 years, earning and improving their human capital more than economic immigrants[^54].

[^53]:[Betts et al. 2014](http://www.rsc.ox.ac.uk/files/publications/other/refugee-economies-2014.pdf)
[^54]:[Cortes 2004](http://ftp.iza.org/dp1063)

**Spatial Misallocation**

We've spent a lot of time discussing the benefits of immigration. But throughout all of this, we haven't discussed the most important people: the migrants themselves. The reason why making migration easier is useful, above all else, is because borders are arbitrary constraints that cause the spatial misallocation of labour. The biggest cause of cross-country income disparity is TFP differences, caused by gaps in technologies and institutions - by artificially trapping labour in places that are deeply unproductive, we are losing out on a huge amount of potential output.

For example, it is found that the place premium i.e. the disparity in wages between identical workers in different countries, of a medium-skilled worker from a median country moving to the US is on the order of $10,000 per annum[^55]. In other words, this is roughly double income per capita in the developing world. Indeed, we can see this by considering the income per capita, organised not by which country one is in but by which country one was born in - when considered thusly, we can see that 40% of living Mexicans escaped poverty by leaving Mexico and that rises to 80% for Haitians[^56].

[^55]:[Clemens, Montenegro and Pritchett 2009](https://dash.harvard.edu/handle/1/4412631)
[^56]:[Clemens and Pritchett 2008](https://onlinelibrary.wiley.com/doi/epdf/10.1111/j.1728-4457.2008.00230.x)

Certainly, this would be one of the most powerful development policies available, to the order of 40 times more effective than any sort of direct aid interventions[^57]. Open borders would yield welfare gains equivalent to a miraculous doubling of income levels in developing countries[^58]. In the words of Dr. Michael Clemens, there are "trillion dollar bills [lying] on the sidewalk"[^59]. And although it is true that there is a danger of migrants transmitting low productivity, we are nowhere close to that being a problem[^60].

[^57]:[Pritchett 2018](https://www.cgdev.org/publication/alleviating-global-poverty-labor-mobility-direct-assistance-and-economic-growth)
[^58]:[Kennan 2012](https://www.ssc.wisc.edu/~jkennan/research/OpenBorders.pdf)
[^59]:[Clemens 2011](https://www.aeaweb.org/articles?id=10.1257/jep.25.3.83)
[^60]:[Clemens and Pritchett 2019](https://www.sciencedirect.com/science/article/pii/S0304387818306382)

If migration is so helpful for the individuals who leave, doesn't this leave their countries of origin hung out to dry? As it turns out, it doesn't. Emigration has a positive net effect even on the sending country[^61]. This occurs via various channels: of remittances[^62], of the possibility of emigration encouraging human capital formation[^63], of emigrants building the trust needed to get FDI back to their home country[^64] and of encouraging the formation of inclusive institutions via the propagation of cultural ideas[^65].

[^61]:[Asch 1994](https://www.rand.org/pubs/monograph_reports/MR244.html)
[^62]:[Giovanni, Levchenko and Ortega 2014](https://www.nber.org/papers/w20002)
[^63]:[Chand and Clemens 2014](https://dx.doi.org/10.2139/ssrn.1299135)
[^64]:[Burchardi, Chaney and Hassan 2018](https://academic.oup.com/restud/article/86/4/1448/5078456)
[^65]:[Barsbai et al. 2017](https://www.aeaweb.org/articles?id=10.1257/app.20150517)

**Migration as a Free Lunch**

It is clear that the fact of a downwards sloping demand curve[^66] doesn't automatically prove that immigration is harmful, especially when it is based on faulty assumptions regarding capital being fixed, the composition of native workers and immigrants being perfect substitutes for native workers[^67].

[^66]:[Borjas 2003](https://www.nber.org/papers/w9755)
[^67]:[Card 2012](https://davidcard.berkeley.edu/papers/jeea2012.pdf)

In reality, a broad survey of the literature paints a much more encouraging picture. This is one of significant benefits to immigrants without noticeable harms on native workers, government services or public finances[^68]. Insofar as most problems around labour market outcomes, assimilation and welfare program usage of immigrants are negatively correlated with human capital accumulation[^69], making legal immigration easier solves most of those.

[^68]:[Kerr and Kerr 2011](https://www.nber.org/papers/w16736)
[^69]:[Drinkwater and Robinson 2011](http://repec.iza.org/dp6144.pdf)

![So Damn Hard To Immigrate](http://www.openlawlab.com/wp-content/uploads/2011/10/IMmigration-Law-Comic-Terry-Colon-Reason.jpg){:width="675px"}

In economics, we often say that there are no free lunches. But reducing migration barriers comes as close to a free lunch as it gets. Given the tiny harms and the ease of solving them, as well as the magnitude of the benefits to the receiving country, individual migrants and even the country of origin, the obvious solution is to make immigration easier and to open up borders[^70].

[^70]:[Bratsberg, Ragan and Nasir 2002](https://www.journals.uchicago.edu/doi/10.1086/339616)

