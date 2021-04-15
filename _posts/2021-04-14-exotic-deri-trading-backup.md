---
title: "Greeks2"
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

    <script src="https://cdn.plot.ly/plotly-latest.min.js"></script>
    <div id="bc3146ac-70a8-4059-a4eb-ba96582b4c41" class="plotly-graph-div" style="height:100%; width:100%;"></div>
    <script type="text/javascript">window.PLOTLYENV=window.PLOTLYENV || {}; window.PLOTLYENV.BASE_URL="https://plot.ly"; Plotly.newPlot( "bc3146ac-70a8-4059-a4eb-ba96582b4c41", [{"name": "Vanilla Call Payoff", "type": "scatter", "x": [50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150], "xaxis": "x", "y": [0, 0, 0, 0, 0, 0, 10, 20, 30, 40, 50], "yaxis": "y"}, {"name": "Delta of High Vol", "type": "scatter", "x": [50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150], "xaxis": "x", "y": [0.01, 0.05, 0.12, 0.2, 0.3, 0.5, 0.7, 0.8, 0.88, 0.95, 0.99], "yaxis": "y2"}, {"name": "Delta of Low Vol", "type": "scatter", "x": [50, 60, 70, 80, 90, 100, 110, 120, 130, 140, 150], "xaxis": "x", "y": [0.01, 0.03, 0.08, 0.15, 0.24, 0.5, 0.76, 0.85, 0.92, 0.97, 0.99], "yaxis": "y2"}], {"yaxis": {"anchor": "x", "domain": [0.0, 1.0], "title": {"text": "<b>Payoff</b>"}}, "yaxis2": {"anchor": "x", "overlaying": "y", "side": "right", "title": {"text": "<b>Delta</b>"}}, "xaxis": {"anchor": "y", "overlaying": "x", "title": {"text": "<b>St</b>"}}}, {"linkText": "Export to plot.ly", "showLink": true}) </script>


# Appendix
## Notations
$$r = \ln(\frac{S_t}{S_0})$$


# References
Adam S. Iqbal, Volatility: Practical Options Theory (2018, Wiley)