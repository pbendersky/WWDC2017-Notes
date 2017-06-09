# 412 - Auto Layout Techniques in Interface Builder

## Changing Layout at runtime

- Collapsing a view at runtime.
  - Instead of changing the spacing, create a containing view and change its height, so there are no conflicts in IB.
- The order when deactivating and activating constraints is important. You get a message in the console if you don't.


## Tracking Touch

- Layout engine owns `frame`


## Supporting Dynamic Type

- Use Accesibility Inspector, choose simulator and change the font size from there.
- Vertical Baseline Standard Spacing (iOS 11)
  - Similar to Vertical Spacing but based on the text styles and selected fonts.
  - Should look better than a fixed spacing.

## Safe Areas

- Safe Area Layout Guide
  - Represents the safe area the view can use, accounting for larger navigation bars, overscan in tvOS, etc.
- When using iOS storyboards Constraints automatically upgrade

## Proportional Positioning

- Position something about 70% from the superview
- Use a UIView that size, and not render it.
  - Mark the UIView as hidden
  - Give it a name in the object library to recognize it
  - Add the constraints
  - iOS 11 - In the constraints you can targe the safe areas directly.

## Stack Views Adaptive Layout

- Standard spacing in UIStackView (iOS 11)
- Xcode 9 - Hidden property can vary by size classes
  - Works great with Stack View
  - Backwards deployable!
- Use Stack View whenever you can

