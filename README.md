# Garmin Workout Builder 🏃‍♂️🚴‍♂️🏊‍♂️

[![Live Demo](https://img.shields.io/badge/status-live%20demo-brightgreen)](https://emanuelfs4.github.io/garmin-workout-builder/)

**Garmin Workout Builder** is a sleek, modern web application designed to create, customize, calibrate, and export structured workouts directly into Garmin-compatible JSON format. 

Whether configuring running intervals, cycling power thresholds, or swimming pool sessions, Garmin Workout Builder lets you map out training blocks, preview them visually, and import them directly into Garmin Connect with one click.

## 🚀 Live Web App
Access and use the tool directly in your browser without downloading anything:
👉 **[https://emanuelfs4.github.io/garmin-workout-builder/](https://emanuelfs4.github.io/garmin-workout-builder/)**

## Features

* **Multi-Sport Support:** Dedicated configuration profiles and template preset libraries for **Running**, **Cycling**, and **Swimming**.
* **GPX Workout Analyzer & Auto-Calibrator:** 
  * Upload your morning workout `.gpx` file directly in your browser.
  * Extract key performance metrics: **Distance, Moving Time, Average Pace, Elevation Gain, and Average Heart Rate** with informative hover descriptions (`(i)`).
  * Interactive metric selection panel to check or uncheck exact metrics for analysis.
  * Automatically calculates optimal training paces (like Zone 2 *Calibrated Easy* pace) to dynamically calibrate upcoming workout intervals.
* **Visual Workout Preview Graph:** Real-time graphical visualization of workout structure (Warmup, Intervals, Recoveries, Cooldowns) scaled dynamically relative to step durations with total estimated duration tracking.
* **Flexible Durations & Conditions:** Set intervals and steps in seconds, minutes, meters, kilometers, miles, or lap button triggers.
* **Advanced Pacing & Targets:** Input pace ranges in standard `min:sec` format (e.g., `4:15` to `4:30`), heart rate zones, power (watts), cadence, or speed.
* **Repeat Loops & Sub-steps:** Easily structure complex multi-step interval workouts with custom iteration loops.
* **Step Reordering & Customization:** Rearrange workout blocks dynamically using drag-and-drop or up/down controls.
* **1-Click Garmin Connect Importer:** Click **🚀 Import to Garmin Connect** to automatically copy the workout JSON payload to your clipboard, dispatch extension postMessage events, launch `connect.garmin.com` in a new tab, and display guided import instructions.

## Usage & Importing to Garmin

1. Open the live app link above.
2. Choose your sport tab at the top (**Running**, **Cycling**, or **Swimming**).
3. *(Optional)* Upload your morning workout `.gpx` file to analyze performance metrics and automatically calibrate your target paces.
4. Select a template preset or build your workout manually.
5. Enter your workout name and customize your warmup, intervals, recovery loops, and cooldowns.
6. Check the live visual preview graph to verify your workout structure.
7. Click **🚀 Import to Garmin Connect**:
   * The workout JSON payload is automatically generated and copied to your clipboard.
   * Garmin Connect (`connect.garmin.com/modern/workouts`) opens automatically in a new tab.
8. On Garmin Connect, click the [Garmin Workout Importer Chrome Extension](https://chromewebstore.google.com/detail/faebbfokokipdpkbolpbpfadmgdbanpo?utm_source=item-share-cb) icon in your browser toolbar, paste the copied JSON, and save your workout!