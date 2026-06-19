## 1. Work to date (June 19, 2026)
<br>

### A. Creation of a Multisite Megachurch database
<br>

As Scott Thumma's megachurch database is continuously updated, I took a snapshot in May 2026, on which I have based [my own database](mcdb_final_backup.xlsx) of multisite megachurches.
I spent over a month going to every single megachurch website (1666 in total), gathering the names of megachurch campuses, number of services offered, addresses, updating
churches who have changed their names or moved to a different denomination, and marking defunct churches where applicable. My updated database has 1579 active megachurches,
1770 satellite campuses, for a combined total of 3349 unique campus locations.
<br>

<br>


![](Figures%20and%20Graphs/Tables/top30_main_metro.png)
<br>

Based on my data, the top 30 US counties in terms of their megachurch presence. Metropole campuses are the main site/headquarters of a multisite megachurch organization,
as distinguished from single-campus megachurches (such as Lakewood Church in Houston, TX), who have no multicampus satellites. 

<br>

<br>

### B. Megachurches by county (Hartford database, 2001-2026)
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

Using the tigris, sf, [OSRM](https://github.com/riatelab/osrm) and tidygeocoder packages in R, I was able to attach lattitude/longitude coordinates to every campus.
I have mapped out the spatial distribution of megachurches and their campuses:
<br>

![](Figures%20and%20Graphs/megachurchmap1.png)
<br>

See [here](Figures%20and%20Graphs/megachurchmap2.png) for a view of main campuses only and [here](Figures%20and%20Graphs/megachurchmap3.png) for satellites only.
An interesting pattern can be observed in many areas with a megachurch presence -- the satellite campuses skew a bit more towards location in the urban periphery (this is
more easily visible when flipping between the main and satellite only versions). Single-campus and main campuses of multisite organizations
concentrate more heavily in urban metro core areas, while satellite campuses are less concentrated, but still distributed in and around suburban and exurban areas surrounding
the urban core.

<br>

### D. Urban-Rural classification
<br>

The apparent difference in distribution of main campuses versus multisite locaitons seen in the maps linked above suggest that multicampus expansion by megachurches favors suburban and exurban locations.
To look a bit closer at this I have joined my database with several databases that hold county-level information on all congregations 
and adherents (US Religion Census), population (USRC for 2010/2020, US Census Vintage 2025), and the CDC's Urban-Rural classification (NCHS).
Using this joined information I have produced a series of state-level maps which better demonstrate the urban-suburban nature of multisite locations:

<br>

![](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in.png)
<br>

See [here](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in_mains.png) for a view of main campuses only and [here](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in_sats.png) here for satellite campuses.
See [here](Figures%20and%20Graphs/NCHS%20Graphs) for additional maps of Arizona, California, Georgia, North & South Carolina, and Texas, as well as a map of the entire US (in 8K resolution!).

<br> 
Interesting patterns can be seen in the other states, such as in Harris County, TX, where satellite campuses are heavily clustered in the suburbs along the Hwy 290 corridor (Southwestern portion of the county), 
or in Southern California, where mains are heavily clustered in Los Angeles County, while satellites are heavily clustered in Orange County. Georgia displays an unsurprising pattern, with mains clustered in Fulton County (Atlanta), while satellites surround Atlanta in the metro area counties.
In Maricopa County, Arizona, which contains the bulk of the Phoenix metro area, mains and satellites are clustered densely along the I-10 and Hwy 60 corridors. 
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

