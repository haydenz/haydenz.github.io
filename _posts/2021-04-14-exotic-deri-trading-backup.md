---
title: "Greeks2"
classes: wide
toc: true
toc_sticky: true
# htmlwidgets: true
# output: html_document
categories: 
  - Post
last_modified_at: 2021-04-15
tags:
  - structured product
  - financial engineering
  - black scholes  
---

<!-- mathjax -->

<script type="text/javascript" async
  src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-MML-AM_CHTML">
</script>

<!-- plotly -->
<!-- https://plotly.com/python/ -->


# Vanna and Skewness
Under risk neutrality assuption, $$S_t = \mathbb{E}_t[S_T], \forall t<T \implies \mathbb{E}[r]=0 $$.

$$\begin{aligned} \text{Skewness} &= \mathbb{E}[\frac{(r - \mathbb{E}[r])^3}{\sigma^3}]=\mathbb{E}[\frac{r^3}{\sigma^3}] \\ &= \frac{1}{\sigma^3}\mathbb{E}[r \cdot r^2]=\frac{1}{\sigma^3}Cov[r, r^2] \\ &= Corr[r, r^2]\frac{\sigma \sqrt{Var[r^2]}}{\sigma^3}=Corr[r, r^2]\frac{\sqrt{Var[r^2]}}{\sigma^2}\end{aligned}$$

Skewness is proportion to the correlation between underlying return $$r$$ and squared underlying return $$r^2$$, the latter of which is associated with volatility. 

# Delta and Implied Vol
FX option traders' convention: $$\sigma_{implied}(\Delta_t)$$ instead of $$\sigma_{implied}(K)$$. It is commonly used among interbank market, and still used in OTC market.

- $$ \sigma_{implied}(K) $$: Implied vol smile

    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
    <div id="25a6c0cd-8172-4064-adde-d675fc86323d" class="plotly-graph-div" style="height:100%; width:100%;"></div>
    <script type="text/javascript">window.PLOTLYENV=window.PLOTLYENV || {}; window.PLOTLYENV.BASE_URL="https://plot.ly"; Plotly.newPlot( "25a6c0cd-8172-4064-adde-d675fc86323d", [{"type": "scatter", "x": [50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150], "y": [25, 20, 16, 13, 11, 10, 9.5, 9.1, 8.8, 9, 9.2]}], {"linkText": "Export to plot.ly", "showLink": true}) </script>


- Delta plots under different implied vol



 

# Appendix
## Notations
$$r = \ln(\frac{S_t}{S_0})$$


# References
Adam S. Iqbal, Volatility: Practical Options Theory (2018, Wiley)