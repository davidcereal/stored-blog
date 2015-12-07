---
layout: page-fullwidth
title: "Exploring MTA Traffic Data"
meta_teaser: "When and where to take the subway if you don't like feeling completely harried by the end of your commute"
teaser: "When and where to take the subway if you don't like feeling completely harried by the end of your commute"
header: yes
image:
    thumb:  homepage_typography_thumb.jpg
    homepage: homepage_typography.jpg
    caption: Image by Antonio
    caption_url: "http://www.aisleone.net/"
categories:
    - blog
---
lAs any unfortunate New York City Metro Transit Authority rider can attest, one’s subway riding experience is directly dependent on how many other unfortunate riders are competing for walking space, standing room, polls, and —the holy grail—a seat.

Navigating through a crowded subway station can be quite disorienting, with other commuters crossing in front of you in all directions, and it is not uncommon to be shouldered aside for taking a moment to read a sign. And that is to say nothing of the actual ride itself. Suffice to say, a crowded NYC subway ride is nasty, brutish, and if you’re lucky, short. 

To my mind one of the surest ways of improving one’s day is to take the subway during a period of relative calm, rather than one of insanity. Accordingly, I was excited to use the MTA’s commuter traffic data to explore which stations and which times of day see the most riders. 

####The Data
The MTA keeps track of turnstile swipes at each of its stations, and usually bins the swipes into 4 or 3 hour intervals. I looked at all the entry swipes at all the turnstiles from November of 2014, when the MTA it updated its data storage scheme to its format, to September of 2015. 

To work with the data I used Pandas data structures in Python. I wanted to hone my skills working with data frames and dictionaries, and this project allowed me to do that. 

####Exploration
![graph]: https://github.com/dberger1989/dberger1989.github.io/blob/master/images/month_sums.pdf "Monthly Traffic"

At the monthly level, we see a significant number more people use the subway during the warm months than the colder ones.

This is pretty logical, as one would expect people to be more apt to adventure about the city when the weather is warm. This apparently outweighs the potential counter-effect of would-be riders opting to walk or bike when the weather is more pleasant.

I now submit to you a chart showing the total MTA entries per day:

![graph]: https://github.com/dberger1989/dberger1989.github.io/blob/master/images/top_days.pdf "Daily Traffic"

This graph should be somewhat intuitive. Weekdays are workdays, and this explains their almost 170% increase over the average weekend day.

We can also see which hours of the day see the most traffic:

![graph]: https://github.com/dberger1989/dberger1989.github.io/blob/master/images/top_hours.pdf "Hourly Traffic"

4-8pm sees the most traffic, as that is when commuters are likely to be heading home after work. Accordingly, the next highest period of traffic is from 8am-12pm. 

However, it was particularly interesting to note that this traffic to time of day pattern does not hold true for all stations. Lets use the 47-50th Street Rockefeller Plaza and 14th Street Union Square stations as examples:

![graph]: https://github.com/dberger1989/dberger1989.github.io/blob/master/images/14_ST-UNION_SQ_station_schedule.pdf "14th Street Traffic"

![graph]: https://github.com/dberger1989/dberger1989.github.io/blob/master/images/47-50_ST-ROCK_station_schedule.pdf "47-50th Street Traffic"


In both examples, the afternoon rush hours still sees the most traffic. But at 14th street, 8pm-midnight sees almost 60% more traffic than during the morning rush hours. 

47-50th Street sees the exact opposite relationship—the AM rush hours see more than 2.6X more traffic than the night hours of 10pm-midnight. 

This trend may be explainable by the fact that the 47th-50th street area is primarily business-oriented, as there are many office buildings in the area, but not too many bars and restaraunts, accounting for its low night time traffic numbers. Contrast this to 14th street, which has a busy night scene and many young NYU students in the area, making this explanation seem plausible. 

If you’re interested in seeing the time breakdown of your favorite subway station, feel free to check out the repo for this project on github. It includes time charts for the top 20 most used subway stations, and the code to examine all the stations for yourself. 

And what do the numbers for the top 20 most-used stations look like? Check it out for yourself below:

![Top 20 Stations]
(https://github.com/dberger1989/dberger1989.github.io/blob/master/images/top_stations.pdf)

With that, you now have some tools to avoid entering into a crowded subway station, and perhaps even get a seat on the subway! 







