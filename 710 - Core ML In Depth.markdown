# 710 - Core ML In Depth

- Think of models as code. Interact with them in Xcode as if they were code files.

## Use cases

- Images
  - Style transfer
- Gestures
  - Gesture recognition
- Video (credit card detection)
- Audio
- Text
  - Sentiment Analysis

- Focus on code, not models!
  - Models as Functions
  - Models are prediction funcitons that take some inputs and give you some outputs.
    - Numeric
    - Categories
    - Images
    - Arrays -> `MLMultiArray` encapsulates multidimensional arrays.
    - Dictionaries
      `[ String: Double]`, `[Int64: Double]`
      
### Example Sentiment Analysis

- Input is a dictionary. Keys are words, values are counts.
  - Can use NLP to process text.
- Most models don't work directly on raw text, there's always a little bit of preprocessing required.

### Example Predictive Keyboard

- Give current work to model.
- Get back a set of choices and a state, associated with the prediction.
- Give next word to model and the previous state.
- On each step, send the next word and the state back to the prediction model.

## Hardware optimized

- Hides the hardware from the developer.
- Built on top of Accelerate and MPS.
- CPU heavy -> Runs on GPU -> MPS
- Memory heavy -> Runs on CPU -> Accelerate
- Automatic context switch of CPU / GPU, hidden from the developer.

## Obtaining models

- Two places to look for:
  - Example models in http://developer.apple.com/machine-learning
  - Popular training tools from others
    - Caffe, etc.
    - Core ML Tools -> Converter package.
      - Open Source
    - `pip install coremltools`

### What is coremltools

- Converters
- Core ML Bindings / Converter Libraries
- Core ML Specification

- Extensible -> Easy to add new converters.
- Public format, fully documented.

- Can test the models with Python as well as convert them.
