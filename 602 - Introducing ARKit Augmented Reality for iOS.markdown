# 602 - Introducing ARKit Augmented Reality for iOS

- A9 and up

- Tracking
  - Relative position of the device in the virtual environment
  - No external setup required
- Scene understanding
  - Plane detection
  - Hit testing
  - Light estimation

- ARSession
  - What kind of tracking you want
  - ARSessionConfiguration
  - -> ARFrame
  - Get the current ARFrame
  - Or be the delegate to receive new frames
  - ARWorldTrackingSessionConfiguration
    - 3 dimensions + 3 dimensions (relative position in the scene)
  - Availability
  
- This works if you have a texture rich environment. In a white wall, might not work as well, or if you have several moving objects.
- Delegate method to let you know the quality of the tracking has changed.
