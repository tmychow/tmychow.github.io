---
layout: post
title: "Facts Don't Care About Your Feelings"
date: 2020-11-20
tags: economics effortposts
---

Today is the Equal Pay Day 2020 in the United Kingdom. It is so named, because by taking the full-time mean gender pay gap in 2020, we can find the day beyond which women are effectively working for free for the rest of the year. But every year, there are those who continue to argue that the gender pay gap is impossible in a competitive labour market or that it is not a problem as it disappears after controlling for some variables. In their words, facts don't care about your feelings. That may well be true, but unfortunately for them, the facts corroborate the existence of a meaningful and statistically significant gender pay gap.

**Labour Market Overview**

When we are talking about the gender pay gap, we are referring to the disparity between men and women with respect to their pay in the workplace. This may involve "taste-based discrimination", where some firms are discriminatory and pay women less for the same job.

> In a free market, won't non-discriminatory firms hire competent workers that have been discriminated against, meaning that a wage gap doesn't form?[^1]

[^1]: [Becker 1975](http://press.uchicago.edu/ucp/books/book/chicago/E/bo22415931.html)

The problem with this characterisation is that it is dependent upon a perfectly competitive labour market. Let's introduce some labour market frictions. For example, suppose that there are search costs associated with finding a job, which seems very reasonable. For a marginalised group which faces discrimination, this likely results in them having higher search costs. As such, even firms without a taste for discrimination will be financially incentivised to pay them less, because they know that said worker has fewer choices and less bargaining power. Another example might be the lack of sufficient non-discriminatory firms to hire discriminated workers - if people face a monopsonistic labour market, they may simply not have these alternatives. As per a previous post about minimum wages, it is very likely that most labour markets face such frictions and imperfections to a non-trivial degree. As such, one would need to believe that the rather implausible claim that all conditions for a perfectly competitive labour market are fulfilled in order to think that the market alone can eliminate the gender wage gap by arbitrage. Instead, a much more data-driven approach is required.

**Controlling for Variables**

What does the data say? Well, what we see in 2020 is that women in the UK make only £0.88 for every pound a man makes. 

> Don't we need to control for other variables, like occupation, education, hours worked and so on, since they cause earnings to be different? Doesn't the gender wage gap mostly disappear when you control for these relevant variables?

It is indeed the case that the raw gap is larger than the controlled gap. But neither the initial claim nor the response represent coherent pictures of what is happening. This is because variables like occupation, education or hours worked are not exogenous - they are very much affected by how much women expect they will be paid. As such, we cannot simply assume that women earn less due to choosing lower earning degrees or jobs. It may well be the case that the existence of discrimination means they change these decisions. Because these choices are dependent variables that are outcomes of discrimination, it is not appropriate to treat them as independent control variables that can just be adjusted for in some sort of regression. Indeed, it would be disingenuous to suggest that controlling away endogenous variables like occupational choice makes the result more accurate. 

If the critique isn't clear, here's another example of a bad choice of control variables[^2]. If we are regressing wages on education to see its effect, it is the case that adding occupation as a control makes the regression more predictive. But that's really not the point of doing this! Part of going to university is that you work in a higher-paying industry - so if you control for occupational choice, you're ignoring a substantial part of the causal effect of education on wages.

[^2]: [Cochrane 2008](https://faculty.chicagobooth.edu/john.cochrane/research/papers/phd_paper_writing.pdf)

> So basically there's no way of knowing anything because of this collider bias[^3]?

[^3]: [Cunningham 2018](http://scunning.com/cunningham_mixtape.pdf)

Well, not exactly. Lots of things we want to understand have features that make causal inference difficult - that's why we employ statistical techniques carefully. For example, we can run experiments, where we can narrow down the direction of the cause and effect. Or we can build a model, where we assume away some level of collider bias. Let's deal with each of these in turn.

**Running Experimental Studies**

There are a plethora of studies to illustrate that gender discrimination exists. For example, in 300 negotiations where a potential buyer of a new car followed a scripted bargaining process, car dealers offered female buyers substantially higher prices compared to those offered to men[^4]. Another case involved undergraduates finding socially dominant female applicants "insufficiently nice" compared to the identically presented male applicants[^5]. Or yet another example, where 6,000 professors receiving emails to meet with a fictional doctoral student in a week saw white males receiving faster responses and being granted more access to faculty than women or minorities[^6]. So it is possible to demonstrate that gender discrimination exists in a general sense.

[^4]: [Ayres and Siegelman 1995](https://www.jstor.org/stable/2118176)
[^5]: [Rudman and Glick 2001](http://onlinelibrary.wiley.com.ezproxy.lib.uh.edu/doi/10.1111/0022-4537.00239/full)
[^6]: [Milkman et al. 2012](http://journals.sagepub.com/doi/abs/10.1177/0956797611434539)

> These studies aren't about jobs though. How does this show discrimination exists in the workplace?

This is where audit studies come into play - effectively, this involves sending identical resumes where the names vary in order to see if people are treated differently. Provided the sample size is large enough, the random selection of employers means that their unique features ought to be insignificant. What happens? In 65 restaurants in Philadelphia, a woman's chance of getting an interview was 40 percentage points lower than for a man's, and the chance of getting an offer was 50 percentage points lower[^7]. For laboratory management positions at science faculties, male applicants were seen as "significantly more competent and hireable", receiving a higher starting salary and more career mentoring[^8]. And when it comes to orchestras, blind auditions substantially improve the likelihood of women being hired[^9]. These are just three examples of the many that have been conducted.

[^7]: [Neumark et al. 1995](http://www.nber.org/papers/w5024)
[^8]: [Moss-Racusin et al. 2012](http://www.pnas.org/content/109/41/16474)
[^9]: [Goldin and Rouse 2000](https://www.aeaweb.org/articles?id=10.1257/aer.90.4.715)

**Conducting Multivariate Analysis**

So it is likely the case, from the plethora of experiments that have been run, that gender discrimination exists and is significant within workplaces.

> These studies show that discrimination exists in the workplace. But does that necessarily mean a gender wage gap?

In order to examine this, we can use multivariate models to break down the data into its components. In doing so, we assume away any role for collider bias and ignore that causal mechanism - that is, we are being generous and likely underestimating the extent to which the gender wage gap exists. Even so, we find that of the 23% raw gender wage gap, only 48% of the gap is accounted for by the choice of occupation and industry - the rest is either due to the 14% attributed to differences in experience and the 38% that is entirely unaccounted for[^10]. Incidentally, it is worth noting that the 14% isn't exogenous - I suspect that societal perceptions and expectations around childrearing will also have an effect on the amount of workplace experience that women are able to accrue on average. That isn't even to mention the 38% that remains having made these two key controls. 

[^10]: [Blau and Kahn 2017](https://pubs.aeaweb.org/doi/pdfplus/10.1257/jel.20160995)

One suggestion is that childrearing and caregiving expectations do not just affect occupational choice, they also affect the choice of how many hours someone works and whether they take a few years out of industry. If wages have a linear relationship with hours worked, this isn't an issue. But this isn't the case across all occupations, with some rewarding working long hours - that is, there are increasing returns to time spent working. Indeed, the research suggests that temporal flexibility is associated with a lower gender wage gap[^11]. That's why we see some of the largest gaps in occupations like business or law. This hypothesis is corroborated by research that decomposes the gender wage gap across a worker's lifetime - what we find is that in these industries, the gap starts out being quite small, but rises massively into one's career[^12]. Notice that this is exactly what is predicted by a hypothesis of non-linear compensation.

[^11]: [Goldin 2014](https://scholar.harvard.edu/files/goldin/files/goldin_aeapress_2014_1.pdf)
[^12]: [Bertrand, Goldin and Katz 2010](https://scholar.harvard.edu/files/goldin/files/dynamics_of_the_gender_gap_for_young_professionals_in_the_financial_and_corporate_sectors.pdf)

> Doesn't this mean women can just work harder?

Unfortunately, it isn't this simple. For one, there are substantial social and economic pressures for women to be the ones taking care of children - in fact, men who take on "non-traditional gender roles" like childrearing get punished in wages even more than women who do so[^13]. That is, discriminatory gender roles make this arrangement economically sensible for many households. But one we can fix it is just be looking at how these gaps have fallen in the past - the most prominent example is in pharmacies. This changed from having as large a gap as lawyers to having a much smaller one - and the solution? Well, it involved the transformation from small mom-and-pop pharmacies where the owner needed to be there the whole day to large corporate ones, where pharmacists were just people working in shifts. So these are very much endogenous to technology and to the managerial decisions around the production process, and can be fixed - after all, the mantra in the 1970s was "59 cents on the dollar". So we have and can make progress in this regard. 

[^13]: [Noonan, Corcoran, Courant 2003](http://www.npc.umich.edu/publications/working_papers/paper1/03-1.pdf)

**Yes, It Exists**

We've established that we cannot assume the gender wage gap doesn't exist from first principles by assuming a perfectly competitive labour market. It is clear that the collider bias means using endogenous variables as controls is not methodologically sound and underestimates the discrimination that occurs. We've shown that there is discrimination against women in general and in the workplace. And even if we assumed you could control for the many dependent variables, there is a still a gap unaccounted for based on the multivariate analysis. The most compelling explanation for these unaccounted differences relate to cultural attitudes around the role of women. So yes - a gender wage gap exists and it is caused by discrimination.
