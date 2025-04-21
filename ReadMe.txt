React Native/Expo Setup Guide for ConfirmationWallet-Frontend (using Expo + EAS)

Welcome to the project! This guide will walk you through setting up your local environment so you can start building features alongside the rest of the team.

Prerequisites
    •	Node.js and npm installed (we recommend using nvm to manage versions)
    •	Git installed
    •	A physical iOS or Android device (or simulators/emulators)
    •	Expo CLI

⸻

1. Set Up Your Expo Account

Create an account at expo.dev if you haven’t already. We use Expo’s EAS build service for development and production.

⸻

2. Clone the Repository

git clone https://github.com/ConfirmationWallet/ConfirmationWallet-Frontend
cd ConfirmationWallet-Frontend

⸻

3. Install Project Dependencies

npm install

⸻

4. A. Configure EAS (Expo Application Services)

Follow the Expo guide to configure your development builds:
https://docs.expo.dev/tutorial/eas/configure-development-build/

Note: This app uses custom native code. Do not use the default Expo Go app. Instead, use a development build installed on your device.

⸻

4. B. Installation

Follow the Expo guide for your physical device or simulator:
    •	Android: https://docs.expo.dev/tutorial/eas/android-development-build/
    •	IOS: https://docs.expo.dev/tutorial/eas/ios-development-build-for-devices/
    •	IOS Simulator: https://docs.expo.dev/tutorial/eas/ios-development-build-for-simulators/
    

Note: This app uses custom native code. Do not use the default Expo Go app. Instead, use a development build installed on your device.

⸻

5. Run the App

Start the development server:

npx expo start

Then:
	•	On a physical device: Scan the QR code shown in your terminal or browser. This will install and open the custom development build.
	•	On a simulator/emulator: You can also run it on iOS/Android emulators if set up, but we recommend frequent testing on a physical device to reduce environment-specific bugs.

⸻

6. Hot Reloading & Refreshing
	•	Most UI changes will automatically reload.
	•	Some changes (like navigation or config) may require a full refresh:
	•	Press r in the terminal
	•	Or shake your device and choose Reload from the menu

⸻

Development Notes
	•	Build settings are version-controlled in eas.json and app.config.js, so no manual updates needed — just make sure you’re on the latest branch! If you make changes to build files, either add to your .gitignore or ensure changes are compatible with all feature branches.
	•	If you run into native issues, try clearing cache: 
            npx expo start --clear