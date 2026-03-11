---
title: 'Building a True GPX Workout Analyzer'
date: 2026-03-12
permalink: /posts/2026/03/gpx-workout-analyzer/
tags:
  - Python
  - Data Visualization
  - Running
  - Cycling
---

If you track your runs or rides, you are probably familiar with the frustration of commercial fitness apps. 

You execute a perfectly structured workout—say, a 3km warmup followed by hard 1km repeats—and then upload it to Strava or Garmin. When you check your splits, the numbers look slightly... off. 

The app smoothed your GPS data. It averaged your pace second-by-second instead of calculating total distance over total time, artificially skewing your lap times. 

I wanted to see my raw, unadulterated telemetry data exactly how I ran or rode it. So, I built a tool to do it.

---

## The GPX Workout Analyzer

Below is a lightweight web application I built using Python and Streamlit. It runs entirely in your browser. 

You can upload your own `.gpx` file, select whether you were running or cycling, and input your exact interval structure (e.g., `3, 1, 1, 1` for a 3km warmup and three 1km repeats). It calculates your **true pace**, extracts your heart rate and cadence, and maps the telemetry across your custom segments.

*(Feel free to upload a file and test it out right here on the page!)*

<iframe 
  src="https://workout-splits.streamlit.app/?embed=true" 
  width="100%" 
  height="850" 
  style="border:none; border-radius: 8px; box-shadow: 0 4px 12px rgba(0,0,0,0.15);">
</iframe>

---

## How it works (The Math Fix)

Most commercial platforms calculate average pace by taking the arithmetic mean of your instantaneous pace at every GPS ping. Mathematically, taking an average of fractions (minutes/km) second-by-second skews the result. 

If you run fast for 10 seconds and slow for 10 seconds, the average of those two *paces* does not equal your true overall pace for that 20-second block. 

This script bypasses that completely. It parses the XML structure of the GPX file, aggregates the total distance and total time for the custom bounds you set, and applies a strict `Total Time / Total Distance` calculation to give you the mathematically true pace for that specific lap. 

Whether you are aiming for a sub-40 10k or just tracking your weekend long rides, having granular control over your own data is incredibly satisfying. 

**CHEERS**