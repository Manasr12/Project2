# RotoScope Project README

## Overview
The RotoScope project is an advanced software tool for video editing and image manipulation. It implements techniques such as rotoscoping, image warping, and keying or color effects. This README provides in-depth insights into the project's functionalities, specifically the coding aspects of each effect.

## Categories and Effects

### I. Rotoscoping
Rotoscoping in this project involves frame-by-frame manipulation to create animations or effects.

#### Overlaying Items (Bird, Cowboy Hat, Eyes)
- **Code Functionality**: These methods overlay elements like birds, cowboy hats, and eyes onto the current image frame.
- **Implementation Details**:
  - **Pixel Iteration**: Loops through each pixel of the overlay images (`m_bird`, `m_cowboy`, `m_eyes`) and the current frame.
  - **Positioning**: Calculates the position for overlaying based on user interaction (click position).
  - **Boundary Checking**: Ensures the overlay does not exceed image boundaries.
  - **Alpha Blending**: Applies alpha blending to integrate the overlay smoothly with the underlying image.

### II. Image Warping
Image Warping allows for both linear and non-linear manipulation of image content.

#### Swirl Effect
- **Code Functionality**: Applies a twirl effect around a user-selected point in the image.
- **Implementation Details**:
  - **Twirl Radius Calculation**: Determines the radius within which the twirl effect is applied.
  - **Pixel Manipulation**: Adjusts the position of pixels within the radius to create a swirl pattern.
  - **Twisting Factor**: Applies a twisting factor based on the distance from the click point, creating the swirl effect.

#### Fisheye Warp
- **Code Functionality**: Distorts the image to simulate a fisheye lens effect.
- **Implementation Details**:
  - **Center Calculation**: Determines the center point for the fisheye effect.
  - **Radial Distortion**: Applies radial distortion to each pixel based on its distance from the center.
  - **Pixel Remapping**: Remaps each pixel's position to create the fisheye effect.

### III. Keying or Other Color Effects
Keying involves blending two images based on computed alpha values.

#### Green/Blue Screen Effect
- **Code Functionality**: Implements chroma keying for green/blue screen effects.
- **Implementation Details**:
  - **Color Analysis**: Analyzes each pixel's color to determine its contribution to the foreground or background.
  - **Alpha Calculation**: Uses the Vlahos method to calculate alpha values for blending.
  - **Image Blending**: Blends the foreground and background images based on the computed alpha values.

#### Clamping Function
- **Code Functionality**: Ensures values stay within a specified range.
- **Implementation Details**:
  - **Boundary Enforcement**: Clamps values to stay within minimum and maximum limits.
  - **Usage in Alpha Calculation**: Particularly used in alpha value calculations to maintain realistic transparency levels.
