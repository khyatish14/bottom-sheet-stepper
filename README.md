# Bottom Sheet Stepper 🚀

![GitHub release (latest by date)](https://img.shields.io/github/v/release/khyatish14/bottom-sheet-stepper)
![GitHub issues](https://img.shields.io/github/issues/khyatish14/bottom-sheet-stepper)
![GitHub forks](https://img.shields.io/github/forks/khyatish14/bottom-sheet-stepper)
![GitHub stars](https://img.shields.io/github/stars/khyatish14/bottom-sheet-stepper)

Welcome to **Bottom Sheet Stepper**, a lightweight and customizable stepper component for React Native. This component is built on top of [@gorhom/bottom-sheet](https://github.com/gorhom/react-native-bottom-sheet), allowing you to easily manage multi-step flows in a modal bottom sheet with smooth animations and full control.

## Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Examples](#examples)
- [API Reference](#api-reference)
- [Contributing](#contributing)
- [License](#license)
- [Changelog](#changelog)

## Features ✨

- **Lightweight**: Minimal impact on your app's performance.
- **Customizable**: Adjust styles and animations to fit your app's theme.
- **Smooth Animations**: Enjoy fluid transitions between steps.
- **Full Control**: Manage step navigation with ease.
- **Mobile-Friendly**: Designed specifically for React Native.

## Installation 🛠️

To install the Bottom Sheet Stepper component, use npm or yarn:

```bash
npm install bottom-sheet-stepper
```

or

```bash
yarn add bottom-sheet-stepper
```

## Usage 📚

To use the Bottom Sheet Stepper, follow these steps:

1. **Import the Component**:

   ```javascript
   import BottomSheetStepper from 'bottom-sheet-stepper';
   ```

2. **Set Up Your Steps**:

   Define the steps you want to include in your stepper. Each step can be a component or a simple view.

   ```javascript
   const steps = [
     { title: 'Step 1', content: <StepOneComponent /> },
     { title: 'Step 2', content: <StepTwoComponent /> },
     { title: 'Step 3', content: <StepThreeComponent /> },
   ];
   ```

3. **Render the Stepper**:

   Use the Bottom Sheet Stepper in your component.

   ```javascript
   const MyComponent = () => {
     return (
       <BottomSheetStepper steps={steps} />
     );
   };
   ```

## Examples 🎨

Check out the following examples to see the Bottom Sheet Stepper in action.

### Basic Example

Here’s a simple example of how to implement the Bottom Sheet Stepper.

```javascript
import React from 'react';
import { View, Text, Button } from 'react-native';
import BottomSheetStepper from 'bottom-sheet-stepper';

const StepOne = ({ next }) => (
  <View>
    <Text>Step 1: Welcome!</Text>
    <Button title="Next" onPress={next} />
  </View>
);

const StepTwo = ({ next, back }) => (
  <View>
    <Text>Step 2: Provide Details</Text>
    <Button title="Back" onPress={back} />
    <Button title="Next" onPress={next} />
  </View>
);

const StepThree = () => (
  <View>
    <Text>Step 3: Confirmation</Text>
  </View>
);

const steps = [
  { title: 'Welcome', content: StepOne },
  { title: 'Details', content: StepTwo },
  { title: 'Confirm', content: StepThree },
];

const App = () => (
  <BottomSheetStepper steps={steps} />
);

export default App;
```

## API Reference 📖

### Props

| Prop           | Type               | Description                                     |
|----------------|--------------------|-------------------------------------------------|
| `steps`        | Array              | Array of steps to display in the stepper.      |
| `initialStep`  | Number (optional)  | The step to start from (default is 0).         |
| `onComplete`   | Function (optional) | Callback when the stepper completes.            |
| `style`        | Object (optional)  | Custom styles for the stepper.                 |

## Contributing 🤝

We welcome contributions! If you want to contribute to the Bottom Sheet Stepper, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature/YourFeature`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature/YourFeature`).
6. Open a pull request.

Please ensure your code follows the project's coding standards and includes tests where applicable.

## License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Changelog 📅

You can find the latest changes in the [Releases](https://github.com/khyatish14/bottom-sheet-stepper/releases) section. Please check this section regularly for updates.

For the latest release, visit [Releases](https://github.com/khyatish14/bottom-sheet-stepper/releases).

---

Thank you for checking out Bottom Sheet Stepper! We hope it makes your development process smoother and more efficient. If you have any questions or suggestions, feel free to reach out. Happy coding!