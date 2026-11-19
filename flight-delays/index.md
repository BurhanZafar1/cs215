---
title: Seattle Flight Delays
---

# Seattle Flight Delays (2025)

[← Back to home](../)

For this project I used about 92,000 flights leaving Seattle (SEA) in 2025 from six airlines (Alaska, Delta, United, Southwest, American and JetBlue), from the U.S. Bureau of Transportation Statistics. I made interactive maps and charts with Plotly to see **where** flights go and **how late** they leave. Hover over any chart to see the numbers.

[See the full notebook (code + outputs)](Interactive_Plotly_Maps_Burhan.ipynb)

---

## 1. Where Alaska Airlines flies from SEA

Each dot is a destination. Bigger dots mean more flights, and the color shows the average departure delay.

<iframe src="charts/alaska_destinations_delays.html" width="100%" height="600" frameborder="0"></iframe>

Alaska's busiest routes are Anchorage (4,407 flights), LA, San Diego and Phoenix. The most on-time destination is Orange County/John Wayne (3.2 min average delay), and the worst are Honolulu (17.3 min), Sitka, Newark and SFO.

## 2. Flight paths

Same data, but as lines from SEA. Thicker, redder lines mean a bigger average delay.

<iframe src="charts/alaska_flight_paths.html" width="100%" height="600" frameborder="0"></iframe>

This one is better for showing *where* Alaska flies. The dot map is better for comparing delays, because long lines (like to Hawaii) look "heavier" just because they're long.

---

## 3. Delays by state

<iframe src="charts/state_delays.html" width="100%" height="850" frameborder="0"></iframe>

The worst states are Massachusetts (21.4 min), New Jersey (17.6), Hawaii (16.3) and New York (15.7). The best are Wisconsin (3.3), Minnesota (4.1) and Oklahoma (4.3). States with only one airport and a few hundred flights can look extra good or bad just by chance, so I trust the big ones like California (23,000+ flights, 9.0 min) more.

## 4. Delays by region and traffic

I grouped states into regions and into low/medium/high traffic.

<iframe src="charts/region_volume_dashboard.html" width="100%" height="550" frameborder="0"></iframe>

- **East** (MA, NJ, NY, PA, RI) is the worst at 16.6 min on average, then **Alaska & Hawaii** (13.4).
- The **Midwest** is the best (8.2 min).
- Busier states have *more* delay: 12.0 min for high-traffic states vs 8.7 for low-traffic ones.

The sunburst and treemap below show the same groups. Click a section to zoom in.

<iframe src="charts/region_sunburst.html" width="100%" height="750" frameborder="0"></iframe>

<iframe src="charts/state_treemap.html" width="100%" height="700" frameborder="0"></iframe>

---

## 5. Delays by month and airline

<iframe src="charts/carrier_month_heatmap.html" width="100%" height="550" frameborder="0"></iframe>

Summer is the worst for basically every airline. June–August are the reddest months, and JetBlue in July averaged almost 110 minutes late. Things calm down in September and October. Delta's row is blank after April because the data only has Delta flights for January–April.

## 6. Do bigger airlines have less delay?

<iframe src="charts/carrier_delay_regression.html" width="100%" height="500" frameborder="0"></iframe>

There's a slight downward trend (airlines with more flights have a bit less delay), but the R² is only 0.13 and there are only 6 airlines, so I wouldn't read much into it. JetBlue being so bad with so few flights pulls the line a lot.

---

**Data:** U.S. Bureau of Transportation Statistics (SEA departures, 2025), compiled for class. The airport locations come from a lookup table made with ChatGPT, so I'd double check those before trusting every dot.
