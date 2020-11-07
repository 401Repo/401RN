# Reading: Gatsby, next.js, and other JS Frameworks

### Review, Research, and Discussion

![source](https://cdn.sanity.io/images/ay6gmb6r/production/2c73361896be95f1f39af11bcd05369f2cf88c88-2240x1260.png)

### What does React Native do when it builds your application?

Instead of the span primitive, which we have on the web, React Native offers the Text primitive. If we are building an iOS app, React Native will make sure that the Text results with a native iOS UIView containing the text. If we are building an Android application, it will result with a native TextView.

This is very important. Even though we are building our app using JavaScript, we do not get a web app embedded inside the shell of a mobile one. The result is a real native iOS or Android app.

[source](https://medium.com/we-talk-it/react-native-what-it-is-and-how-it-works-e2182d008f5e#:~:text=React%20Native%20offers%20a%20way,iOS%20UIView%20containing%20the%20text.)

### Can you simply deploy a react web app to the phone?

No, it seems that we need that difference between text primitivess creates a true app rather than a web version for our phones wich would be a poor product if a true app is needed.

*eject*

Ejection essentially allows you to take complete control of the build process. It will allow us to add these native libraries from XCode and Android Studio.

[source](https://www.yyesoftware.com/react-native-blog/react-native-eject.html)

*android avd*

An Android Virtual Device (AVD) is a configuration that defines the characteristics of an Android phone, tablet, Wear OS, Android TV, or Automotive OS device that you want to simulate in the Android Emulator. The AVD Manager is an interface you can launch from Android Studio that helps you create and manage AVDs.

[source](https://developer.android.com/studio/run/managing-avds)

*expo*

Expo is an open-source platform for making universal native apps for Android, iOS, and the web with JavaScript and React.

[source](https://expo.io/)
