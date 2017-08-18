# Cordova Starter

Custom build-extras.gradle for building auto signed apk's for release and debug. The gradle also handles auto naming of apk's depending on the build type. 

## Includes 
- build-extras.gradle
- build.json
- appBeforeBuild.bat

Just edit projectName's value.

## How to use these files:
1. Copy all the included file in your main cordova folder
2. Add the following line in your config.xml
```
<hook src="appBeforeBuild.bat" type="before_build" />
```
3. Generate a keystore
```
keytool -genkey -v -keystore keystoreName.keystore -alias keystoreAlias -keyalg RSA -keysize 2048 -validity 10000`
```
4. Copy keystore in your main cordova folder
5. Edit build-extras.gradle and build.json