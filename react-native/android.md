# android 4.4


had this issue - https://github.com/facebook/react-native/issues/12055 but chmod +x to gradle didn’t work

then this - https://github.com/facebook/react-native/issues/11767


`react-native run-android --configuration Release`

did not work, complains gradle build version
+
“task installRelease not found in app”



`react-native run-android --configuration=release`


normal build - ENOENT: no such file or directory, open 'android/app/src/main/assets/index.android.bundle'

fix by creating a folder manually “assets” in folder and run curl to create the bundle

by following - http://stackoverflow.com/a/32621060/240255



for build tools error, installed 23.0.1 and ran react-native run-android to create app

failed to install the app, manually copied the apk and installed on device


follow the steps in cnjon/react-native-pdf-view

Project with path ':PDFView' could not be found in root project 'Paper'

Could not find method compile() for arguments [project ':PDFView']

settings.gradle created seems to be different from the documentation

http://stackoverflow.com/a/33384263/240255


Error: more than one library with package name 'com.keyee.pdfview'

commented default pdf-view

```
Arrays.<ReactPackage>asList(

:app:compileDebugJavaWithJavac FAILED

````

add missing imports in `mainactivity.java` from example


stuck with 

```
npm install react-native-fs --save
```
following RNFS also failed


remove `@override` from `getPackages` seems to remove the `@override` error

seems to run curl before building apk

develop menu not showing up? 
http://stackoverflow.com/a/42008728/240255


`window.postMessage` doesnt work most of the time, even if there are no js error in injectedjs. 

Solution seems to be calling it after `timeOut` even `1ms` seems to work. 
