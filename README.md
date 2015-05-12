# loopback-users-mobile

How to use Loopback and Angular on mobile device with linux based system (Ubuntu 14.04 LTS)


## Requirements
- Open JDK + icedtea
- Android SDK
- ANT
- Node.js
- Cordova
- An emulator (Android AVD, Genymotion...)

### Install required tools

- OpenJDK : 
```bash
$ sudo apt-get install openjdk-7-jdk
$ sudo apt-get install openjdk-7-jre
```
- Icedtea : http://apt.ubuntu.com/p/icedtea-7-plugin
- Android SDK is available here : http://developer.android.com/sdk/index.html#Other (follow instructions)
  
  -> Once dowloaded, unpack the android-sdk-linux folder and keep the extraction path in mind.

  -> Open terminal, add those 2 folders to your PATH :

```bash
$ export PATH=${PATH}:~/android-sdk-linux/tools
$ export PATH=${PATH}:~/android-sdk-linux/platform-tools
```
You can now run ```$ android``` in terminal.

It should open Android SDK, from there select and install : Android SDK Tools, Android SDK Platform-tools, Android SDK build-tools, SDK Platform you wish to use, ARM EABI v7a System Image, Intel x86 Atom_64 System Image, Intel x86 Atom System Image, Android Support Library (Pay attention to the API version you want to use).

- ANT : ```$ sudo apt-get install ant```
- Node.js : ```$ sudo apt-get install nodejs npm```
- Cordova and dependencies : 
```bash
1 $ sudo add-apt-repository ppa:cordova-ubuntu/ppa
2 $ sudo apt-get update
3 $ sudo apt-get install cordova-cli
4 $ sudo apt-get install click-dev
5 $ sudo apt-get install lib32stdc++6 lib32z1
```

## Create your Cordova app

In terminal run : ```$ cordova create [dir] [domain].[yourName].[appName] [displayName]```

in my example, [appName] = 'hello' and [displayName] = 'HelloWorld'.

This will create a new folder called [dir].

Go to your app folder with ```$ cd [dir]```

And now run :
```bash
1 $ cordova platform add android
2 $ cordova build android
```
To use the app, you have to do different things, depending on the emulator.

