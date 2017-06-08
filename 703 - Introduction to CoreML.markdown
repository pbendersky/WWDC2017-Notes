# 703 - Introduction to CoreML

- Domain specific frameworks
  - Vision / NLP
- ML Framework
  - Core ML
- ML Performance Primitives
  - Accelerate

- Vision
  - Object tracking
  - Face identification
  
- NLP
  - Language identification
  - Named Entity Recognition
  
## Core ML

- Take a MLModel and integrate into app
- Focus on experience rather than implementation details.
- Simple & performant
- Unified inference API
- Xcode integration
- Fine tuned inference engines
- Built on Accelerate and Metal
- Compatible
  - Public model format
  - Support for popular training libraries

- Model
  - Observed inputs
  - Predicted outputs
  
- http://developer.apple.com/machine-learning
  - Predefined MLModels
- ResNet50

- Resources
  - Caffe
  - Keras
  - dmlc XGBoost
  - Turi
  - LibSVM

- Core ML Tools (Python). Open source tools to convert models to MLModel

- Xcode generates Swift code from the MLModel
- Model gets compiled and bundled in the app, optimized for runtime.

