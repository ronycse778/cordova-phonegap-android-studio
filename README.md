# cordova-phonegap-android-studio
Simple android app built with Cordova, PhoneGap and Android Studio (Manual Process)

<b>Prerequisite:</b> <br>
1. Android Studio(Jellyfish | 2023.3.1)(zip) <br>
2. Gradle-8.8(complete-zip) <br>
3. JDK-17 (installer) <br>
4. NodeJs-20.15.1 <br>

<b>Procedure:</b> <br>
1. Unzip Android Studio. (D:/Android-Studio/android-studio) <br>
2. Unzip Gradle (D:/Android-Studio/gradle-8.8 <br>
3. SDK location (D:/Android-Studio/SDK) <br>

<b>Set Environment Path(If path not added):</b> <br>
<b>System variable:</b> <br>
1. Name(ANDROID_HOME), Value(D:\Android-Studio\SDK) <br>
2. Name(ANDROID_SDK_ROOT), Value(D:\Android-Studio\SDK) <br>
3. Name(GRADLE_HOME), Value(D:\Android-Studio\gradle-8.8) <br>
4. Name(JAVA_HOME), Value(C:\Program Files\Java\jdk-17) <br> <br>
1. Path (D:\Android-Studio\SDK\platform-tools) <br>
2. Path (D:\Android-Studio\gradle-8.8\bin) <br>
3. Path (%JAVA_HOME%\bin) <br>

<b>Install Node.JS, then Cordova:</b> <br>
<pre>npm install -g cordova</pre>

<b>PhoneGap Procedure(CMD):</b> <br>
Step 1: Create a new Cordova App <br>
<pre>cordova create MyInfo info.androidabcd.myinfo MyInfo<br>cd MyInfo</pre>

Step 2: Add the Android platform <br>
<pre>cordova platform add android@latest</pre>

Step 3: Prepare the Cordova project <br>
<pre>cordova prepare</pre>
If cordova prepare show problem (ex. app import from outside), then remove and re-add the Android platform
<pre>cordova platform remove android <br>
cordova platform add android</pre>

Step 4: Build Cordova Project <br>
<pre>cordova build android</pre>

Build Successful--APK built (In CMD)

<b>Build/Import With Android Studio Procesure:</b> <br>
1. Select Project MyInfo > platform > android
2. Auto build start & finish successfully. If not, File>Sync project with gradle.
3. If build problem, then set bellow settings.

<b>Android Studio:</b> <br>
Show snapshot from Data.Source folder <br>
File> Settings> Build & Execution> Build Tools> Gradle <br>
Distribution> Wrapper(auto selected), Gradle JDK> or select any JDK-17, Select 2nd box> jbr/JDK-17 <br>
If gradle wrapper not find, then select Local Installation > Select any JDK-17 <br>

File> Project Structure> gradle 8.4 auto selected or not. (optional). <br>
Tools> SDK Manager> Set SDK location. <br>
API Level-35 checked. <br>
Show attached snapshot of SDK tools download in Data.Source folder. <br>

Project should be build after that.

<b>Cordova config file:</b> <br>
Cordova app manifesto file (like config.xml in Android Studio)  <br>
location: node_modules\cordova_android\framework\cdv-gradle-config-defaults.json <br>
If build have problem with SDK image not found, then see SDK version from manifesto & download in SDK manager. <br>
Check snapshot. <br>

<b>APK build file location:</b> <br>
MyInfo\platforms\android\app\build\outputs\apk\debug

<b>To use this repository:</b> <br>
Unzip node_modules.zip and platforms.zip file

Done.
