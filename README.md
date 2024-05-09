# KlazTween - Unity Tweening Library

KlazTween is a robust tweening library designed for Unity, offering high-performance animations utilizing Unity's Job System and Burst Compiler for optimized execution. It supports various data types including scalar, vector, and quaternion interpolations, enabling smooth transitions and animations in game development.

## Features

- **Versatile Tweening**: Support for floats, vectors, quaternions, and colors.
- **Job System Integration**: Leverages Unity's Job System for high-performance computations, ideal for heavy tweening scenarios.
- **Ease Functions**: Includes multiple easing functions to create dynamic and natural motion.
- **Burst Compilation**: Ready for Unity's Burst compiler to enhance performance.
- **Delay and Callbacks**: Supports initial delays and start/end callbacks for robust animation scripting.

## Dependencies

- Unity 2020.3 LTS or newer.
- Unity Mathematics Library.
- Unity Collections Library.
- Unity Jobs System (optional, for enhanced performance).

## Installation

1. Clone or download the repository.
2. Import the package into your Unity project.
3. Ensure all dependencies are resolved via Unity's Package Manager.

## Usage

To create a tween, use the `KlazTweenManager`:

```csharp
KlazTweenManager.Instance.DoTween(startValue, endValue, duration, onUpdateAction, delay, easeType, onStartCallback, onCompleteCallback);
```

### Parameters:

- **startValue** & **endValue**: The start and end values of the tween.
- **duration**: Duration of the tween in seconds.
- **onUpdateAction**: Action to perform on value update.
- **delay** (optional): Initial delay before the tween starts.
- **easeType** (optional): Type of easing function to apply.
- **onStartCallback** & **onCompleteCallback** (optional): Callbacks for start and completion of the tween.

## Customization

Modify the `KlazTweenManager` to add or adjust the tween types and behaviors as needed. You can also extend the easing functions by modifying the `Easing` class.

## Known Issues

- Job System integration is complex and should be tested extensively in different build environments.

## To-Do List

- Improve the integration with Unity's new DOTs architecture.
- Expand the library to include more complex animations such as path following.
- Optimize memory management for large-scale animations.

## License

This project is licensed under the MIT License - see the LICENSE.md file for details.
