# 230 - Advanced Animations with UIKit

## Basics

- `UIViewPropertyAnimator`

## Interactive and Interruptible Animations

- The user actions interactively drive the progress of the animation.
- Create an animator
  - On the touches handler
    - pauseAnimation
    - set fractionComplete based on the scrubber position
    - continueAnimation on .ended
    
- Interruptible
  - Scroll in safari, where you can stop the acceleration by tapping again.
  - Catch the animator mid-flight.
  

## New Property Animator behaviors

- .scrubsLinearly
- .pauseOnCompletion
  - Used in drag n drop
- You can start an animation before providing animation blocks.

- When interrupting sprint animations
  - Stop and create a new property animator
  - Consider critically damped spring without velocity

## Coordinating Animations

- Blur effect is animatable.

- View morphing
  - Scaling, translation and opacity blending of two views.
  - Compute .scale and .transform when animating
    - Dimentional ratio
  - 3 animators

## Tips & Tricks

- Animating corner radius
  - .cornerRadius is now animatable
    - Access to the layer's .cornerRadius within an animation block and it works.
  - CALayer .maskedCorners
    - Can provide the corners to mask.
- Delays in interactive animations (like UINavigationBar)
  - Keyframe animations
    - relativeStartTime, relativeDuration
  - Can use `UIView.addKeyFrame` within `UIViewPropertyAnimator` block.
- Additive Animations
  - Rotate a square
    - Decompose into several smaller additive rotation animations
    - Have a for inside `UIViewPropertyAnimator` block.
    - Each change to an animatable property will be chained.
