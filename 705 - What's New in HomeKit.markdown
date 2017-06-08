# 705 - What's New in HomeKit

## Overview

- Allows apps to set up and control accessories. Central contorl for the configuration of your home. Accessories, rooms, automation, etc.
- Integrated in watchOS, iOS, tvOS.
- HomePod will also be home hub.

## Framework updates

### Event Triggers

- New events
  - HMSignificantTimeEvent
    - Sunrise
    - Sunset
      - Supports relative time offset (positive and negative).
  - HMCharacteristicTheresholdRangeEvent
    - Temperature raises to...
  - HMPresenceEvent
    - Don't run the air conditioner if no one is home.
    - Supported via HMPresenceEvent
    - Current user arrives home
    - Current user leaves home
    - Track a user instead of the device.
    - Last user leaves home.
    - First user arrives home.
  - Execute one, and auto disables after
    - Like an alarm.
- New conditions
  - User presence conditions
    - Don't execute the "Good morning" scene if no one's at home.
- End events
  - Available on HMEventTrigger
  - HMDurationEvent
    - Specify time interval from the trigger's execution time.
- Recurrencies
  - Only on certain days of the week.
- Mutable events
  - Simpler to update than before.

## Accessory updates

- 2014 session
- Specification was only accessible to MFi licensees. Starting today, specification available to anyone with a dev license.
- If you come up with a cool prototype.
  - Join the MFi program.
  - Go through self certification
  - http://developer.apple.com/mfi
- Scanning of QR Codes for setting up homekit accessories. Can be as small as 10mm x 10mm
- NFC tags for setup. Tap-to-pair.
  - Enhanced setup codes.
- HomeKit BLE
  - Broadcast notifications.
  - Secure broadcast sessions.
  - Lower latency, as it goes accessory-accessory instead of accessory-ATV-accessory
- Categories
  - Sprinklers and faucets
- Authentication
  - Software-based authentication!
  - Enables HomeKit on shipping accessories
- Self-Certification
  - Improved process and tools to help.
