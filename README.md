# Xbox Cloud Gaming PWA on Android
## Optimized for Chromecast with Google TV
A wrapper for the Xbox Cloud Gaming PWA that generates a .apk file that can be installed on Chromecast with Google TV (CCWGTV).

## Installation
You will need prior knowledge on sideloading apps on CCWGTV. There are several options. Google "Sideloading apps on Chromecast with Google TV" and read some of the articles in the results.

### Pre-requisites
- Connect bluetooth mouse to you CCWGTV
- [Enable Developer Options](https://developers.google.com/cast/docs/android_tv_receiver/debugging#setting_up_for_development)
- You may also need to enable "unknown sources" depending on the sideloading method you choose

### Steps
1. Download and install/sideload [Google Chrome: Fast & Secure 107.0.5304.91 (arm-v7a)](https://www.apkmirror.com/apk/google-inc/chrome/chrome-107-0-5304-91-release/google-chrome-fast-secure-107-0-5304-91-5-android-apk-download/download/?key=e27e2cd57d80b879bc4be28ee3c9785f129bfa05&forcebaseapk=true) on your CCWGTV  
  **Note:** You may need to uninstall Chrome from you CCWGTV if it's already installed.
1. Download the .zip file from [releases](https://github.com/djbreen7/xbox-cloud-gaming-android/releases/tag/0.1.0)
1. Extract the .zip file
1. Install/sideload the extracted .apk on your CCWGTV

### First Run
1. Use your favorite sideload launcher to run the app. It will be installed as "Cloud Gaming"  
  a. Alternatively, you can launch the app without a sideload launcher by going to **Settings > Apps > See all apps > Cloud Gaming > Open**
1. Login as you normally would on `xbox.com/play`. At the time of writing, a mouse is required to select the login and password inputs
  
## Development

### Pre-requisites
- [node](https://nodejs.org/en/)
- (optional*) [JDK 11](https://github.com/AdoptOpenJDK/openjdk11-binaries/releases/)
- (optional*) [Android SDK](https://developer.android.com/about/versions/11/setup-sdk#get-sdk)

*_You have the option to let bubblewrap install JDK 11 and Android SDK for you when prompted the first time you run `npm run build`. Alternatively, you can download and install them manually. The links correlate to the same versions that bubblewrap installs. I assum you know what you're doing if you install different versions._


**NOTE: You may need to add the binaries to the `PATH` variable manually**
```shell
# Paths as of writing when letting bubblewrap install
export PATH="$PATH:$HOME/.bubblewrap/jdk/jdk-11.0.9.1+1/bin"
export PATH="$PATH:$HOME/.bubblewrap/android_sdk/platform-tools"
```

### Setup
1. Create a folder named `.android` in the root of this project  
  a. If you DO NOT already have a debug keystore:  
```shell
keytool -genkey -v -keystore ./.android/debug.keystore -storepass android -alias androiddebugkey -keypass android -keyalg RSA -keysize 2048 -validity 10000
```  
  b. If you DO already have a debug keystore, copy it into the `.android` folder you created in step one  
2. `npm install`

### Building
1. `npm run build:debug`



