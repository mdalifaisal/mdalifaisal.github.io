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

Like many other financial assets, we can analyze lira's behavior through chartist's or fundamentalist's lenses. While it is quite tough to cover these two broad perspectives in this short blog, I will try to provide a glimpse of the overall situation.[^1] Fundamentalists make use of the expected changes in the economic variables to forecast the asset prices. When it comes to exchange rate, probably the most important macroeconomic variable is the short-term interest rate. To offset the financial uncertainty, interest rates are a natural choice as a policy instrument. And like other central banks, the Central Bank of the Republic of Turkey (CBRT) used it to control the free fall. Take the one-week repo rate between 2016 and 2018 as an example. It increased from 8% to 16.5% (850 bps) at the beginning of 2018 and eventually reached 24% by September 2018, following a 40% depreciation of the lira in mid-August. However, it got gradually reduced in the subsequent announcements. The lira kept receiving shocks, the worst of which came after the global pandemic. On the 20^{th} of December 2021, the lira’s nominal value against USD reached an all-time high of 18.4, decreasing to a closing value of 13.5 the next day. The government announced a scheme on the same day to curb the effects of dollarization. It was aimed to protect the lira deposits in the banks against fluctuations in foreign exchaneg markets. In the past, CBRT also used instruments like reserve option mechanism (ROM), required reserve ratio (RRR), and interest rate corridor (IRO), which were only partially successful. It should be noted that the central bank's policy tools are just a part of the larger picture.  Simply the increase or decrease of the repo rates and reserve requirements won't control the supply and demand shocks. Domestic and overseas capital movements, geopolitical uncertainty, or even economic uncertainty do play their own rrespective roles.  
  


As part of my study, I analyzed the volatility of Turkish lira through a set of different volatility models. 

<div>
  <iframe width="900" height="800" frameborder="0" scrolling="no" src="//plotly.com/~alishaikh1119/1.embed"></iframe>
</div>
*Note:* The code used to generate this graph is available at my github [repository](https://github.com/mdalifaisal/blogs/tree/main/z-score)




**_Disclaimer:_** Some of the points highlighted in this blog are a part of the second chapter of my PhD dissertation and a paper that I have co-authored with my supervisor Prof. Dr. Murat Donduran of Yildiz Technical University.

[^1]: In a future blog, I intend to cover the major theoretical and empirical models of the exchange rates and hopefully provide a map that provides a systematic picture for the information derived from the literature. This is such an interesting and important issue, that I feel it deserves a separate effort! 
