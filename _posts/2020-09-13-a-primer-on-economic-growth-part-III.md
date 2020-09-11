---
layout: post
title: "A Primer on Economic Growth: Part III - Mankiw, Romer and Weil"
date: 2020-09-13
tags: economics effortposts
---

In [Part II]({% post_url 2020-07-24-a-primer-on-economic-growth-part-II %}), I promised to end this series with a more practical application of growth theory. Originally, I was going talk about the literature regarding the Industrial Revolution and the Great Divergence, but it seemed more fun to apply the theory we have seen so far onto real world data by using R. So instead, I'm going to be explaining a 1992 paper by Greg Mankiw, David Romer and David Weil called ["A Contribution to the Empirics of Economic Growth"](https://eml.berkeley.edu/~dromer/papers/MRW_QJE1992.pdf). I will also be replicating the paper in R, both for my own satisfaction and to demonstrate that the barrier to getting a feel for empirical work is sufficiently low as to allow some exploration.

MRW 1992 is about the Solow-Swan growth model. The Solow model suggests that savings and population growth determine the steady-state level of per capita income. This offers a simple test -  are countries with higher savings rates and lower population growth rates richer? MRW find that the evidence supports the basic Solow model to a first-degree of approximation, which is to say that the signs are correct. But it is only able to account for around half of the cross-country variation in income, with the magnitudes of the coefficients being wrong. 

MRW augment it by including human capital in addition to physical capital, capturing 80% of the variation in income. They further confirm that although convergence does not occur, conditional convergence does - that is, countries with the same savings and population growth rates do converge at the rate the model suggests. As such, the Solow growth model remains a useful core of theorising growth. This was an important part of the neoclassical revival, at a time when many were looking to endogenous growth models and turning their backs on the Solow model.

Consider the basic Solow model - we have a Cobb-Douglas production function with output $Y$ as well as inputs of capital $K$ and labour $L$. We have the exogenous rates of savings $s$, population growth $n$ and technological progress $g$. We can define the capital stock and level of output in relation to the effective units of labour as $k=\frac{K}{AL}$ and $y=\frac{Y}{AL}$. Capital depreciates at rate $\delta$.

$$ Y(t) = K(t)^\alpha [A(t) L(t)]^{1-\alpha} \; \text{where} \; 0 < \alpha < 1 $$ 

$$ L(t) = L(0) e^{nt} $$

$$ A(t) = A(0) e^{gt} $$

$$ \dot{k}(t) = sk(t)^\alpha - (n+g+\delta)k(t) $$

$$ k^* = [\frac{s}{n+g+\delta}]^{\frac{1}{1-a}} $$

From this set up of the model and its steady state, we can see the steady-state per capita income level. As it assumes factors are paid their marginal products, we can substitute in labour's share of income as $\alpha = \frac{1}{3}$ to produce the magnitudes of the coefficients as 0.5 for the elasticity of income per capita to the savings rate and -0.5 for the elasticity of income per capita to $n+g+\delta$. This is a testable prediction.

$$ \ln{[\frac{Y(t)}{L(t)}]} = \ln{A(0)} + gt + \frac{\alpha}{1-\alpha} \ln{(s)} - \frac{\alpha}{1-\alpha} \ln{(n+g+\delta)} $$

MRW assume that the rate of technological progress and the rate of capital depreciation are both not country-specific, such that only $A$ varies with a country-specific shock in the form of $\ln{A(0)} = a + \epsilon$. Thus the log income per capita at time 0 is below. MRW assume that $s$ and $n$ is independent of $\epsilon$. This is one of the seven classical assumptions behind ordinary least squares regression. Based on the Gauss-Markov Theorem, we know that it being true implies that OLS is BLUE - it is the best linear unbiased estimator.

$$ \ln{[\frac{Y}{L}]} = a + \frac{\alpha}{1-\alpha} \ln{(s)} - \frac{\alpha}{1-\alpha} \ln{(n+g+\delta)} + \epsilon $$

MRW take a dataset going from 1960 to 1985, considering a sample of 98 countries that are not dominated by oil production, a sample of 75 countries where the data is of non-suboptimal quality and a sample of 22 OECD countries with high quality data. Let's now do the same.

Firstly, we do some exploratory data analysis. We can see that the three factor variables allows us to separate the three different samples. We can also see that we have per capita GDP in 1960, per capita GDP in 1985, the average growth rate of per capita GDP between 1960 and 1985, the average growth rate of working-wage population between 1960 and 1985, the average ratio of investment to GDP from 1960 to 1985 and the average fraction of working-age population in secondary school from 1960 to 1985. (There is also a measure of literacy, but that's an artifact of using the Durlauf and Johnson 1995 dataset - the rest of the data is taken straight out of MRW. A csv file with just the MRW data is [here](/assets/mrw1992.csv).)

```
library(AER)
library(dplyr)
library(skimr)
library(moderndive)
data("GrowthDJ")

skim(GrowthDJ)
── Data Summary ────────────────────────
                           Values  
Name                       GrowthDJ
Number of rows             121     
Number of columns          10      
_______________________            
Column type frequency:             
  factor                   3       
  numeric                  7       
________________________           
Group variables            None    

── Variable type: factor ──────────────────────────────────────────────────────────────────────────
  skim_variable n_missing complete_rate ordered n_unique top_counts     
1 oil                   0             1 FALSE          2 no: 98, yes: 23
2 inter                 0             1 FALSE          2 yes: 75, no: 46
3 oecd                  0             1 FALSE          2 no: 99, yes: 22

── Variable type: numeric ─────────────────────────────────────────────────────────────────────────
  skim_variable n_missing complete_rate    mean       sd    p0    p25     p50     p75    p100 hist 
1 gdp60                 5         0.959 3682.   7493.    383    973.  1962    4274.   77881   ▇▁▁▁▁
2 gdp85                13         0.893 5683.   5689.    412   1209.  3484.   7719.   25635   ▇▂▂▁▁
3 gdpgrowth             4         0.967    4.09    1.89   -0.9    2.8    3.9     5.3      9.2 ▁▅▇▃▁
4 popgrowth            14         0.884    2.28    0.999   0.3    1.7    2.4     2.9      6.8 ▃▇▃▁▁
5 invest                0         1       18.2     7.85    4.1   12     17.7    24.1     36.9 ▅▇▇▅▂
6 school                3         0.975    5.53    3.53    0.4    2.4    4.95    8.17    12.1 ▇▆▅▅▅
7 literacy60           18         0.851   48.2    35.4     1     15     39      83.5    100   ▇▃▂▃▆
```

<br>

Now we can do the estimation. We take $g + \delta$ as 0.05, based on how MRW calibrated those values. First, we need to separate the three samples. Then, we can regress using OLS for each sample. We find the following results. If we compare salient features of the intercept, coefficients, their standard errors and the $R^2$ values, they are all consistent with Table I of MRW. For the sake of brevity, I've only showed the results for the first sample, but you can easily replicate the other two in your own time.

```
nonoil <- subset(GrowthDJ, oil == "no")
inter <- subset(GrowthDJ, inter == "yes")
oecd <- subset(GrowthDJ, oecd == "yes")

mrw1 <- lm(log(gdp85) ~ log(invest/100) + log((popgrowth/100) + 0.05), data = nonoil)
mrw2 <- lm(log(gdp85) ~ log(invest/100) + log((popgrowth/100) + 0.05), data = inter)
mrw3 <- lm(log(gdp85) ~ log(invest/100) + log((popgrowth/100) + 0.05), data = oecd)

summary(mrw1)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.79144 -0.39367  0.04124  0.43368  1.58046 

Coefficients:
                            Estimate Std. Error t value Pr(>|t|)    
(Intercept)                   5.4299     1.5839   3.428 0.000900 ***
log(invest/100)               1.4240     0.1431   9.951  < 2e-16 ***
log((popgrowth/100) + 0.05)  -1.9898     0.5634  -3.532 0.000639 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.6891 on 95 degrees of freedom
Multiple R-squared:  0.6009,	Adjusted R-squared:  0.5925 
F-statistic: 71.51 on 2 and 95 DF,  p-value: < 2.2e-16
```

<br>

In Table I, MRW also do a restricted regression where they set the coefficient of $\ln{(s)}$ and the coefficient of $\ln{(n+g+\delta)}$ to sum to 0. We can do the same by running a restricted regression.

```
mrw4 <- lm(log(gdp85) ~ I(log(invest/100) - log((popgrowth/100) + 0.05)), data = nonoil)
mrw5 <- lm(log(gdp85) ~ I(log(invest/100) - log((popgrowth/100) + 0.05)), data = inter)
mrw6 <- lm(log(gdp85) ~ I(log(invest/100) - log((popgrowth/100) + 0.05)), data = oecd)

summary(mrw4)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.87388 -0.43133  0.03757  0.51698  1.49645 

Coefficients:
                                                 Estimate Std. Error t value Pr(>|t|)    
(Intercept)                                        6.8724     0.1206   56.99   <2e-16 ***
I(log(invest/100) - log((popgrowth/100) + 0.05))   1.4880     0.1247   11.93   <2e-16 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.6885 on 96 degrees of freedom
Multiple R-squared:  0.5974,	Adjusted R-squared:  0.5932 
F-statistic: 142.4 on 1 and 96 DF,  p-value: < 2.2e-16
```

<br>

Again, we see that it corresponds to the results of MRW Table I. So we are now satisfied that the replication has been successful. What can we conclude from this? As expected, we see that savings are positively correlated with the steady-state level, while $n+g+\delta$ is negatively correlated. And crucially, for the two samples with the most cross-country variation, they have $R^2$ values of 0.59. $R^2$ is a statistical measure regarding how much of a dependent variable the independent variables explain within the regression. This suggests that our two simple variables account for over half of the cross-country variation. 

But this isn't perfect either. Based on the restricted regression telling us $\frac{\alpha}{1-\alpha}=1.4880$, we can deduce that $\alpha=0.60$. This doesn't correspond with capital's share of income in practice - and so although easily observable variables may be able to account for a majority of the variation in real incomes, the basic Solow model is not up to scratch. 

It is here where MRW offer their specific contribution - they incorporate human capital as part of the model. Based on this, they produce two equations for per capita income to be estimated, assuming the share of income accruing to human capital $\beta$ to be between a third and a half. The first equation shows per capita income in relation to population growth and the accumulation of human and physical capital. The second involves substituting in the steady-state level of human capital. Because it is difficult to find data on human capital, MRW limit the scope solely to education and use a proxy of the average fraction of working-age population in secondary school.

$$ Y(t) = K(t)^\alpha H(t)^\beta [A(t) L(t)]^{1-\alpha-\beta} \; \text{where} \; 0 < \alpha + \beta < 1 $$

$$ \dot{k}(t) = s_k y(t) - (n+g+\delta)k(t) $$

$$ \dot{h}(t) = s_h y(t) - (n+g+\delta)h(t) $$

$$ \ln{[\frac{Y(t)}{L(t)}]} = \ln{A(0)} + gt + \frac{\alpha}{1-\alpha-\beta} \ln{(s_k)} + \frac{\beta}{1-\alpha-\beta} \ln{(s_h)} - \frac{\alpha + \beta}{1-\alpha-\beta} \ln{(n+g+\delta)} $$

$$ \ln{[\frac{Y(t)}{L(t)}]} =  \ln{A(0)} + gt + \frac{\alpha}{1-\alpha} \ln{(s_k)} + \frac{\beta}{1-\alpha} \ln{(h^*)} - \frac{\alpha}{1-\alpha} \ln{(n+g+\delta)} $$

We can go through a similar estimation process of doing both the unrestricted and restricted regressions for all three samples to produce the results of MRW's Table II. As evidenced by the $R^2$ values and coefficients, human capital is important and makes the Solow model able to explain nearly 80% of cross-country variation for the two meaningful samples. The implied $\alpha$ and $\beta$ values are both around one third, which seem reasonable. And so a simple proxy for human capital has made the Solow model an adept model for understanding differences in per capita income.

```
mrw7 <- lm(log(gdp85) ~ log(invest/100) + log((popgrowth/100) + 0.05) + log(school/100), data = nonoil)
mrw8 <- lm(log(gdp85) ~ log(invest/100) + log((popgrowth/100) + 0.05) + log(school/100), data = inter)
mrw9 <- lm(log(gdp85) ~ log(invest/100) + log((popgrowth/100) + 0.05) + log(school/100), data = oecd)
mrw10 <- lm(log(gdp85) ~ I(log(invest/100) - log((popgrowth/100) + 0.05)) + I(log(school/100) - log((popgrowth/100) + 0.05)), data = nonoil)
mrw11 <- lm(log(gdp85) ~ I(log(invest/100) - log((popgrowth/100) + 0.05)) + I(log(school/100) - log((popgrowth/100) + 0.05)), data = inter)
mrw12 <- lm(log(gdp85) ~ I(log(invest/100) - log((popgrowth/100) + 0.05)) + I(log(school/100) - log((popgrowth/100) + 0.05)), data = oecd)

```

<br>

But we aren't just interested in cross-country comparisons. One of the main criticisms of the Solow model at the time was that its predictions of convergence did not materialise. But to be clear, the Solow model only predicts the conditional convergence of countries with similar determinants of the steady state. And it offers an expression for how quickly this conditional convergence occurs in terms of the initial level of income and the steady state - this can be tested by using an expression where $y^*$ has been substituted in. To defend the Solow model, MRW test for convergence and conditional convergence from 1960 to 1985.

$$ \frac{d \ln{[y(t)]}}{dt} = \lambda [\ln{(y^*)}-\ln{(y(t))}] \; \text{where} \; \lambda = (n+g+\delta)(1-\alpha-\beta) $$

$$ \ln{(y(t))} = (1-e^{-\lambda t}) \ln(y^*) + e^{-\lambda t} \ln(y(0)) $$

$$ \ln{(y(t))} - \ln{(y(0))} = (1-e^{-\lambda t}) \frac{\alpha}{1-\alpha-\beta} \ln{(s_k)} + (1-e^{-\lambda t}) \frac{\beta}{1-\alpha-\beta} \ln{(s_h)} - (1-e^{-\lambda t}) \frac{\alpha+\beta}{1-\alpha-\beta} \ln{(n+g+\delta)} -  (1-e^{-\lambda t}) \ln(y(0)) $$

For the sake of brevity I am not going to list out the tests for all the samples. Instead, I will only show it for one sample per test. The results below are a snapshot of all of the results corresponding with Tables III, IV and V of MRW.

```
converge1 <- lm(I(log(gdp85)-log(gdp60)) ~ log(gdp60), data = nonoil)

summary(converge1)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.09784 -0.27467 -0.02826  0.25975  1.17747 

Coefficients:
            Estimate Std. Error t value Pr(>|t|)  
(Intercept) -0.26658    0.37960  -0.702   0.4842  
log(gdp60)   0.09431    0.04962   1.901   0.0603 .
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.4405 on 96 degrees of freedom
Multiple R-squared:  0.03627,	Adjusted R-squared:  0.02623 
F-statistic: 3.613 on 1 and 96 DF,  p-value: 0.06033

converge4 <- lm(I(log(gdp85)-log(gdp60)) ~ log(gdp60) + log(invest/100) + log(popgrowth/100 + 0.05), data = nonoil)

summary(converge4)

Residuals:
     Min       1Q   Median       3Q      Max 
-1.07648 -0.15215  0.01185  0.19595  0.96056 

Coefficients:
                          Estimate Std. Error t value Pr(>|t|)    
(Intercept)                1.91938    0.83367   2.302  0.02352 *  
log(gdp60)                -0.14090    0.05202  -2.709  0.00803 ** 
log(invest/100)            0.64724    0.08670   7.465 4.16e-11 ***
log(popgrowth/100 + 0.05) -0.30235    0.30438  -0.993  0.32311    
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.3507 on 94 degrees of freedom
Multiple R-squared:  0.4019,	Adjusted R-squared:  0.3828 
F-statistic: 21.05 on 3 and 94 DF,  p-value: 1.622e-10

converge7 <- lm(I(log(gdp85)-log(gdp60)) ~ log(gdp60) + log(invest/100) + log(popgrowth/100 + 0.05) + log(school/100), data = nonoil)

summary(converge7)

Residuals:
     Min       1Q   Median       3Q      Max 
-0.91041 -0.17599  0.01789  0.18439  0.93846 

Coefficients:
                          Estimate Std. Error t value Pr(>|t|)    
(Intercept)                3.02152    0.82748   3.651 0.000431 ***
log(gdp60)                -0.28837    0.06158  -4.683 9.62e-06 ***
log(invest/100)            0.52374    0.08687   6.029 3.30e-08 ***
log(popgrowth/100 + 0.05) -0.50566    0.28861  -1.752 0.083061 .  
log(school/100)            0.23112    0.05946   3.887 0.000190 ***
---
Signif. codes:  0 ‘***’ 0.001 ‘**’ 0.01 ‘*’ 0.05 ‘.’ 0.1 ‘ ’ 1

Residual standard error: 0.327 on 93 degrees of freedom
Multiple R-squared:  0.4855,	Adjusted R-squared:  0.4633 
F-statistic: 21.94 on 4 and 93 DF,  p-value: 8.987e-13
```
<br>

We can see that there is no tendency for absolute convergence, there is some tendency for conditional convergence when controlling for savings and population, and there is a strong tendency for conditional convergence when controlling for savings, population and human capital. A nice graphical description is given following the code. Indeed, we can create a nice graphical display of all of this. (Unlike MRW, I elected to use the 98 country sample instead of the 75 country one for the graphics.)

```
library(ggplot2)
library(gridExtra)

controlx1 <- lm(log(gdp60) ~ log(invest/100) + log(popgrowth/100 + 0.05), data = nonoil)
controlx1res <- residuals(controlx1)


controly1 <- lm(gdpgrowth ~ log(invest/100) + log(popgrowth/100 + 0.05), data = nonoil)
controly1res <- residuals(controly1)


controlx2 <- lm(log(gdp60) ~ log(invest/100) + log(popgrowth/100 + 0.05) + log(school/100), data = nonoil)
controlx2res <- residuals(controlx2)

controly2 <- lm(gdpgrowth ~ log(invest/100) + log(popgrowth/100 + 0.05) + log(school/100), data = nonoil)
controly2res <- residuals(controly2)


p1 <- ggplot(data = nonoil, mapping = aes(x=log(gdp60), y=gdpgrowth)) + geom_point() + geom_smooth(method = "lm") + labs(title = "A. Unconditional", x = "", y="")
p2 <- ggplot(data = nonoil, mapping = aes(x=(mean(log(gdp60))+controlx1res), y=(mean(gdpgrowth)+controly1res))) + geom_point() + geom_smooth(method = "lm") + labs(title = "B. Conditional on Savings and Population Growth", x = "", y="")
p3 <- ggplot(data = nonoil, mapping = aes(x=(mean(log(gdp60))+controlx2res), y=(mean(gdpgrowth)+controly2res))) + geom_point() + geom_smooth(method = "lm") + labs(title = "C. Conditional on Savings, Population Growth and Human Capital", x = "", y="")

grid.arrange(p1, p2, p3, ncol=1, top = "Unconditional versus Conditional Convergence", left = "% Growth Rate of GDP 1960-1985", bottom = "Log GDP per capita in 1960")
```

![Convergence](/assets/convergence.png){:width="675px"}

MRW go on to conclude by talking about interest rate differentials and capital movements, which while interesting, are not as relevant to the growth theories from the previous parts in the series. But hopefully this has illustrated some of the more theoretical aspects of Part I - and even if the paper is full of endogeneity issues and is rather outdated within the growth theory literature, it does gesture towards the idea that an augmented Solow model can be a useful and accurate description of growth in the real world. And perhaps more importantly, I could very easily have taken an updated dataset and applied the same statistical procedures to figure out for myself whether the claims of MRW hold true to this day - so this is a nice demonstration that as technical as economics can get sometimes, there is a lot of cool stuff you can do simply within the confines of your own home.





