# GenLayer Portal - Custom Loading Spinner

A high-performance, lightweight custom loading animation designed specifically for the GenLayer Portal. Built with pure SVG vectors and seamless CSS animations, this component provides a consistent visual identity across all loading states and interface themes.



## Key Features

* GenLayer Identity: Features the sharp, centered GenLayer vector geometry.
* Seamless Infinite Loop: Engineered with pure linear frame transitions to eliminate keyframe reset stutters during continuous loading.
* Dual Theme Adaptability: Native support and optimized contrast for both Dark Interface (#0b0f17) and Light Interface (#ffffff).
* Scalability: Designed to remain legible and crisp at any dimension, from inline button loaders (24px) to full-page loading overlays (80px+).
* Zero Dependencies: Pure HTML/CSS/SVG implementation with zero external libraries, ensuring optimal runtime performance.

---

## Design and Motion Logic

The loading spinner utilizes a dual-ring differential motion system to represent validator consensus and state resolution across the GenLayer network.

1. Loading Page Animation
   - Outer Ring: Clockwise rotation at 3.0s duration
   - Inner Ring: Counter-clockwise rotation at 2.0s duration
   - Purpose: Visualizes initial network signal convergence and data processing.

2. Loading State Animation
   - Outer Ring: Clockwise rotation at 1.8s duration
   - Inner Ring: Clockwise rotation at 3.6s duration
   - Motion Ratio: 1:2 speed differential
   - Purpose: Visualizes active consensus building and transaction resolution.

---

## Setup & Integration Guide

### 1. Local Demo Setup
To run the live showcase locally:
```bash
git clone [https://github.com/keplr32b/Genlayer-Spinner.git](https://github.com/keplr32b/Genlayer-Spinner.git)
cd Genlayer-Spinner


2. Project Integration (HTML & CSS)
Copy and paste the HTML markup and CSS rules directly into your target codebase:
HTML Markup:

<div class="spinner-wrapper loading-page-spin">
  <svg class="ring-outer" viewBox="0 0 100 100">
    <circle cx="50" cy="50" r="45" fill="none" stroke="#00FF88" stroke-width="2" stroke-dasharray="10 20" />
  </svg>
  <svg class="ring-inner" viewBox="0 0 100 100">
    <circle cx="50" cy="50" r="35" fill="none" stroke="#00E5FF" stroke-width="2" stroke-dasharray="5 15" />
  </svg>
  <svg class="gl-logo-center" viewBox="0 0 100 100">
    <path d="M50 10 L 90 90 L 50 70 L 10 90 Z M50 30 L 35 70 L 65 70 Z" />
  </svg>
</div>


## CSS Styles & Keyframes:

.spinner-wrapper {
  width: 60px;
  height: 60px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-shrink: 0;
}

.ring-outer, 
.ring-inner {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0;
  left: 0;
}

.gl-logo-center {
  width: 25px;
  height: 25px;
  fill: currentColor;
  transform-origin: 50% 50%;
  position: relative;
  z-index: 2;
  animation: rotate-cw 4s linear infinite;
}

.loading-page-spin .ring-outer {
  animation: rotate-cw 3s linear infinite;
}
.loading-page-spin .ring-inner {
  animation: rotate-ccw 2s linear infinite;
}

.loading-state-spin .ring-outer {
  animation: rotate-cw 1.8s linear infinite;
}
.loading-state-spin .ring-inner {
  animation: rotate-cw 3.6s linear infinite;
}

@keyframes rotate-cw {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}

@keyframes rotate-ccw {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(-360deg); }
}
