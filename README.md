# RotoScope Project README

## Overview
The RotoScope project is an advanced software tool for video editing and image manipulation, implementing various techniques such as rotoscoping, image warping, and keying or color effects. This README provides detailed insights into the project's functionalities, focusing on the coding aspects of each effect in the Rotoscoping category.

## Categories and Effects

### I. Rotoscoping
Rotoscoping in this project involves frame-by-frame manipulation to create animations or effects.

#### Phaser (Laser-like Weapon)
- **Code Functionality**: This code adds a laser-like effect, represented as a Phaser, onto the video frames.
- **Implementation Details**:
  - **Initial Image Copying**: The process begins by copying the initial image to the current frame.
  - **Overlaying Phaser**: Iterates over user-clicked points (`m_draw`) where the Phaser should appear.
  - **Positioning and Alpha Blending**: For each clicked position, the Phaser image is placed with alpha blending, ensuring it appears seamlessly integrated into the scene.

#### Cowboy Hat
- **Code Functionality**: The code overlays a cowboy hat image onto the video frames.
- **Implementation Details**:
  - **Copying Base Image**: Similar to the Phaser, it starts by preparing the base frame.
  - **Calculating Hat Position**: Adjusts the clicked position to center the cowboy hat image over it.
  - **Overlaying the Hat**: Checks boundaries and alpha values to overlay the cowboy hat image, blending it with the current frame.

#### Bulging Eyes
- **Code Functionality**: Overlays an exaggerated eyes image onto the video frames.
- **Implementation Details**:
  - **Initial Image Copying**: Copies pixel data from an initial image to the current working image.
  - **Overlaying Eyes**: Iterates over user-clicked points and calculates the position for overlaying the eyes image.
  - **Applying the Overlay**: Ensures boundary checks and alpha value conditions to blend the eyes image seamlessly.
  - **Updating Views**: Refreshes the display to show the updated frame with the bulging eyes effect.

#### Draw Red Lines (Outlined Drawings)
- **Code Functionality**: This segment of code is responsible for drawing red lines or squares around certain points in the video, typically used for outlining characters or objects.
- **Implementation Details**:
  - **Base Image Preparation**: Similar to other effects, it starts by copying the initial image to the current working image.
  - **Iterating Over Points**: Loops through a list of points (`m_draw`) where the red outlines should be drawn in the current frame (`m_movieframe`).
  - **Drawing Red Squares**: For each point, it draws a 30x30 red square around the point. This is achieved by iterating through a 30x30 pixel area centered on the point.
  - **Boundary Checks**: Ensures that the drawing does not exceed the image boundaries.
  - **Color Setting**: Sets the color of the selected pixels to red (255, 0, 0) to create the red outline.

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
