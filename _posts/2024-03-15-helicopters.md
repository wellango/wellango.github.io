---
title: 'Helicopter Noise'
date: 2023-03-15
permalink: /posts/2024/03/nyc-helicopters/
author_profile: false
tags:
  - New York City
  - Helicopters
---

<meta name="twitter:card" content="summary_large_image">
<meta name="twitter:title" content="Helicopters in NYC">

During the pandemic I started noticing an increasing number of helicopters hovering over New York City. Many other New Yorkers evidently also noticed the same and complained to the city's [311 service](https://portal.311.nyc.gov/article/?kanumber=KA-02267). The issue received a [lot](https://www.bloomberg.com/news/articles/2022-12-14/nyc-complaints-about-helicopter-noise-top-rat-complaints-in-some-parts-of-city) of [news](https://www.newyorker.com/magazine/2022/01/31/the-choppers-that-ate-new-york) [coverage](https://www.newyorker.com/magazine/2022/01/31/the-choppers-that-ate-new-york) and lawmakers have been [trying](https://www.northjersey.com/story/news/2023/04/24/menendez-pascrell-hope-to-get-faa-attention-on-helicopter-issues-through-budget/70135404007/) to [pass laws](https://nyc.streetsblog.org/2022/12/12/going-in-circles-laws-to-tame-helicopters-struggle-to-take-off) to address this. 

I wanted to dive into the data to see how the number of noise complaints have changed overtime and what could explain it.

An exponential increase in 311 calls
=======

The number of complaints about helicopter noise to the 311 service has been on a steady exponential rise since 2019, reaching an all-time high in December 2023 and shows no sign of slowing down. Between 2016 and 2018, the average number of calls about this problem was only 3 per day, now that number has skyrocketed to nearly 160 calls per day. The chart below illustrates the average number of complaints about helicopter noise filed with 311 between 2016 and 2023.

There are some seasonalities that can be observed in the data because fewer helicopters fly when there is rain or snow. While the majority of the complaints are from Manhattan, Queens and Brooklyn have been contributing to about 40% of the complaints over the last two years. 

What caused the increase in noise complaints?
=======

Here is a chart on one of the busiest days in the data (October 1st, 2021) where the different lines are different helicopter trips:

<iframe src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2021_10_01.html" title="Helicopters over Manhattan" width="950" height="775" style="border: none;"></iframe> 


Route change in Jersey City and Hoboken


Sometime in April 2022 FlyNYON helicopters from Linden mostly stopped flying over Newport, in Jersey City, and instead now fly over The Heights. 

<div style="float: left; margin-right: 2px;">
 <iframe src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2022_4_01_legend.html" frameborder="0" scrolling="no" width="105%" height="775"></iframe>
</div>

<div style="float: left;">
 <iframe src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2022_5_01_legend.html" frameborder="0" scrolling="no" width="105%" height="775"></iframe>
</div>

<div style="clear: both;"></div>





[^1]: The last year before the pandemic for which commuting data is available.

[^2]: I couldn’t figure out how to get data for those who work specifically in the CBD.

[^3]: The PATH and NJTransit to Penn Station and Port Authority Bus Terminal are all designed towards transporting people to the CBD.

[^4]: This includes anyone entering the CBD from New Jersey, not just New Jersey residents.

[^5]: Fall 2021 is the latest available data from NYMTC.

[^6]: Capital funding is money for structural improvements, new train cars; not for day-to-day operation costs of running the transit system.

[^7]:  NYC Transit, the agency that runs the subway and the buses in New York City, gets the remaining 80%.
