# Xbox Cloud Gaming (Unofficial)
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
TODO

### Caveats
- I haven't been able to `npm run build` on Windows 11. Subsystem for Linux (WSL) _might_ be a workaround.

### Pre-requisites
WIP
- [node](https://nodejs.org/en/)
