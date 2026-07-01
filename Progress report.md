## Table of Contents

- [1. Work to date](#1-work-to-date)
  - [A. Multisite Megachurch Census](#a-multisite-megachurch-census)
  - [B. Megachurch county historical rankings (Hartford database, 2001-2026)](#b-megachurch-county-historical-rankings-hartford-database-2001-2026)
  - [C. Spatial distribution (based on my location data)](#c-spatial-distribution-based-on-my-location-data)
  - [D. Urban-Rural classification](#d-urban-rural-classification)
- [2. Next steps](#2-next-steps)
<br>
<br>

## 1. Work to date
<br>

### A. Multisite Megachurch Census
<br>

As Scott Thumma's megachurch database is continuously updated, I took a snapshot in May 2026, on which I have based my own census of multisite megachurches.
I spent over a month going to every single megachurch website (1666 in total), gathering data on multisite megachurches. My census includes:
<br>

* Names of megachurch satellite campuses
* Number of services offered
* Street addresses
* Geolocation coordinates
* Updated names & denominational information
* Marked defunct church organizations where applicable

My expansion of the Thumma/Hartford database has 1579 active megachurches,
1770 satellite campuses, for a combined total of 3349 unique campus locations.
<br>
<br>

#### Definitions
For the purposes of my census, a campus was defined as a discrete physical property (whether leased, borrowed, or owned by the church) where a church organization holds gatherings on a regular schedule (usually weekly), with a unique postal address. A **satellite campus** is an expansion location of a multisite megachurch organization (Such as Saddleback in California, or Life.Church in Pennsylvania), a discrete congregation that has a subordinate relationship with a metropole campus.
**Metropole campuses** are the main site/headquarters of a multisite megachurch organization, as distinguished from **single-campus** megachurches (such as Lakewood Church in Houston, TX), who have no multicampus satellites. 
<br>

A multisite location was counted as a campus if it holds services in a physically distinct location from its parent/mother church. I made operationalization/methodological decisions in counting satellite campuses in two other cases:
<br>

1. "Online" campuses (recordings or live streaming of a service)
2. "Spanish" or "Español" campuses (and sometimes, other languages) 
<br>

I made the decision not to count these as discrete campuses, as my ultimate goal with this study is to evaluate the impact that multisite church organizations have on the local religious ecology in areas where multisite expansions occur. Many churches list an "online" campus that is simply a link to a youtube page or live stream. The effect of online campuses is nearly impossible to gauge, as there are no reliable "attendance" figures available for online services, which would be the only metric by which they could be evaluated. I did not count separate language services as campuses, as many churches do on their website, if they do not meet in a discrete physical location separate from the main or other satellite campuses. In these cases, they were instead counted as another service at that particular location/campus. 
<br>

Churches that otherwise had no multisite locations, but claimed an "online" campus and/or a Spanish-language campus at the same location as the main service were not counted as multi-site organizations, but rather as single-campus organizations.
<br>

#### Top 30 multisite megachurch counties

![](Figures%20and%20Graphs/Tables/top30_main_metro.png)
<br>

Based on my data, the top 30 US counties in terms of their megachurch presence. 
<br>
<br>
<br>


### B. Megachurch county historical rankings (Hartford database, 2001-2026)
<br>

I have also compiled snapshots of the Hartford database going back to 2001:
<br>

![](Figures%20and%20Graphs/Tables/combined_wide.png)
<br>

This dataset does not include multicampus information.

<br>
<br>

### C. Spatial distribution (based on my location data)
<br>

Using the tigris, sf, [OSRM](https://github.com/riatelab/osrm) and tidygeocoder packages in R, I attached lattitude/longitude coordinates to every campus in my database.
I have mapped out the spatial distribution of megachurches and their satellite campuses:
<br>

![](Figures%20and%20Graphs/megachurchmap1.png)
<br>

See [here](Figures%20and%20Graphs/megachurchmap2.png) for a view of main campuses only and [here](Figures%20and%20Graphs/megachurchmap3.png) for satellites only.
<br>

An interesting pattern can be observed in many areas with a megachurch presence -- the satellite campuses skew a bit more towards location in the urban periphery (this is
more easily visible when flipping between the main and satellite only versions). Single-campus and main campuses of multisite organizations
concentrate more heavily in urban metro core areas, while satellite campuses are less concentrated, but still distributed in and around suburban and exurban areas surrounding
the urban core.

<br>

### D. Urban-Rural classification
<br>

The apparent difference in distribution of main campuses versus multisite locaitons seen in the maps linked above suggest that multicampus expansion by megachurches favors suburban and exurban locations.
This is not exactly surprising, but the sub/exurban choice of location for where megachurches plan much of their multicampus expansion does hint at possible strategic goals (whether conscious or unconscious) behind these choices.
To look a bit closer at this I have joined my database with several databases that hold county-level information on all congregations 
and adherents (US Religion Census), population (USRC for 2010/2020, US Census Vintage 2025), and the CDC's Urban-Rural classification (NCHS).
Using this joined information I have produced a series of state-level maps which better demonstrate the urban-suburban nature of multisite locations:

<br>

![](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in.png)
<br>

See [here](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in_mains.png) for a view of main campuses only and [here](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in_sats.png) here for satellite campuses.
See [here](Figures%20and%20Graphs/NCHS%20Graphs) for additional maps of Arizona, California, Georgia, North & South Carolina, and Texas, as well as a map of the entire US (in 8K resolution!).

<br> 

Interesting patterns can be seen in the other states, such as in Harris County, [Texas](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_texas.png), where satellite campuses are heavily clustered in the suburbs along the Hwy 290 corridor (Southwestern portion of the county), 
or in Southern [California](https://github.com/elizabethrushjohnson/Multisite-Megachurch-Project/blob/main/Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_california.png), where mains are heavily clustered in Los Angeles County, while satellites are heavily clustered in Orange County. [Georgia](https://github.com/elizabethrushjohnson/Multisite-Megachurch-Project/blob/main/Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_georgia.png) with mains clustered more loosely around Atlanta's urban core in Fulton, Cobb, and Gwinnett Counties (Atlanta), while satellites push further into the Atlanta exurban areas, especially Northeastern Gwinnett.
In Maricopa County, [Arizona](https://github.com/elizabethrushjohnson/Multisite-Megachurch-Project/blob/main/Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_az.png), which contains the bulk of the Phoenix metro area, mains and satellites are clustered densely along the I-10 and Hwy 60 corridors. 
<br>
<br>

Summary table of the NCHS-Census-USRC-multisite database join:

<br>

![](Figures%20and%20Graphs/Tables/summarystat_tab.png)

<br>
<br>


## 2. Next steps

At the moment, my data is insufficient to proceed on a study of the impact of multisite megachurch organizations. Using the Hartford
database as the basis for my study presents with a time-order problem. Since the US Religion Census, which will be my other
dataset, has waves every 10 years (2010, 2020), but the Hartford database is updated continuously, I must have the founding dates for
satellite campuses to make sure I am not introducing major errors introduced by including multisite campuses founded after 2020.
<br>

Unfortunately churches usually do not publish the founding dates of their main nor satellite campuses on their websites. 
The next phase of my project will be to use archive.org snapshots of megachurch websites to ascertain the 
founding dates of satellite campuses. 

<br>
<br>
<br>
<br>


*Last revision: July 1, 2026*
