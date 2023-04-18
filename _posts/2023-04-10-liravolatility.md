---
layout: post
title:  Can we catch the uncatchable? An attempt to capture Turkish Lira's hypervolatility! 
date: 2023-04-10 09:00:00
output:
  html_document:
    theme: cosmo
    highlight: tango
    self_contained: false
description: blog on lira's volatility
tags: r-plot econometrics
categories: finance-posts
---


Saying that Turkish lira experienced high volatility during the last decade would be an understatement. We can see why this is true if we compare the simplest variance measure, that is, the annualized standard deviation (sd) of lira with other major currencies. From 2011 onwards, lira's sd stands at **17.2%** compared to the Australian dollar's 10.4%, Swiss franc's 10.3%, Japanese yen's 9.04%, Euro's 8.5%, and Canadian dollar's 7.5%. 

In a future blog, I intend to cover the major theoretical and empirical models of the exchange rates and hopefully provide a map that provides a systematic picture for the overall information derived from the literature. This is such an interesting and important issue, that I feel it deserves a separate effort! 

As part of my study, I analyzed the volatility of Turkish lira through a set of different volatility models. 

<div>
  <iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~alishaikh1119/1.embed"></iframe>
</div>

**_Disclaimer:_** Some of the points highlighted in this blog are a part of the second chapter of my PhD dissertation and a paper that I have co-authored with my supervisor Prof. Dr. Murat Donduran of Yildiz Technical University.

*Note:* The code used to generate this graph is available at my github [repository](https://github.com/mdalifaisal/blogs/tree/main/z-score)
