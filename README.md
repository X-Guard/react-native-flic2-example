# react-native-flic2-example
This repository contains a functional example of https://github.com/X-Guard/react-native-flic2.

The purpose of this repistory is to explain how the plugin works and at the same time test the Flic2 library functionality on React Native.

# Install 
Follow these steps to install this test project and run it on your device. Please note that you will need a Flic2 button to actually use this application.

1. Clone this project to your local development environment
2. Run `npm install` from your project root
3. Run `cd ios; pod update; cd ../` to install CocoaPods plugins
4. **iOS** Open the `ios/Flic2.xcworkspace` file in Xcode (or run `xed ./ios` to open Xcode)
5. **iOS** Fix certificates and team setup for both `Flic2Example` target
6. **iOS** Run project on your physical device (simulator is not supported out of the box, please take a look at https://github.com/50ButtonsEach/flic2lib-ios/wiki/Simulator-Support to add Simulator support)
7. **Android** run `npm run android` to run the app on Android, 

# Exploring the example
All functional code for this example has been included in a single file: `App.js`.

This example shows:
1. Scanning for new buttons including serveral example errors (`Flic2.startScan()`)
2. Forgetting all the connected buttons (`Flic2.forgetAllButtons()`)
3. A list of buttons the app knows including:
	1. The ready state of the button (`Flic2Button.isReady`) will color the row border red or green
	2. The estimated battery level (`Flic2Button.getBatteryLevel()`)
	3. Forgetting a button completely (`Flic2Button.forgetButton()`)
	4. Getting and setting the button name (`Flic2Button.getName()` and `Flic2Button.setName()`)
	5. Connecting and disconnecting a button connection (`Flic2Button.connect()` and `Flic2Button.disconnect()`)