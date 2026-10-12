# Garmin Workout Builder 🏃‍♂️🚴‍♂️🏊‍♂️

[![Live Demo](https://img.shields.io/badge/status-live%20demo-brightgreen)](https://emanuelfs4.github.io/garmin-workout-builder/)

**Garmin Workout Builder** is a sleek, modern web application designed to create, customize, calibrate, and export structured workouts directly into Garmin-compatible JSON format. 

Whether configuring running intervals, cycling power thresholds, or swimming pool sessions, Garmin Workout Builder lets you map out training blocks, preview them visually, and import them directly into Garmin Connect with one click.

## 🚀 Live Web App
Access and use the tool directly in your browser without downloading anything:
👉 **[https://emanuelfs4.github.io/garmin-workout-builder/](https://emanuelfs4.github.io/garmin-workout-builder/)**

## Features

* **Multi-Sport Support:** Dedicated configuration profiles and template preset libraries for **Running**, **Cycling**, and **Swimming**.
* **Visual Workout Preview Graph:** Real-time graphical visualization of workout structure (Warmup, Intervals, Recoveries, Cooldowns) scaled dynamically relative to step durations with total estimated duration tracking.
* **Flexible Durations & Conditions:** Set intervals and steps in seconds, minutes, meters, kilometers, miles, or lap button triggers.
* **Advanced Pacing & Targets:** Input pace ranges in standard `min:sec` format (e.g., `4:15` to `4:30`), heart rate zones, power (watts), cadence, or speed.
* **Repeat Loops & Sub-steps:** Easily structure complex multi-step interval workouts with custom iteration loops.
* **Step Reordering & Customization:** Rearrange workout blocks dynamically using drag-and-drop or up/down controls.
* **1-Click Garmin Connect Importer:** Click **🚀 Import to Garmin Connect** to automatically copy the workout JSON payload to your clipboard, dispatch extension postMessage events, launch `connect.garmin.com` in a new tab, and display guided import instructions.
* **Intervals.icu Native Format & 1-Click Import:** 
  * Switch to the **⚡ Intervals.icu (Workout Text)** tab to generate clean, human-readable plain text adhering to the Intervals.icu workout syntax.
  * Click **⚡ Copy & Open Intervals.icu** to copy the formatted workout text straight to your clipboard and launch `intervals.icu`.
  * Seamlessly paste into your personal calendar or athlete coaching library to automatically populate structured workouts, pace ranges, and interval target charts.
  * Option to download as `.txt` for offline storage or manual uploading.
* **Garmin Device Binary (.FIT) Generator:**
  * Switch to the **💾 Garmin Device (.FIT Binary)** tab or click **💾 Download .fit** to generate and download native binary `.fit` workout files directly in the browser!
  * Fully compliant with the official Garmin FIT Protocol 2.0 (File ID 5: Workout):
    * Encodes exact min/max speeds in millimeters/second (`custom_target_value_low/high`), wattage for power, and heart rate zones.
    * Encodes native repeat loops (`repeat_until_steps_cmplt`) with cycle counts and jump targets.
    * 16-bit FIT CRC checksum validated for full hardware integrity.
  * **Direct Watch Install:** Connect your Garmin watch via USB, drop the `.fit` file into `GARMIN/Workouts/` (or `GARMIN/NewFiles/`), and your workout is instantly ready with native gauge needles and alerts!
  * Can also be directly uploaded to Intervals.icu, TrainingPeaks, or shared with athletes.
* **Universal Workout Importer (.FIT Binary, Garmin JSON & Intervals.icu Text):**
  * Click **📥 Import Workout** (or **📥 Import .fit** on the FIT tab) to upload, drag-and-drop, or paste existing workout files (`.fit`, `.json`, or `.txt`).
  * **Auto-Detects Format:** Seamlessly parses binary **Garmin Device `.fit` workout files**, Garmin Connect `.json` payloads, and **Intervals.icu plain-text / markdown workouts**!
  * **Decodes Binary FIT Workouts:** Decodes Global Message 26 (workout metadata) and Global Message 27 (workout steps), reconstructing warmup, cooldown, active, interval, recovery steps, repeat blocks (`repeat_until_steps_cmplt`), and pace/power/heart-rate/cadence targets with full precision.
  * Load and modify existing workouts, preview them on the visualizer graph, make adjustments, and generate updated Garmin JSON, Intervals.icu text, or binary `.fit` files!

## Usage & Importing

### Importing to Garmin Connect
1. Open the live app link above.
2. Choose your sport tab at the top (**Running**, **Cycling**, or **Swimming**).
3. Select a template preset, build your workout manually, or click **📥 Import Workout (.json)** to load a past workout.
4. Enter your workout name and customize your warmup, intervals, recovery loops, and cooldowns.
5. Check the live visual preview graph to verify your workout structure.
6. Click **🚀 Import to Garmin Connect**:
   * The workout JSON payload is automatically generated and copied to your clipboard.
   * Garmin Connect (`connect.garmin.com/modern/workouts`) opens automatically in a new tab.
7. On Garmin Connect, click the [Garmin Workout Importer Chrome Extension](https://chromewebstore.google.com/detail/faebbfokokipdpkbolpbpfadmgdbanpo?utm_source=item-share-cb) icon in your browser toolbar, paste the copied JSON, and save your workout!

### Importing to Intervals.icu
1. Click **Generate Workout** or switch to the **⚡ Intervals.icu (Workout Text)** tab.
2. Click **⚡ Copy & Open Intervals.icu**:
   * The Intervals.icu workout text is copied to your clipboard.
   * `intervals.icu` opens in a new tab with an interactive guidance modal.
3. On Intervals.icu, open your Calendar or Coaching Library, click **+ Add Workout**, and paste the text into the workout description box. Intervals.icu will immediately render your workout intervals and target power/pace graphs!

> [!NOTE]
> **Why does my Garmin Watch show "No Target" for Pace when synced from Intervals.icu?**
> Intervals.icu translates workouts to Garmin Connect using the Garmin Training API. For Garmin to receive pace targets:
> 1. In Intervals.icu **Settings → Sport Settings → Running**, your **Threshold Pace** must be set (e.g., `4:30 /km`). If unset, Intervals.icu drops pace targets and Garmin shows *No Target*.
> 2. In the workout dialog on Intervals.icu, verify the **Target** dropdown is set to **Pace** (or Auto).
> 3. If you already synced the workout prior to configuring your threshold, delete the workout from your calendar and re-add it to trigger a fresh export to Garmin Connect.
> 
> *Alternatively*, you can import directly into Garmin Connect using our **Garmin Connect (JSON)** tab and the Chrome extension, which uses native Garmin speed zones with full-screen gauge needles and alerts!

### Exporting Direct Binary (.FIT) to Garmin Watch
1. Select the **💾 Garmin Device (.FIT Binary)** tab or click **💾 Download .fit**.
2. Connect your Garmin watch to your computer with its USB charging/data cable.
3. Open your watch drive in your file manager (e.g. `GARMIN`).
4. Copy the downloaded `.fit` file directly into the **`GARMIN/Workouts/`** folder (or **`GARMIN/NewFiles/`**).
5. Unplug the watch. Your workout is instantly available under **Run/Bike > Training > Workouts** with 100% native gauge needles, sound alerts, and vibration prompts!
6. You can also upload this `.fit` file directly into Intervals.icu or TrainingPeaks.