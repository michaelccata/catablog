---
title: Street Meat
taxonomy:
    category: blog
date: 05/19/2016
---

**Courtney Kasuboski, a (now?) reader, asked where to find the best hotdog in the city.** Problem is, not many people are raving on social media about their $2 grab-and-gos. So, I had ask the opposite question: where are the ***worst*** street-vendors in the city?

**So, I turned to public health records.** Specifically, [311 Call Records](https://nycopendata.socrata.com/Social-Services/311-Service-Requests-from-2010-to-Present/erm2-nwe9) filed as "Food poisoning" from "Street Vendors".

**New York City keeps great records** and continues to develop and share with the [community](http://www1.nyc.gov/site/doitt/initiatives/open-data.page). After a quick query (see below) via their version of a SOAP URL (they call the language "SoQL" which is...cute?) we get around 750 results over the past 5 years.

<p>
    <iframe width='100%' height='520' frameborder='0' src='https://michaelcata.cartodb.com/viz/a7a00728-7e82-11e5-b3b6-0e8c56e2ffdb/embed_map' allowfullscreen webkitallowfullscreen mozallowfullscreen oallowfullscreen msallowfullscreen></iframe>
</p>

**The map's verdict? Avoid central Midtown and Fidi if you want to grab some food on the run.**

**It's not the most scientific study in the world.** We're relying heavily on self-reported cases of food-borne illness where people may misattribute their stomache ache for their most questionable meal of the day. Maybe they ate Chipotle right before? But the map should confirms your expectations. Midtown and FiDi are heavy traffic areas with lots of vendors and even more tourists. Turn-over's got to be high.

Here's to sticking with tacos next time you visit Court!

    https://data.cityofnewyork.us/resource/fhrw-4uyv.json?$select=borough,%20incident_zip,%20latitude,%20longitude%20&$where=complaint_type=%22Food%20Poisoning%22%20AND%20location_type=%22Food%20Cart%20Vendor%22&$limit=2500000
