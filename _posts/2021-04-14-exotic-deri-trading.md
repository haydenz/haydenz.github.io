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
Under risk neutrality assuption,
<img src="https://latex.codecogs.com/svg.latex?S_t = \mathbb{E}_t[S_T], \forall t<T \implies \mathbb{E}[r]=0"/><br/>

<img src="https://latex.codecogs.com/svg.latex?Skewness = \mathbb{E}[\frac{(r - \mathbb{E}[r])^3}{\sigma^3}]=\mathbb{E}[\frac{r^3}{\sigma^3}]=\frac{1}{\sigma^3}\mathbb{E}[r \cdot r^2]=\frac{1}{\sigma^3}Cov[r, r^2] \\ =Corr[r, r^2]\frac{\sigma \sqrt{Var[r^2]}}{\sigma^3}=Corr[r, r^2]\frac{\sqrt{Var[r^2]}}{\sigma^2}"/><br/>


# Appendix
## Notations
<img src="https://latex.codecogs.com/svg.latex? r = \ln(\frac{S_t}{S_0})"/><br/>
<img src="https://latex.codecogs.com/svg.latex? r = \ln(\frac{S_t}{S_0})"/><br/>


  Testing $$\alpha$$