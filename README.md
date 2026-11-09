# Text to Hear

A one-screen React Native app, built with Expo, that reads typed text aloud using the device's speech synthesiser through `expo-speech`. The project sits one folder down in `text-to-speech/`.

## Requirements

- Node.js and npm (or yarn)
- The Expo CLI, run through `npx expo`
- A device or simulator with a speech engine. Expo Go on an iOS or Android phone works; the web target depends on the browser supporting the Web Speech API.

## Setup

```sh
cd text-to-speech
npm install
```

Both a `yarn.lock` and a `package-lock.json` are committed; use whichever package manager you prefer.

## Usage

```sh
npm start          # Expo dev server with QR code
npm run web
npm run android
npm run ios
```

Type something into the text box and press "Click to Hear". The device speaks the text in its default voice and language.

## How it works

`App.js` is the whole app. It holds the input text in component state and, on button press, calls `Speech.speak(text)` from `expo-speech`. The header comes from `react-native-elements`, and the speaker icon above the input is loaded from an external URL (shareicon.net), so it only appears with a network connection.

## Project layout

```
text-to-speech/
  App.js             the single screen: header, icon, text input, speak button
  assets/            icon, splash, adaptive icon, favicon
  app.json           Expo configuration (name Project65-TextToSpeechConverter)
  package.json       Expo 51 / React Native 0.74, expo-speech, react-native-elements
  babel.config.js
  package-lock.json, yarn.lock
```
