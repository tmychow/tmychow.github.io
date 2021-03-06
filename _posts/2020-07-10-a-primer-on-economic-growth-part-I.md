---
layout: post
title: "A Primer on Economic Growth: Part I - The Theoretical Underpinnings"
date: 2020-07-10
tags: economics effortposts
---

In Part I, we will consider three main paradigms about economic growth: Malthusian, neoclassical and endogenous. These models show the role of the factors of production in driving economic growth. They also demonstrate that the accumulation of these factors alone cannot be the drivers of economic growth in the long-run. Instead, the long-run driver of economic growth is increasing productivity - we will look at how that occurs via technological progression and improvements in resource allocation. 

**What is the Malthusian theory of economic growth?**

Thomas Malthus had a theory of growth in 1798, resulting in this production function:

$$ Y = f (T,L) $$

A production function relates output with the inputs in production. Malthus saw the total economic output $Y$ as being related to the land used $T$ and the labour used $L$ by some function $f$. Since the amount of land available is fixed, the only way to increase aggregate production is to increase the number of people.

It seems reasonable to suggest that there are diminishing returns from increasing the number of workers used. This is because we assume that employers would hire the most efficient worker available, so the additional worker would always be less productive. Given these diminishing returns, economic output does not increase proportionally to the labour input. This would mean that if the human population kept expanding, we would run out of resources needed to sustain ourselves.

It would suggest that a event like the Black Death would lead to an increase in GDP/capita. Indeed, the drop in England's population in 1348-1349 from 6 million to 3.5 million people caused real wages to triple in the next 150 years, though by the 1500s, real wages were back at pre-plague levels[^1].

[^1]: [Clark 2001](http://faculty.econ.ucdavis.edu/faculty/gclark/papers/secret2001.pdf)

> Doesn't this mean we will perpetually be stuck at a subsistence level?

Clearly, a lot of us aren't living at subsistence levels. And that's because of the constraints of the Malthusian model. It assumes that land and labour are the only inputs in the production process.

It also assumes that the function $f$ doesn't change, and that any productivity gains that result in greater output for the same inputs would be diluted by the growth in population. Indeed, Malthus conceived of humans as reproductive machines, kept back only by culture of abstinence and plagues.

However, by the 1900s we no longer see such a strong correlation - while productivity grew in Europe, population didn't grow as quickly. This is mirrored across the globe at various points, creating three phases of growth: Malthusian, post-Malthusian and modern[^2].

[^2]: [Galor and Weil 2000](https://pubs.aeaweb.org/doi/pdfplus/10.1257/aer.90.4.806)

- **Malthusian**: slow technological growth coupled with high birth and high death rates means population grows and shrinks alongside productivity - static per capita income
- **Post-Malthusian**: fast technological growth coupled with high birth and decreasing death rates means population grows and shrinks alongside productivity - but per capita income steadily rises
- **Modern**: fast technological progress coupled with rapidly decreasing birth and not-as-decreasing death rates means population growth slows while productivity keeps increasing - per capita income rises a lot

It is unsurprising that death rates fall over time as technology improves and we become more prosperous. What's more surprising is the reduction in fertility past a certain point of per capita income. One explanation is the *missing institutions theory*, which suggests that offspring are replacements for insurance or social security. Another is that the *cost of child rearing* increases with technological progress. The returns on child labour become lower compared to education and the likelihood of children dying is reduced, making quantity less important.

**What is the neoclassical theory of economic growth?**

The Malthusian model seems to fail once we go beyond the initial Malthusian trap. The neoclassical theory of economic growth was pioneered by Nobel Laureate Robert Solow and Trevor Swan in 1956. The Solow-Swan production model replaces the input of land with capital, where capital describes tangible manmade objects used in production e.g. machinery, buildings, and equipment. Because capital can be produced and accumulated, this represents a substantial shift from land in the Malthusian model. The Solow model has the following production function:

$$ Y = \bar{A} f(K,L) = \bar{A} K^\frac{1}{3} L^\frac{2}{3} $$

Again, we have a function $f$ describing output $Y$. However, we now have the capital used $K$ and productivity level $\bar{A}$, alongside the labour used $L$. If we imagine we had a society and cloned it, we would have $2K$ and $2L$. Unsurprisingly, the result of that would be $2Y$ - that is, there are constant returns to scaling up both factors of production. However, this does not hold for only increasing one factor of production as in the Malthusian model. Imagine if we had 10 accountants and 10 computers - although having 20 accountants and 20 computers might double their output, I suspect having 10 accountants and 20 computers would not.

Let us make a few further assumptions. For one, we will assume that all economic output becomes income, and households save a certain proportion $\bar{s}$ of their income $Y$. All of these savings are used for investments $I$.

$$ S = \bar{s} Y = I $$

Capital depreciates over time, since machinery faces wear and tear, and obselete equipment needs to be upgraded. This occurs at the rate $\delta$. Consequently, the change in the total amount of capital $\dot{K}$ is equal to investment minus depreciation.

$$ \dot{K} = I - \delta K $$

Since capital can accumulate, we don't need to worry about limits on population growth, and so we take the population growth rate to be $n$. By some algebraic manipulations we get the *Fundamental Dynamic Equation* of the Solow model where $k=\frac{K}{L}$.

$$ \dot{k} = \bar{s} \bar{A} k - (n+\delta)k $$

What this says is that the change in the capital per worker $\dot{k}$ is positively correlated with the per capita savings $\bar{s} \bar{A} k$ and negatively correlated with the population growth rate $n$ and the depreciation rate $\delta$. Furthermore, there is a theoretical point $k^*$ where $\dot{k}=0$ and so the investment in new capital is just enough to offset the population increase and capital depreciation.

> This is all very mathsy. What does this mean?

Firstly, the long-run growth rate of output is zero and not determined by the savings rate. This is because the capital per worker will keep increasing when $k < k^* $ and once $k > k^* $, it will decrease. This means there is a steady state at $ k^* $ where the capital-labour ratio and thus per capita income will be static.

Secondly, the savings rate determines the level of per capita income at the steady state.

Thirdly, we cannot keep increasing the savings rate to increase the per capita income at the steady state. This is because there is a limit - consider a savings rate of 1, where all income is saved. This would be infeasible, since consumption right now would be 0.

The general result of the Solow model is that countries with similar parameters (savings rate, population growth rate and technology level) will converge at the same steady state of per capita income.

We can see two practical observations. Firstly, the idea of convergence explains how post-war Germany rebounded so quickly. Secondly, the idea of parameters changing steady states explains how some of the Asian Tigers grew so quickly. Empirical analysis of their growth suggests that their productivity increases played a critical role in their catch-up - almost 30% of their annual growth rate[^3]. Although there has been some controversy with some authors attributing their growth to an increase in the fraction of the population at work and high investment rates in physical and human capital[^4], the consensus among modern research credits a larger role to technological catch-up[^5][^6].

[^3]: [World Bank 1991](https://openknowledge.worldbank.org/bitstream/handle/10986/5974/WDR%201991%20-%20English.pdf?sequence=1&isAllowed=y)
[^4]: [Young 1995](http://www.jstor.com/stable/2946695)
[^5]: [Klenow and Rodriguez-Clare 1997](https://www.nber.org/chapters/c11037.pdf)
[^6]: [Hsieh 1999](https://pubs.aeaweb.org/doi/pdfplus/10.1257/aer.89.2.133)

The case of the Asian Tigers points to a broader issue with the basic Solow model - it assumes only physical capital exists. Instead, it is worth remembering that part of capital is human capital, which involves people investing in knowledge and in health[^7]. This can be accumulated by education and training.

[^7]: [Mankiw, Romer and Weil 1992](https://eml.berkeley.edu/~dromer/papers/MRW_QJE1992.pdf)

**What is the endogenous growth theory?**

We know from above that if there are diminishing returns to factors, factor accumulation cannot explain long-run economic growth. As such, we assumed that growth in the long-run was determined exogeneously by the value of the $\bar{A}$, the productivity level of an economy. With the Romer model of endogenous growth, we will do away with that by considering what happens if we endogenise the process of productivity gains. That is, labour is split between production and research - with ideas being non-rivalrous, we are able to get increasing returns in the model such that there isn't an eventual steady state.

$$ Y = f(A,K,L) = A K^\frac{1}{3} L^\frac{2}{3} $$

$$ \dot{A} = \bar{z} A L_{at} $$

$$ \bar{L} = L_{yt} + L_{at} $$

$$ L_{at} = \bar{\ell} \bar{L} $$

$$ g_Y^* = \frac{3}{2} \bar{z} \bar{\ell} \bar{L} $$

> Wait a second. You've assumed that labour never changes!

This is an incredibly stylised model - but the insights remain useful, because it allows for a steady growth path while being consistent with the empirical evidence of the conditional convergence that both models predict [^8].

[^8]: [Barro 1991](http://piketty.pse.ens.fr/files/Barro91.pdf)

What the Romer model uniquely shows us is that even when there are diminishing returns to capital, ideas alone can drive economic growth. This could be caused by positive externalities to capital accumulation, such as "improvements in the level of organisation, technical change, better social overhead facilities in the form of transport and communication networks"[^9]. That is, even if firms individually have diminishing returns, there can be non-diminishing returns when firms group up together due to the productivity gains.

[^9]: [Frankel 1962](https://www.jstor.org/stable/1812179)

As such, it is useful to think about endogenous growth as a way to make productivity the driver of growth in the long-run, without forgetting about the transition dynamics of capital accumulation in the shorter run. Productivity is a complicated factor that takes two forms - of technology and efficiency in resource allocation, and it is worth exploring the foundational cause of these two types of improvements.

**Where does the growth of technology come from?**

Joseph Schumpeter's paradigm of economic growth involves the prospects of profits as the basis for technological progress. This relies on the ability of researchers to extract profit from their ideas - which means they must be excludable for a while i.e. it is possible to prevent people who have not paid for it from having access to it. Excludability can come from enforcing trade secrets, the lead time of introducing a product, customer loyalty, brand recognition and reputation, and the benefits of experience.

Where these are less impactful, patents, copyrights, and trademarks can help establish private claims on intellectual property. The optimal length and breadth of patents is determined by the balance between providing ex ante incentives to researches and providing benefits to consumers from the patent expiring.

> Hold up - doesn't research cost a lot even with these benefits from excludability?

Incentives alone are not sufficient - financing constraints are important and firms may face difficulties in raising capital to finance R&D. Firstly, research projects may fail or be beaten to the patent office, meaning there is a significant probability of ex post returns being insufficient to cover loans. Secondly, there is asymmetric information where investors may not be told or may not understand the technical details - this causes a problem of moral hazard. Thirdly, R&D doesn't provide a form of collateral that lenders could take if a firm defaults.

**How can technological diffusion occur?**

There is "an advantage of backwardness" as described by Alexander Gerschenkron, since there is a possibility of less technologically developed countries adopting frontier technologies without the need to learn from the beginning. The effectiveness of this depends upon the "social capability"[^11] of the country to absorb available technologies.

[^11]: [Abramowitz 1979](https://doi.org/10.1007/978-1-349-16173-7_1)

One such mechanism for this is trade - by importing equipment, by opening up domestic firms to foreign competition, by exposing exporting firms to foreign consumers with high standards, by raising domestic expectations and by allowing export industries to arise. The advent of European economic integration helped Western Europe to catch up with the USA[^12] and there was a substantial increase in output per worker in 16 Brazilian industries after the reductions in trade barriers in the 1990s[^13]. More generally, it has been found that trade openness tends to be associated with faster adoption of technologies[^14] and faster productivity growth[^15].

The empirical effectiveness of foreign direct investment has been harder to determine. This is possibly due to country characteristics mattering for technological diffusion via FDI. It was found that the productivity effect of FDI from industrial countries in 69 developing countries was positive, but conditional upon its "absorptive capability"[^16]. The specific analysis of USA-outward FDI to fourty countries from 1966 and 1994 found that although the effects were positive in all cases, richer countries benefitted more from hosting multinational subsidiaries, confirming the importance of this baseline level of human capital[^17].

[^12]: [Parente and Prescott 2005](https://doi.org/10.1016/S1574-0684(05)01021-X)
[^13]: [Ferreira-Cavalcanti and Rossi 2003](https://www.jstor.org/stable/3663656)
[^14]: [Comin and Hobijn 2004](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=892588)
[^15]: [Sachs and Warner 1995](https://www.brookings.edu/wp-content/uploads/1995/01/1995a_bpea_sachs_warner_aslund_fischer.pdf)
[^16]: [Borenztein et al. 1998](http://www.nber.org/papers/w5057.pdf)
[^17]: [Xu 2000](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=173428)


**What are the barriers to technological diffusion?**

One reason for slow adoption is the lack of a complementary inputs. The most obvious of these is human capital, but others include physical infrastructure, business services, financial services, and government services. This is where governments play a role in shaping the absorptive capacity of a country or adapting rather than adopting foreign technology.

Another is the way in which old technology can block the new. This can be because updating to a new technology would devalue the worker's experience and skill with an old technology. It can be because of network effects e.g. if everyone uses Microsoft Word, it is convenient to keep using it even if Apple Pages is a better word processor, because there will be costs associated with sending incompatible files.

**Where do improvements in resource allocation come from?**

The other avenue of productivity gains is resource allocation, which relates to the effectiveness with which factors of production and technology are combined to produce output. The government has a role in providing goods and services the free market wouldn't. The most obvious is to provide public order, set up a coherent system to property rights and enforce contracts. Indeed, Joseph Stiglitz suggests that property rights and contract enforcement are the foundations upon which the market economy rests.

They also have a role in correcting for market failures. For example, public goods that are non-rival (consumption by one party doesn't affect the ability of another party to consume it) and non-excludable (non-paying consumers cannot be prevented from accessing it) will be under-provided by the free market. This includes thins like roads or the police force.

Externalities, where there are positive or negative effects on third parties due to the transaction of the good or services, are another area for government intervention. For example, there is a benefit to society from vaccination by building up herd immunity, and the social benefit is not factored in to an individual's decision making. As such, there is a role for governments to subsidise vaccinations to correct for the market not pricing in this social benefit.

There are also missing markets the government can compensate for. One example might be the provision of postal services in rural areas, where private companies may find it too expensive to set up a mail network. Another might be the funding for R&D, which as discussed can be stymied by the market.

In all of these cases, the government may have a role in correcting these market failures by direct provisions, regulations, taxes and subsidies, and setting up institutions. This has to be weighed against the distortionary effects these interventions can cause, especially when the government itself fails due to its limited information or inability to foresee how the market reacts.

> But we can't just snap out fingers and get efficient production processes and technological developments. What are the root causes behind them forming?

There are several theories explaining how these are formed. Each emphasises a different original factor - geography, culture, institutions etc. And although none of them explain the picture completely, they combine to form a useful picture of how we understand the disparities in growth. But that's a story for [Part II]({% post_url 2020-07-24-a-primer-on-economic-growth-part-II %})!
