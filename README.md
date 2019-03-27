```
  git clone 
  cd cordova-vue-apk
  npm install
  sudo apt install openjdk-8-jdk
  sudo apt install openjdk-11-jre-headless
  sudo apt-add-repository ppa:maarten-fonville/android-studio
  sudo apt-get update
  sudo apt-get install android-studi
  sudo apt-get install android-studio-preview
  npm install -g cordova
  cordova platform add android
  export ANDROID_HOME=~/Android/Sdk/
  sudo apt install gradle* || 5.3
  npm run build && cordova run android --device
```

#### INSTAll

1. Make sure to use the v10.11.0 version of the node js.
2. run npm install.
3. cordova platform add android
4. cordova platform add ios


#### Build production

##### iOS
``` bash
cordova build ios --release
```

##### web
``` bash
npm run build
```

##### Android
``` bash
  cordova build android --release

  jarsigner -verbose -sigalg SHA1withRSA -digestalg SHA1 -keystore keys/android.jks platforms/android/build/outputs/apk/release/android-release-unsigned.apk zeke_name
  
  ~/Android/Sdk/build-tools/28.0.2/./zipalign -v 4 platforms/android/build/outputs/apk/release/android-release-unsigned.apk ./Zeke.apk
```

##### Keys

1. android keystore -> Password "zekehubculture"

> A Vuetify project running in Cordova

## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build

# build for production and view the bundle analyzer report
npm run build --report

# build for production and cordova build.
npm run cordova-build

# build for production and serve the app through the browser - no hot reload.
npm run browser

# add respective platforms
cordova platform add android
cordova platform add ios

# build for production and serve the app on an iOS device
npm run ios

# build for production and serve the app on an android device (won't serve on a virtual device)
npm run android

# build for production and serve the app on an android device (will serve on a virtual device or physical device - prefers virtual)
npm run android-vm
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
