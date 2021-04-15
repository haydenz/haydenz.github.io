---
title: "Greeks2"
classes: wide
toc: true
toc_sticky: true
htmlwidgets: true
output: html_document
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



<script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
<div id="cd52e831-399a-403d-9bb2-0c56214b1d38" style="height: 100%; width: 100%;" class="plotly-graph-div"></div>
<script type="text/javascript">window.PLOTLYENV=window.PLOTLYENV || {};window.PLOTLYENV.BASE_URL="https://plot.ly";Plotly.newPlot("cd52e831-399a-403d-9bb2-0c56214b1d38", [{"type": "pie", "values": [4500, 2500, 1053, 500], "labels": ["Oxygen", "Hydrogen", "Carbon_Dioxide", "Nitrogen"]}], {}, {"linkText": "Export to plot.ly", "showLink": true})</script>

# Vanna and Skewness
Under risk neutrality assuption, $$S_t = \mathbb{E}_t[S_T], \forall t<T \implies \mathbb{E}[r]=0 $$.

$$\begin{aligned} \text{Skewness} &= \mathbb{E}[\frac{(r - \mathbb{E}[r])^3}{\sigma^3}]=\mathbb{E}[\frac{r^3}{\sigma^3}] \\ &= \frac{1}{\sigma^3}\mathbb{E}[r \cdot r^2]=\frac{1}{\sigma^3}Cov[r, r^2] \\ &= Corr[r, r^2]\frac{\sigma \sqrt{Var[r^2]}}{\sigma^3}=Corr[r, r^2]\frac{\sqrt{Var[r^2]}}{\sigma^2}\end{aligned}$$

Skewness is proportion to the correlation between underlying return $$r$$ and squared underlying return $$r^2$$, the latter of which is associated with volatility. 

# Delta and Implied Vol
FX option traders' convention: $$\sigma_{implied}(\Delta_t)$$ instead of $$\sigma_{implied}(K)$$. It is commonly used among interbank market, and still used in OTC market.

- $$ \sigma_{implied}(K) $$: Implied vol smile


```{r, out.width="50%", out.extra='style="background-color: #9ecff7; padding:10px; display: inline-block;"', eval=FALSE}
plot(10:1, pch=21, bg="red")
```

- Delta plots under different implied vol



 

# Appendix
## Notations
$$r = \ln(\frac{S_t}{S_0})$$


# References
Adam S. Iqbal, Volatility: Practical Options Theory (2018, Wiley)