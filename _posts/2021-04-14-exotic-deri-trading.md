---
title: "Greeks"
classes: wide
toc: true
toc_sticky: true
categories: 
  - Post
last_modified_at: 2021-04-15
tags:
  - structured product
  - financial engineering
  - black scholes
---

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

# Vanna and Skewness
Under risk neutrality assuption, $S_t = \mathbb{E}_t[S_T], \forall t<T \implies \mathbb{E}[r]=0 $.

$$\begin{aligned} \text{Skewness} &= \mathbb{E}[\frac{(r - \mathbb{E}[r])^3}{\sigma^3}]=\mathbb{E}[\frac{r^3}{\sigma^3}] \\ &= \frac{1}{\sigma^3}\mathbb{E}[r \cdot r^2]=\frac{1}{\sigma^3}Cov[r, r^2] \\ &= Corr[r, r^2]\frac{\sigma \sqrt{Var[r^2]}}{\sigma^3}=Corr[r, r^2]\frac{\sqrt{Var[r^2]}}{\sigma^2}\end{aligned}$$

Skewness is proportion to the correlation between underlying return $r$ and squared underlying return $r^2$, the latter of which is associated with volatility. 

# Delta and Implied Vol
FX option traders' convention: $\sigma_{implied}(\Delta_t)$ instead of $\sigma_{implied}(K)$. It is commonly used among interbank market, and still used in OTC market.


- $\sigma_{implied}(K)$: Implied vol smile

    using Plots, LaTeXStrings
    plotly()
    Plots.plot(1:4, [[1,4,9,16], [0.5, 2, 4.5, 8]], 
        labels = [L"\alpha_{1c} = 352 \pm 11 \text{ km s}^{-1}" L"\beta_{1c} = 25 \pm 11 \text{ km s}^{-1}"],
        xlabel = L"\sqrt{(n_\text{c}(t|{T_\text{early}}))}",
        ylabel = L"d, r \text{ (solar radius)}"
        )

- Delta plots under different implied vol
    var myChart = echarts.init(document.getElementById('main'));
    var chars = ['\u00BC', '\u00BD', '\u00BE', '\u2150', '\u2151', '\u2152'];
    var option = {
    xAxis: [{
        data: [0, 1, 2, 3, 4, 5],
        axisLabel: {
        formatter: (val, idx) => chars[parseInt(val)],
        }
    }],
    yAxis: [{}],
    series: [{
        name: 'Series',
        type: 'line',
        data: [5, 20, 36, 10, 10, 20]
    }]
    };

    myChart.setOption(option);


 

# Appendix
## Notations
$$r = \ln(\frac{S_t}{S_0})$$


# References
Adam S. Iqbal, Volatility: Practical Options Theory (2018, Wiley)