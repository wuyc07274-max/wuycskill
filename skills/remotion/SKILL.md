---
name: "remotion"
description: "Best practices and guide for Remotion - programmatic video creation in React"
---

# Remotion - Video Creation in React

Comprehensive skill set for creating programmatic videos using Remotion, a framework for creating videos programmatically using React.

## When to Use
Use when dealing with Remotion code for:
- Creating video compositions with React components
- Animating elements using frame-based animations
- Working with audio, video, and image assets
- Building charts and data visualizations
- Implementing text animations and captions
- Using 3D content with Three.js
- Applying transitions and sequencing
- Integrating Tailwind CSS and Lottie animations

## Core Concepts
Remotion uses React components to define video frames. Each frame is a snapshot of the component tree at a given time index.

## Key APIs
- `useCurrentFrame()` — Get current frame index
- `useVideoConfig()` — Get video configuration (durationInFrames, fps, width, height)
- `<Composition>` — Define a video composition
- `<Sequence>` — Time-shift nested components
- `interpolate()` — Map frame values to animation values
- `spring()` — Physics-based animations
- `<Audio>` / `<Video>` — Media elements
- `<Img>` — Optimized image element

## Dependencies
- remotion >= 4.0.0
- react >= 18.0.0
