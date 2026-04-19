# Workout Cards — Project Context for Claude Code

## What this is
A single-file offline web app (`index.html`) for generating home gym workouts on the fly.
Originally designed to simulate physical workout cards pulled from a box.
Built in vanilla HTML/CSS/JS — no frameworks, no dependencies, no build step.

## Deployment
- Hosted on GitHub Pages
- Single file: `index.html`
- Works fully offline except for YouTube form guide links

## How it works
- 4 exercise categories: **Aerobic**, **Core**, **Arms & Back**, **Legs & Glutes**
- Cards flip on tap to reveal description + reps + YouTube form guide link
- Cards can be selected (+ button) and added to a **My Workout** view
- My Workout shows selected exercises with category colour, reps, and form link
- Clear all button resets the workout selection

## User's equipment
- Bench with leg press, dip, and hip thrust attachments
- 2 × 7kg kettlebells
- 2 × fit balls
- Skipping rope
- Olympic weights + 10kg padded bar (for hip thrusts etc.)
- Resistance bands

## Exercise design rules
- All exercises must be **low injury risk**
- Exercises are chosen to support **mountain biking, skiing, and running**
- Every exercise must have a **YouTube link** for form reference
- Aerobic cards are intended for use **between sets or as a warm-up**
- Core focus is **anti-rotation and anti-extension** over sit-up style work

## Tech decisions
- Vanilla JS only — no React, no CDN dependencies
- All state managed in plain JS variables (flipped, selected, activeCat, mode)
- Full re-render on every state change via `render()` function
- CSS uses gradients and utility classes defined in `<style>` block
- Each category has a colour index (ci): Aerobic=0, Core=1, Arms & Back=2, Legs & Glutes=3

## Current exercise list
### Aerobic (ci=0)
1. Jump Rope — 30–60 sec
2. Box Step-Ups (Fast Pace) — 30 sec each leg
3. Kettlebell Swing — 15–20 reps
4. Jumping Jacks — 40–60 reps
5. Lateral Band Walks — 15 each direction
6. Mountain Climbers — 30–45 sec
7. Fit Ball Wall Squat — 45–60 sec hold
8. High Knees — 30–45 sec
9. Kettlebell Figure-8 — 30 sec

### Core (ci=1)
1. Dead Bug — 10 each side
2. Plank (Fit Ball) — 3 × 30–45 sec
3. Pallof Press (Band) — 10–12 each side
4. Fit Ball Rollout — 10–12 reps
5. Hollow Body Hold — 3 × 20–30 sec
6. Side Plank with Hip Dip — 10–12 each side
7. Bird Dog — 10 each side
8. Fit Ball Pike — 3 × 8–10 reps
9. Suitcase Carry (Kettlebell) — 20m each side

### Arms & Back (ci=2)
1. Dips (Bench Attachment) — 3 × 8–12 reps
2. Band Pull-Apart — 3 × 15–20 reps
3. Kettlebell Row (Single Arm) — 10–12 each side
4. Fit Ball Press-Up — 3 × 8–12 reps
5. Kettlebell Halo — 8 each direction
6. Face Pull (Band) — 3 × 15 reps
7. Kettlebell Press (Single Arm) — 3 × 8 each side
8. Bench Dip (Feet on Fit Ball) — 3 × 8–10 reps
9. Banded Bicep Curl — 3 × 12–15 reps

### Legs & Glutes (ci=3)
1. Hip Thrust (Barbell) — 3 × 10–12 reps
2. Bulgarian Split Squat — 8–10 each leg
3. Romanian Deadlift (Kettlebel
