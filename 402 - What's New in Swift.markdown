# 402 - What's New in Swift

# Swift 4

## Language refinements and additions

### Access control

- `private` can be seen in extensions in the same file.

### Composing Classes and Protocols

`func shakeEm(controls: [UIControl & Shakeable])` -> array of objects that are UIControl and conform to Shakeable.

## Source compatibility

Language hasn't change all that much. Additive features.

- Swift 3.2
  - Same compiler. Emulates Swift 3, but it's the same compiler.
  - Allows Swift 3 syntax that has changed in Swift 4.
- 3.2 and 4.0 can coexist. Set per-target basis.
  - Swift PM understands this too.

## Tools and performance

### Build Improvements

- Preview build system.
- Fast, lower overhead, especially in large projects.
- Precompiled bridging header, faster compile times.
- Shared build for coverage testing
- If you want only some functions accessible in ObjC, put them in an @objc extension.
- Strip Swift symbols enabled by default. `xcrun dyldinfo -export` to check symbols.
  - Should not be a problem.
- Swift standard libraries are stripped as part of app thinning.
  - Recommend we leave it enabled.

## Standard library

### Strings

- Unicode Correctness by default.
- A character is a grapheme
- Equal but differently composed grapheme, cmopare as equal
- Strings are collections in Swift 4
- Syntax to get to the end of a collection (`i...`)
- `Substring` type.
  - Substrings keep a reference to the original buffer.
  - Substrings can share buffer with original string.
  - When the string goes out of scope, substring doesn't dissappear.
  - Tradeoff -> You need to convert back a Substring to a String, like when assigning to a UILabel.text property.
- Multi-line string literals. """ (triple quote to start and end multi-line string literals).
  - Indentation of the closing triple quote determines the indentantion each line.
  
### Generics

- `where` closes on associated types, to keep them in sync.

## Exclusive access to memory

- Compiler checks for access to collections.
