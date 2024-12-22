# React Native Dimensions API Inconsistency

This repository demonstrates a bug related to inconsistencies in screen dimension retrieval using the `Dimensions` API in React Native.  The problem manifests primarily on devices with display notches or when the software keyboard is active, resulting in inaccurate window dimensions being returned.

The `DimensionsBug.js` file showcases the problematic behavior. The `DimensionsBugSolution.js` file provides a potential workaround.

## Reproduction

1. Clone this repository.
2. Run `npm install` or `yarn install` to install dependencies.
3. Run the app on a device or emulator, observing the layout on various devices and scenarios (keyboard shown/hidden).

## Solution

The proposed solution involves using event listeners (`onLayout` or `keyboardDidShow`/`keyboardDidHide`) and a state variable to track dimensions and apply corrections.