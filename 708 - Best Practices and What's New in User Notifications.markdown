# 708 - Best Practices and What's New in User Notifications

## Hidden Content

- A way for users to hide private information in the notifications when it doesn't need to be seen.
- Extended support for third party apps (similar to messages)
  - Global setting for all notifications.
  - Customize privacy setting per app.
- API to customize how a hidden notification looks like.
  - Body placeholder can be modified (default: "Notification")
  - Private notifications are coalesced by thread identifier.
  - Placeholder can be a format string, where the first parameter is the number of notifications.
  - Can use a Strings Dictionary for singular / plural.
  - In the options, can select to show title and subtitle when content is hidden.
- Best practices
  - Retreive settings using `showPreviewSetting`
  - Use thread identifiers for the automatic coalescing.
  - Use string dictionaries for plurals and localization.

## Modifying content

- Using a service extension.
  - To download an image / video, or enhance the notificatin payload (like decrypting a message).
- Service extension can't drop the notification, it will be delivered.
- If you want to have more time to process, you can send a silent notification, and the app can then determine if it wants to present a local notification or not.

## Customizing rich notifications

- App specific look and feel.
- Custom display of notification content.
- Interactive and dynamic UI, so they can complete the notification without leaving.

- Content Extensions
  - Change the title.
  - Customize the content and the way its shown.
  - Can remove the default content.
  - Can specify a content size ratio in the extension's Info.plist

## User input customizations

- Content extension body does not allow touches.
- To customize use:
  - Media buttons
    - Override a few methods with the position, tintColor and type.
  - Actions
    - Intercept the action in the content extension or forward to the app.
  - Custom input views
    - You can show a custom UI instead of the keyboard.
      - `canBecomeFirstResponder` -> true
      - Override `inputView` to return it.
      - Call `self.becomeFirstResponder()` on `didReceive` in the `UNNotificationContentExtension`.
      