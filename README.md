# Burhan Zafar — CS/Math 215: Intro to Data Science

Hi! I'm Burhan, and this is where I'm putting my work for CS/Math 215 at Whitman College (Fall 2026). I'll add my mini projects and final project here as the semester goes on.

## About this class
We use Python, pandas and Colab to clean, analyze and visualize real data, and also think about who makes data and why.

## Final Project Ideas

**Topic:** Sleep, exercise, weight and blood sugar in US adults.

I want to look at how sleep, physical activity, body weight and blood sugar are connected, and whether those connections look different for different groups of people (like different ages).

**Data:** The CDC's National Health and Nutrition Examination Survey (NHANES), 2017–2018. I'll merge five of its files: demographics, body measurements (for BMI), sleep, physical activity, and HbA1c (a blood test that shows average blood sugar over the last few months).

- **Pros:** real national health data, with actual measurements (weight, blood tests) and not just survey answers. All the files share an ID for each person, so they're easy to merge.
- **Cons:** lots of missing values, some variables are measured in weird ways, and NHANES uses survey weights, so my results won't perfectly represent the whole US unless I account for that.

**Questions I want to explore:**
1. **Sleep and weight:** Does BMI change for adults who sleep different amounts?
2. **Exercise and weight:** How does BMI look for people with different activity levels?
3. **Blood sugar:** How do HbA1c levels change across BMI categories and age groups?

**Tools:** pandas for cleaning and merging, matplotlib/seaborn (and maybe Plotly) for graphs.

This data only shows connections, not causes. If people who sleep less have a higher BMI, that doesn't mean less sleep *causes* weight gain.

## Projects
*Coming soon.*
