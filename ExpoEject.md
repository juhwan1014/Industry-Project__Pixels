# Sets on how to run app on xcode after cloning github repo
ios simulator does not have access to camera, so to test app properly you must connect your iphone to your laptop
In the terminal, inside the capture-front end folder:
1. npm install
2. npm i -g react-native-cli
3. In package.json under scripts add 
    "build:ios": "react-native bundle --entry-file='index.js' --bundle-output='./ios/main.jsbundle' --dev=false --platform='ios'"
4. npm run build:ios
    * this step may take some time to complete
5. npm install aws-amplify aws-amplify-react-native amazon-cognito-identity-js @react-native-community/netinfo
6. expo eject
    * you can use default settings
7. cd ios -> pod install
8. open capture.xcworkspace
9. in capture.xcodeproj -> signing & capabilities -> choose team (can be personal or owners)
    * if you don't have an apple ID developer account yet, create one first
        * then in preferences, under account add your apple ID 
    * if personal, change bundle identifier to avoid conflicts
    **insert image of capture.xcodeproj**
10. in same capture.xcodeproj -> build phases -> under Bundle React native code and images -> remove all code in shell
11. in supporting folder -> expo.plist -> in Root, add EXUpdatesURL: https://Examples.com 
    **insert image of expo.plist**
12. in same expo.plist, change EXUpdatesEnabled to false

and the app should be runnable on expo
