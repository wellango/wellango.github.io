---
title: 'Changing trajectory of helicopter trips in New York City'
date: 2024-03-10
permalink: /posts/2024/03/nyc-helicopters/
author_profile: false
tags:
  - New York City
  - Helicopter Noise
---

During the pandemic I started noticing an increasing number of helicopters hovering over New York City. Many other New Yorkers evidently also noticed the same and complained to the city's [311 service](https://portal.311.nyc.gov/article/?kanumber=KA-02267). The issue received a [lot](https://www.bloomberg.com/news/articles/2022-12-14/nyc-complaints-about-helicopter-noise-top-rat-complaints-in-some-parts-of-city) of [news](https://www.newyorker.com/magazine/2022/01/31/the-choppers-that-ate-new-york) [coverage](https://www.newyorker.com/magazine/2022/01/31/the-choppers-that-ate-new-york) and lawmakers have been [trying](https://www.northjersey.com/story/news/2023/04/24/menendez-pascrell-hope-to-get-faa-attention-on-helicopter-issues-through-budget/70135404007/) to [pass laws](https://nyc.streetsblog.org/2022/12/12/going-in-circles-laws-to-tame-helicopters-struggle-to-take-off) to address this. 

I wanted to dive into the data to see how the number of noise complaints have changed overtime and identify potential factors that could explain it.

An exponential increase in 311 calls
=======

The number of complaints about helicopter noise to the city's 311 non-emergency complaint service, has been on a steady exponential rise since 2019. It reached an all-time high in December 2023 and the trend shows no sign of slowing. Between 2016 and 2018, the average daily call volume about this issue was merely 3. Now that number has skyrocketed to over 260 calls a day in December 2023. The graph below shows the average number of helicopter noise complaints reported to 311 from 2016 to 2023.

<p float="left">
  <img src="/images/helicopters-in-nyc/helicopter-complaints-nyc.png" width="99%" />
</p>

There are some seasonalities that can be observed in the data because helicopter trips are restricted when there is rain or snow. While the majority of the complaints are from Manhattan, Queens and Brooklyn have been contributing to about 40% of the complaints over the last two years as shown below.

<p float="left">
  <img src="/images/helicopters-in-nyc/helicopter-complaints-by-borough.png" width="99%" />
</p>


What caused the increase in noise complaints?
=======

ADS-B Exchange offers free public access to global air traffic data, from mid-2016, for the first day of every month. Additionally, the FAA maintains a database of all aircraft registered in the United States. All US aircrafts have a unique N-Number which is their registration number and its registration data can be accessed on the [FAA website](https://registry.faa.gov/aircraftinquiry/Search/NNumberInquiry).

Using the FAA database, I compiled a list of helicopters and filtered it to include only those that fly over Manhattan, since the majority of the noise complaints are from Manhattan. By utilizing the ADS-B data, I can plot the trajectories of these helicopters as they fly during this 24-hour period. 

Here is a chart on one of the busiest days in the data, October 1st, 2021, where the different lines are different helicopters (the chart is interactive and can be zoomed in and out):

<iframe src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2021_10_01.html" title="Helicopters over Manhattan" width="950" height="680" style="border: none;"></iframe> 

While I tried to gauge the frequency of helicopter trips over Manhattan using the available data, the analysis lacked significance because of the limited temporal scope of the data. As a single day’s worth of data is not representative of what happened over the whole month.

Since showing all the helicopters over the Manhattan airspace leads to a cluttered map, I tried to identify a group of helicopters that could be making frequent trips. I discovered that Stop The Chop, an advocacy group, had compiled a [list](https://stopthechopnynj.org/wp-content/uploads/2022/12/Helicopter-Tail-numbers-Dec-2022.pdf) of helicopters operating over New York City, along with annotations indicating their probable operators. They list FlyNYON as the most prominent tourist helicopter provider. So, I filtered the data to keep only these helicopters, and get their trajectories for the first day of each month.

Here are gifs showing FlyNYON helicopter trajectories on the first day of each month from 2021 to 2023.

<p float="left">
  <img src="/images/helicopters-in-nyc/flynyon_2021_full_gif.gif" width="99%" />
  <img src="/images/helicopters-in-nyc/flynyon_2022_full_gif.gif" width="99%" />
  <img src="/images/helicopters-in-nyc/flynyon_2023_full_gif.gif" width="99%" />
</p>

After analyzing the helicopter paths from the past three years, I noticed two interesting changes.


**Route change in Jersey City and Hoboken**

<div style="width:985px;">
  <div style="float:left;">
    <iframe width="490px" height="775px" src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2022_4_01_legend.html" scrolling="no" frameborder="0" allowfullscreen></iframe>
  </div>
  <div style="float:right;">
<iframe width="490px" height="775px" src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2022_5_01_legend.html" scrolling="no" frameborder="0" allowfullscreen></iframe>
  </div>
  <div style="clear:both;"></div>
</div>

In April 2022, FlyNYON helicopters departing from Linden had largely stopped flying over Newport in Jersey City. Instead they now fly over The Heights. 

**Route change in Upper West Side and Upper East Side**

<div style="width:985px;">
  <div style="float:left;">
    <iframe width="490px" height="775px" src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2022_9_01_legend.html" scrolling="no" frameborder="0" allowfullscreen></iframe>
  </div>
  <div style="float:right;">
<iframe width="490px" height="775px" src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_all_2022_11_01_legend.html" scrolling="no" frameborder="0" allowfullscreen></iframe>
  </div>
  <div style="clear:both;"></div>
</div>

Since November 2022, Central park helicopter tours have changed their route. After circling Central Park, the tours now turn back to the Upper West Side (UWS) instead of proceeding to the Upper East Side (UES) and crossing over to the East River.

These routes appear to be long-lasting, as evidence by the FlyNYON helicopter trajectories on Dec 1st of 2023:

<iframe src="https://wellango.github.io/images/helicopters-in-nyc/mapbox_trace_nyon_2023_12_01.html" title="Helicopters over Manhattan" width="950" height="775" style="border: none;"></iframe> 

Since this route causes each helicopter to go over UWS twice per trip, This could lead to doubling of helicopter noise complaints. We can see this in the 311 complaints data, where the number of complaints from the Upper West Side has more than doubled in 2023 compared to 2022.

<p float="left">
  <img src="/images/helicopters-in-nyc/helicopter-complaints-uws.png" width="99%" />
</p>

Since I couldn’t get helicopter trajectory data for every day of the month[^1], it is difficult to identify all the causes of the skyrocketing helicopter noise complaints in New York City. While I identified that factors such as an increase in helicopter tourism and changes in helicopter flight routes have contributed to the issue. People spending more time outdoors and being more cognizant of helicopter noise could also play a role.

Without legislation to address helicopter tourism, groups like Stop the Chop might want to investigate the reasons behind FlyNYON's decision to change their flight paths. This could be helpful in their lobbying efforts aimed at reducing the noise from helicopters in New York City.

[^1]: If someone can find me the data, I’m happy to do the analysis!

