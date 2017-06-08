# 201 - What's new in Cocoa Touch

## Productivity

### Drag and Drop

- To make dragable, create a UIDragInteraction (similar to a UIGestureRecognizer)
  - Customize lift animation, previews
- To enable drop, create a UIDropInteraction. Attach to the superview that receives the dropped items.
  - Update UI as drag moves
  - Receive data on drop
  - Customize drop animation
- Built-in support in TableView, CollectionView, TextView
- Integration with UIPasteConfiguration. Pastes can receive drags.

### File Management

- New documents view controller.
- Coordinate access of files. NSFileCoordinator or UIDocument.

## UI refinements

### Navigation Bar

- Large title on navigation bars with integrated search field.
- As you scroll top, the search bar and large title collapse into the old style.
- Not a lot of work to do in most times.
- Opt in `prefersLargeTitle` in UINavigationBar
- `largeTitleDisplayMode` in UINavigationItem
- You can add Search controller to navigation item.
- Guidance
  - use large title on the first level.
  - Subsequent might use small titles
- UIRefreshControl integrated in the new navigation bar.
- Title is part of the navigation bar, not the content view. Navigation bar starts larger, and changes height.
- safeAreaInsets.top / .bottom -> Safe area of the content view, so we can set the insets of content views.

### Table View

- Swipe actions `UIContextualAction`. Automatically be invoked when you swipe across like mail.
- Don't make it the only way to perform a particular action.


## API enhancements

- Archiving native swift types -> `Codable` protocol
- Key pats -> Literal syntax with `\Presenter.copresenter.name`
- Users expects to be able to swipe from the edge, regardless of status bar visibility.
  - Now explicit in iOS 11.
- `preferredScreenEdgesDeferringSystemGestures`
  - Only return edges that you need to protect.

### Auto Layout and Scroll Views

- Frame vs. Content
- `contentLayoutGuide`, `frameLayoutGuide`. Constraints in the two reference systems.

### Dynamic Type

- Now can be changed from control center.
- Apps need to participate and honor this.

- How do you choose a font appropriate for your user's dynamic type size?
  - Inflexible for custom fonts.
  - UIFontMetrics
    - Create a font metrics. Size the font for the standard size.
    - Can return a sized font instead.
- Addition to autolayout to support Dynamic Type
  - spacingBaselineToBaseline -> Get system recommended style.

### Password Autofill

- Add an entitlement
- Some JSON to web services
- (similar to support for universal links)

### Asset Catalogs

- Named colors in asset catalogs.
  - Wide gamut color support
- App thinning for icons.
- PDF images -> Preserve Vector Data
  - Allows you to scale images.
  - Symbolic glyphs that resizes with dynamic types
  - Tab bar images
    - For accesibility tap and hold can show the larger icon.

### ProMotion

- `UIScreen` query the refresh rate.



