# Multisite Megachurch Project
<br>
This repository is intended to share my progress on my master's thesis project, 
a study of American megachurches (Protestant congregations with 2000 or more weekly attendance) 
and their satellite campuses, and the impact that they have on local church density. 
<br>
<br>

## Introduction

The narrow goal of this project is a desire to examine the "Wal-Mart effect" that megachurches have on local 
Protestant Christian congregations, and examine the impact of a more recent trend in the ecclesial 
ecology of the megachurch phenomenon -- the emergence of "multicampus" or "multisite" megachurches. 
These multisite megachurches open satellite campuses, who typically (though not always) livestream the 
sermon or entire service from the main campus. This form of expansion has allowed a new avenue
of expansion for megachurches beyond the construction of larger and larger buildings and main
campuses. This model emerged in the mid-2000's and rapidly proliferated throughout the 2010's. Today,
roughly 1/3 of organizations identified as megachurches (by the Hartford Institute) possess at least
one multicampus expansion site. This phenomenon exists within an overarching trend in American
Protestant church attendance since the 1970's into larger, fewer churches, concentrating more heavily
in the top 1% and top 10% of churches by attendance.

The aim of my research is to establish the multsite megachurch within conceptions of
a competitive religious marketplace, one in which churches not only compete with one another,
but also with the secular. In more simple terms, American churches are competing not only with 
nearby congregations of a similar theological tradition, but also with shopping malls, Sunday morning
NFL games, and (perhaps the greatest secular competitor!) marginal interest in religious activity.

The broader context of my research is the interdisciplinary intersection of sociology of religion and
economics known as "religious economics." Research in this subfield has been overly-influenced
by neoclassical conceptions of markets and competition. My desire with this project is to broaden the theoretical horizon of religious economics. 

Megachurches and multisite organizations did not arise spontaneously or purely from organizational innovation, 
but must be understood as a product of the American macroeconomic conditions. Just as corporations and individuals 
must grapple with the economic  realities of their own political-economic context in a competitive marketplace, 
churches must do so as well, competing for money and volunteer time. These two resources come from a single 
source -- parishioners, and are a finite and dwindling resource in the United States. I believe that both 
megachurches and their organizational evolution into multisite organizations represent a response to the 
confluence of declining religious activity participation and macroeconomic conditions starting in the 1970's 
and continuing through the present day that have depressed congregants' ability to donate both time and money.

My project is inspired by the work of Mark Chaves on megachurches and church concentration (especially [Chaves 2006](https://www.jstor.org/stable/20058102)),
and the work of Jörg Stolz (who is also one of my supervisors on my thesis) on secular-religious competition. I am also grateful for Scott Thumma who has maintained the Hartford
Institute's [megachurch database](https://hirr.hartfordinternational.edu/research/megachurch-database/) for over 30 years. My project owes a great deal to the 
[2011 paper](https://doi.org/10.1007/s13644-011-0009-2) by Wollschleger & Porter, who first showed the "Wal-mart" effect of megachurches, in the context of a nuanced
understanding of religious markets.
<br>
<br>

## 1. Work to date
<br>

### A. Creation of a Multisite Megachurch database
<br>

As Scott Thumma's megachurch database is continuously updated, I took a snapshot in May 2026, on which I have based [my own database](mcdb_final_backup.xlsx) of multisite megachurches.
I spent over a month going to every single megachurch website (1666 in total), gathering the names of megachurch campuses, number of services offered, addresses, updating
churches who have changed their names or moved to a different denomination, and marking defunct churches where applicable. My updated database has 1579 active megachurches,
1770 satellite campuses, for a combined total of 3349 unique campus locations.
<br>

<br>

### B. Megachurches by county (Hartford database, 2001-2026)
<br>

I have also compiled snapshots of the Hartford database going back to 2001:
<br>
![](Figures%20and%20Graphs/Tables/combined_wide.png)

<br>
<br>

### C. Spatial distribution (based on my location data)
<br>

Using the tigris, sf, [OSRM](https://github.com/riatelab/osrm) and tidygeocoder packages in R, I was able to attach lattitude/longitude coordinates to every campus.
I have mapped out the spatial distribution of megachurches and their campuses:
<br>

![](Figures%20and%20Graphs/megachurchmap1.png)
See [here](Figures%20and%20Graphs/megachurchmap2.png) for a view of main campuses only and [here](Figures%20and%20Graphs/megachurchmap3.png) for satellites only.
An interesting pattern can be observed in many areas with a megachurch presence -- the satellite campuses skew towards location in the urban periphery (this is
more easily visible when flipping between the main and satellite only versions).

<br>

### D. Urban-Rural classification
<br>

I have joined my database with several databases with county-level information on all congregations and adherents (US Religion Census), population (USRC for 2010/2020, US Census Vintage 2025), and the CDC's Urban-Rural classification (NCHS).
Using this joined information I have produced a series of state-level maps which better demonstrate the urban-suburban nature of multisite locations:

<br>

![](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in.png)
See [here](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in_mains.png) for a view of main campuses only and [here](Figures%20and%20Graphs/NCHS%20Graphs/nchs_map_il_in_sats.png) here for satellite campuses.
See [here](Figures%20and%20Graphs/NCHS%20Graphs) for additional maps of Arizona, California, Georgia, North & South Carolina, and Texas, as well as a map of the entire US (in 8K resolution!).

<br> 
Interesting patterns can be seen in the other states, such as in Harris County, TX, where satellite campuses are heavily clustered in the suburbs along the Hwy 290 corridor (Southwestern portion of the county), 
or in Southern California, where mains are heavily clustered in Los Angeles County, while satellites are heavily clustered in Orange County. Georgia displays an unsurprising pattern, with mains clustered in Fulton County (Atlanta), while satellites surround Atlanta in the metro area counties.
In Maricopa County, Arizona, which contains the bulk of the Phoenix metro area, mains and satellites are clustered densely along the I-10 and Hwy 60 corridors. 
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

