# India at the Asian Games 2026: Power BI dashboard

A one-page Power BI dashboard on India's medals at the 20th Asian Games (Aichi-Nagoya 2026).

I wanted to answer two things: where do India's medals actually come from, and does more state funding mean more medals?

<img width="1530" height="857" alt="image" src="https://github.com/user-attachments/assets/b2fd801c-cf71-43a2-af15-10c98ccf24b7" />


Video walkthrough: LinkedIn 

## What's on the page

Five KPI cards across the top (gold, total medals, India's rank, women's share, medal points), then four charts. The gender and medal filters sit on the left with a reset button, and the chart titles change with whatever is selected.

Medal leaders by sport. One bar per sport, split into bronze, gold and silver. Athletics leads with 24 medals, then shooting with 15 and archery with 9. Cricket, golf, hockey and kabaddi have 2 each. Both filters change this chart.

Medal share by gender. A donut with the total medal count in the middle. At the moment it's 85 medals: men and women 44.71% each, mixed/open events 10.59%. The medal filter changes the split, and picking a gender narrows it to that gender.

Funding vs Glory. Bars are each state's funding and the line is the medals it won. This one is my own analysis at state level, so it doesn't react to the filters.

India vs Asian giants. A lollipop chart of India against China, Japan and South Korea. On total medals it reads China 341, Japan 269, South Korea 150 and India 85. Pick gold and it becomes 169, 83, 39 and 21. Only the medal filter moves it (more on that below).

## What I found

In Funding vs Glory, Gujarat sits at the top of the funding scale and has no medals. Haryana gets far less funding and has the most medals of the five states shown. In this data, more money didn't mean more medals.

## One modelling decision

The country medal table has one row per country, so it can't join to the main medals table, which only covers India by sport and gender. I didn't force a relationship. I wrote a measure that reads the medal filter directly, so the India vs Asian Giants chart reacts to the medal filter and ignores gender and sport. That's on purpose.

## Data

The data is real, and I checked it against the source before building anything. Sources: (list where the medal tables and the state funding figures came from).

I cleaned and modelled it in Power Query before it went into the dashboard.

## Built with

Power BI, Power Query, DAX

Open the .pbix file in Power BI Desktop (Windows only).
