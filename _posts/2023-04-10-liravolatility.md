---
layout: post
title:  Can we catch the uncatchable? An attempt to capture Turkish Lira's hyper volatility! 
date: 2023-04-10 09:00:00
output:
  html_document:
    theme: cosmo
    highlight: tango
    self_contained: false
description: blog on the lira's volatility
tags: r-plot econometrics
categories: finance-posts
---


Saying that the Turkish lira experienced high volatility during the last decade would be an understatement. We can see why this is true if we compare the simplest variance measure, that is, the annualized standard deviation (sd) of the lira with other major currencies. From 2011 onwards, the lira's sd stands at **17.2%** compared to the Australian dollar's 10.4%, Swiss franc's 10.3%, Japanese yen's 9.04%, Euro's 8.5%, and Canadian dollar's 7.5%.

Like many other financial assets, we can analyze the lira's behavior through chartist's or fundamentalist's lenses. While it is quite tough to cover these two broad perspectives in this short blog, I will try to provide a glimpse of the overall situation.[^1] Fundamentalists make use of the expected changes in the economic variables to forecast asset prices. When it comes to the exchange rate, probably the most important macroeconomic variable is the short-term interest rate. To offset the financial uncertainty, interest rates are a natural choice as a policy instrument. And like other central banks, the Central Bank of the Republic of Turkey (CBRT) used it to control the free fall. Take the one-week repo rate between 2016 and 2018 as an example. It increased from 8% to 16.5% (850 bps) at the beginning of 2018 and eventually reached 24% by September 2018, following a 40% depreciation of the lira in mid-August. However, it got gradually reduced in the subsequent announcements. The lira kept receiving shocks, the worst of which came after the global pandemic. On the 20^{th} of December 2021, the lira’s nominal value against USD reached an all-time high of 18.4, decreasing to a closing value of 13.5 the next day. The government announced a scheme on the same day to curb the effects of dollarization. It was aimed to protect the lira deposits in the banks against fluctuations in foreign exchange markets. In the past, CBRT also used instruments like reserve option mechanism (ROM), required reserve ratio (RRR), and interest rate corridor (IRO), which were only partially successful. It should be noted that the central bank's policy tools are just a part of the larger picture.  It should be noted that the central bank's policy tools are just a part of the larger picture.  Simply the increase or decrease of the repo rates and reserve requirements won't control the shocks that may stem from supply and demand or other sources. Domestic and overseas capital movements, geopolitical uncertainty, or even economic uncertainty do play their respective roles. In a recent paper, I wrote as part of my Ph.D. research, it was found that economic policy uncertainty had an impact on volatility, specially long-run variance.  This brings us to the chartist point of view, which states that an asset's price movements may have an explanation
in its history. In the same paper, we modeled the Turkish lira's volatility with seven different classes of models having a total of 76 specifications. Our findings were really interesting from several perspectives. Firstly, we observed that to model the lira's volatility, model specifications that had non-gaussian distribution assumptions, provided comparatively decent results. Secondly, it isn't always necessary to have over complicated techniques to model a currency like a lira. For example, many simple specifications gave better estimates than fancy models that had jump components in them. In the final part of our study, we applied a support vector regression (SVR) to our variables. When the effectiveness of an estimate was checked, it showed that this issue depends highly on the proxy being used as a dependent variable. For example, when the range return (**RR**) of Parkinson's was used as a volatility proxy, estimates from range-based models were better able to explain the variation.  We share a part of our analysis in the bar graphs below to provide a brief idea regarding our findings. We used three proxies as dependent volatility measures, these are **RR**, **RV**, and **MASR**, given in Figures 1, 2, and 3, respectively.

 
<div>
  <iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~alishaikh1119/1.embed"></iframe>
</div>
*Note:* The code used to generate this graph is available at my GitHub [repository](https://github.com/mdalifaisal/blogs/tree/main/z-score)




**_Disclaimer:_** Some of the points highlighted in this blog are a part of the second chapter of my Ph.D. dissertation and a paper that I have co-authored with my supervisor Prof. Dr. Murat Donduran of Yildiz Technical University.

[^1]: In a future blog, I intend to cover the major theoretical and empirical models of the exchange rates and hopefully provide a map that provides a systematic picture of the information derived from the literature. This is such an interesting and important issue, that I feel it deserves a separate effort! 
