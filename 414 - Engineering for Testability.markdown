# 414 - Engineering for Testability

## Testable app code

- Characteristics of testable code
  - Control over inputs
  - Visibility into outputs
  - No hidden state

- Testability techniques
  - Protocols and parameterization (dependency injection)
  - Separation of side effects
  
- Use a protocol to wrap global methods used from `UIApplication.shared`
  - Match the method signatures in `UIApplication`, so conforming to the protocol doesn't require any code.
  - Now we can mock it for testing.
  
- Extract algorithms in separate types.
  - Try to give them a more functional style.
- Think layer on top to execute effects.

## Scalable app code

- UI Tests
  - Abstract UI Element Queries.
  - Store parts of queries in variables.
  - Wrap cmoplex queries in utility methods.
  - Reduces noise and clutter in UI code.

- `XCTContext.runActivity`
  - Organizes logging by nesting activity.