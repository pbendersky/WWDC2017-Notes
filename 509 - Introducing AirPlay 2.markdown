# 509 - Introducing AirPlay 2

## Today

- Screen
- Audio
- Video

To an Apple TV or Speaker.

## AirPlay 2 (Audio)

- Wireless audio
- Multi-room playback with very tight sync
- Enhanced buffering on the speakers
- Multi-device control
  - Multiple devices can interact with the audio that is being streamed.

### Adoption

- Identify as long-form audio
  - Music, podcasts or audiobooks
  - Set `AVAudioSession` route sharing policy.
- Add an AirPlay picker
  - Allows users to route their content to AirPlay speakers without leaving the app.
  - `AVRoutePickerView`
  - `AVRouteDetector` to check if there are speakers available
- Integrate with MediaPlayer framework
  - Display the currently playing album art
  - Receive playback / pause commands from other devices on the network
  - `MPRemoteCommandCenter`
  - `MPNowPlayingInfoCenter`
- Adopt an AirPlay 2 playback APIs
  - Large audio buffering capacity on speakers
    - minutes, not seconds
  - Faster-than-real-time streaming to speakers
    - Robustnetss
    - More responsive playback
  - `AVPlayer` / `AVQueuePlayer`
    - Easier way, if you have an URL of the content.
  - `AVSampleBufferAudioRenderer` / `AVSampleBufferRendersynchronizer`
    - Harder way if you are preprocessing the content before sending it out.

### Advanced playback scenarios

### Availability

