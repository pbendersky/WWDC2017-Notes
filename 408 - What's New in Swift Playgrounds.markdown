# 408 - What's New in Swift Playgrounds

## Playground book review

- Two file formats
  - Classic playgrounds, like Xcode
  - Playground books
    - Split into chapters, chapters into pages.
  - Contents.swift
  - LiveView.swift
  - Auxiliary files

## Enhacements for playground books

- Support for copying the code between pages, so you can continue with the work that has been done.
- Support for speed control, speed of execution.
  - Speed of step through in the code, as it executes in the liveview.
  - Can run faster / fastest
- It will now show runtime errors and highlight the line that made it crash.
- Users are now able to add / delete and duplicate pages.
- Support for new frameworks in iOS 11. Can now access the camera.
- Special markup in code comments to identify the code that can be copied and carried over.

- Speed controls
  - Pages can opt-in to run faster / run fastest.
  
- Template pages to support creating new pages in user editable books.
- Support for localization.

## New Bluetooth API for playgrounds

- PlaygroundBluetooth API.
- Full access to CoreBluetooth.
- PlaygroundBluetoothCentralManagerDelegate
  - Methods to manage / check connection status of accessories.
