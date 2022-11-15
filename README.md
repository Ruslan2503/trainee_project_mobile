# MobxTest Mobile Application created to learn how to build an application.

## Windows environment 

## Installation

* **Install NodeJS** - version `v14.8.0`. Link for it: (https://nodejs.org/dist/). 
Check version after installing: `node -v`
Add the paths to the `node.exe file` to the Path variable: `C:\Program Files\nodejs`

* **Install Yarn** -  Command for Power Shell: `npm install --global yarn`
Command: `Set-ExecutionPolicy -Scope CurrentUser -ExecutionPolicy Unrestricted` fixed error `cannot be loaded because running scripts is disabled on this system`
Check version after installing: `yarn --version`

* **Install Microsoft Visual Studio** - Link for it: (https://visualstudio.microsoft.com/downloads/) including the `"Desktop development with C++" workload`. It fixed problem with `node-gyp` during `npm install` 
command: `npm install -g node-gyp`.

* **Install Chocolatey** - if it is not install with Nodejs 
To check the possibility of running scripts from third-party manufacturers, enter the command: `Get-ExecutionPolicy`
By default, the use of third-party scripts is blocked `(Restricted)`. Allow the execution of third-party scripts with the command: `Set-ExecutionPolicy Bypass -Scope Process`
The execution of the command will require confirmation, we answer with the symbol `A (Yes to All)`.

~ Now you can use third-party scripts. Install the Chocolatey package manager with the following command: `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))`

Check version after installing: `choco -v`

* **Install Python and Set PYTHON** if it is not install with - Chocolatey and Nodejs. Last version is `3.10.6`. Link for it: (https://nodejs.org/dist/) OR with the following command: `npm install -g python`
Add the paths to the `.windows-build-tools` to the Path variable: `%USERPROFILE%\.windows-build-tools\python27\python.exe`

* **Install Android SDK and Set ANDROID_HOME** Link for it: (https://developer.android.com/studio) 
Add to the Path variable: `%LOCALAPPDATA%\Android\Sdk` and `%LOCALAPPDATA%\Android\Sdk\platform-tools`
Install `NDK(side by side) version 20.1.5948944` in the `SDK tools` in `Android studio`

* **Install Gradle and Set GRADLE_HOME** Link for Download: binary-only: (https://gradle.org/releases/)
Add to the Path variable: `C:\Gradle\gradle-6.9` and `C:\Gradle\gradle-6.9\bin`

* **Install Java SDK and Set JAVA_HOME** - install by command: `choco install openjdk11`
Add the paths to the platform tools to the Path variable: C:\Program Files\Java\jdk-11.0.2\bin
Check version after installing: java -version

* **For Windows local commands:** 

# Run on Android ##

1) Open a new bash shell
2) yarn install
3) npm run android

## Run on iOS ##

1) Open a new bash shell
2) yarn install
4) cd ios
5) rm -rf ~/Library/Caches/CocoaPods Pods ~/Library/Developer/Xcode/DerivedData/*; pod deintegrate; pod setup; pod install;
6) open in folder ios filename extension with .xcworkspace

## Create apk ##

1) yarn install
2) npx jetify
3) cd android
4) ./gradlew assembleRelease

## Create ipa ##

1) yarn install
3) cd ios
4) rm -rf ~/Library/Caches/CocoaPods Pods ~/Library/Developer/Xcode/DerivedData/*; pod deintegrate; pod setup; pod install;
5)  open xcode; Product -> Clean Build Folder -> Archive -> Distribute app -> Manage certificate -> upload


## Main test package.json file with
* dependencies 
* devDependencies

## dependencies versions:
    "@react-native-community/async-storage": "1.12.1",
    "@react-native-community/masked-view": "0.1.10",
    "@react-navigation/native": "5.8.6",
    "@react-navigation/stack": "5.12.3",
    "@types/react": "^16.9.56",
    "appcenter": "4.0.0",
    "appcenter-analytics": "4.0.0",
    "appcenter-crashes": "4.0.0",
    "mobx": "6.0.3",
    "mobx-react": "7.0.0",
    "react": "16.13.1",
    "react-native": "0.63.5",
    "react-native-gesture-handler": "1.8.0",
    "react-native-reanimated": "1.13.1",
    "react-native-safe-area-context": "3.1.8",
    "react-native-screens": "2.13.0"
## devDependencies versions:       
    "@babel/core": "7.12.3",
    "@babel/plugin-proposal-decorators": "7.10.5",
    "@babel/runtime": "7.12.5",
    "@react-native-community/eslint-config": "1.1.0",
    "@types/react-native": "^0.63.35",
    "babel-jest": "25.5.1",
    "detox": "^17.14.6",
    "eslint": "6.8.0",
    "jest": "^25.5.4",
    "jest-circus": "^26.6.3",
    "metro-react-native-babel-preset": "0.59.0",
    "react-test-renderer": "16.13.1"

## Project navigation






