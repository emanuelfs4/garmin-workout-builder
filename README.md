# Garmin Workout Builder 🏃‍♂️🚴‍♂️🏊‍♂️

[![Live Demo](https://img.shields.io/badge/status-live%20demo-brightgreen)](https://emanuelfs4.github.io/garmin-workout-builder/)

**Garmin Workout Builder** is a sleek, modern web application designed to create, customize, calibrate, and export structured workouts directly into the Garmin-compatible JSON format. 

Whether you are configuring running intervals, cycling power thresholds, or swimming pool sessions, Garmin Workout Builder lets you map out your training blocks, preview them visually, and download or copy them instantly.

## 🚀 Live Web App
Access and use the tool directly in your browser without downloading anything:
👉 **[https://emanuelfs4.github.io/garmin-workout-builder/](https://emanuelfs4.github.io/garmin-workout-builder/)**

## Features

* **Multi-Sport Support:** Dedicated configuration profiles and template preset libraries for **Running**, **Cycling**, and **Swimming**.
* **GPX Workout Analyzer & Auto-Calibrator:** 
  * Upload your morning workout `.gpx` file directly in your browser.
  * Extract key performance metrics: **Distance, Moving Time, Average Pace, Elevation Gain, and Average Heart Rate** with informative descriptions on hover (`(i)`).
  * Interactive metric selection panel to check or uncheck the exact metrics you want to display and analyze.
  * Automatically calculates optimal training paces (like Zone 2 *Calibrated Easy* pace) to dynamically calibrate your upcoming workout intervals.
* **Visual Workout Preview Graph:** Real-time graphical visualization of your workout structure (Warmup, Intervals, Recoveries, Cooldowns) scaled dynamically relative to step durations with total estimated duration tracking.
* **Flexible Durations & Conditions:** Set intervals and steps in seconds, minutes, meters, kilometers, miles, or lap button triggers.
* **Advanced Pacing & Targets:** Input pace ranges in standard `min:sec` format (e.g., `4:15` to `4:30`), heart rate zones, power (watts), cadence, or speed.
* **Repeat Loops & Sub-steps:** Easily structure complex multi-step interval workouts with custom iteration loops.
* **Step Reordering & Customization:** Rearrange your workout blocks dynamically using up and down controls.
* **Instant Export:** Generate, copy, or download the official Garmin JSON payload with a single click.

## Usage & Importing to Garmin

1. Open the live app link above.
2. Choose your sport tab at the top.
3. *(Optional)* Upload your morning workout `.gpx` file to analyze performance metrics and automatically calibrate your target paces.
4. Select a template preset or build your workout manually.
5. Enter your workout name and customize your warmup, intervals, recovery loops, and cooldowns.
6. Check the live visual preview graph to verify your workout structure.
7. Click **Generate Garmin JSON** and download your `.json` file.
8. To import the generated JSON files into Garmin Connect, use the [Garmin Workout Importer Google Chrome Extension](https://chromewebstore.google.com/detail/faebbfokokipdpkbolpbpfadmgdbanpo?utm_source=item-share-cb).