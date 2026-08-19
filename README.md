# GenLayer Portal - Custom Loading Spinner

A high-performance, lightweight custom loading animation designed specifically for the GenLayer Portal. Built with pure SVG vectors and seamless CSS animations, this component provides a consistent visual identity across all loading states and interface themes.


## Key Features

* GenLayer Identity: Features the sharp, centered GenLayer vector geometry.
* Seamless Infinite Loop: Engineered with pure linear frame transitions to eliminate keyframe reset stutters during continuous loading.
* Dual Theme Adaptability: Native support and optimized contrast for both Dark Interface (#0b0f17) and Light Interface (#ffffff).
* Scalability: Designed to remain legible and crisp at any dimension, from inline button loaders (24px) to full-page loading overlays (80px+).
* Zero Dependencies: Pure HTML/CSS/SVG implementation with zero external libraries, ensuring optimal runtime performance.


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
