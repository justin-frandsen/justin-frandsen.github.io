---
title: "Eye Tracking"
excerpt: "Setup, calibration, running sessions, and exporting data with the EyeLink 1000."
---

This page covers everything you need to run an eye-tracking session in the lab, from setup through data export. Our primary system is the **EyeLink 1000**, recorded and managed through **SR Research** software.

## Overview

Eye tracking lets us measure where and when participants look during a task. In our lab we primarily use it to study attentional guidance during visual search through naturalistic scenes. A typical session involves:

1. Preparing the participant and the room.
2. Calibrating and validating the tracker.
3. Running the experiment.
4. Exporting and backing up the data.

## Equipment

- **EyeLink 1000** (tower or desktop mount)
- Host PC (runs the EyeLink tracking software)
- Display/stimulus PC (runs PsychoPy / Psychtoolbox)
- Chin rest and forehead bar

## Setup

1. Power on the **Host PC** first, then the display PC.
2. Confirm the camera has a clear, unobstructed view of the participant's eye.
3. Seat the participant and adjust the chin rest so their eyes are level with the camera.
4. Adjust the camera focus and pupil/corneal-reflection thresholds until both are stable.

> **Tip:** Keep the room lighting consistent across participants. Changing light levels can affect pupil detection.

## Calibration & Validation

1. Run a **9-point calibration** from the Host PC.
2. Follow with a **validation** pass — aim for average error **< 0.5°** and max error **< 1.0°**.
3. If validation is poor, re-focus the camera and re-run calibration before starting the task.
4. Use **drift correction/check** between blocks to maintain accuracy.

## Running a Session

- Start recording from the experiment script (the display PC communicates with the Host PC via the EyeLink API).
- Monitor the live gaze cursor on the Host PC during the task.
- Watch for excessive blinks, drift, or loss of tracking, and re-calibrate if needed.

## Data Export

- Raw data is saved as **`.EDF`** files on the Host PC.
- Convert `.EDF` files with **EDF2ASC** or open them in **DataViewer** for interest-area and event analysis.
- Back up every `.EDF` to the lab server the same day it is collected.

## Troubleshooting

| Problem | Likely fix |
| --- | --- |
| Can't detect pupil | Re-focus camera; adjust pupil threshold; check lighting |
| Poor validation | Re-seat participant; re-run calibration; check chin rest height |
| Losing tracking mid-task | Add drift correction between blocks; check for glasses/eyelash occlusion |

## Resources

- [SR Research EyeLink documentation](https://www.sr-research.com/support/)

---

*Feel free to add new info at `_wiki/eyetracking.md`.*
