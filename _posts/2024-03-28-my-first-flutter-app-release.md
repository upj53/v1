---
title: 플러터 앱 출시 방법
layout: upj_design
permalink: /flutter-app-release
---

참고

- [코딩파파](https://www.youtube.com/watch?v=1KYEPKRVFZA)
- []()
- []()
- []()

key 생성하기

```text
keytool -genkey -v -keystore key.jks -keyalg RSA -keysize 2048 -validity 10000 -alias key
```

key.properties 파일 만들기


```text
key.properties 파일 내용

storePassword=암호
keyPassword=암호
keyAlias=key
storeFile=./key.jks

android\app 폴더에 key.properties 파일 생성하기
key.jks 파일 위치 C:\Users\unite\Documents\__git__\store_my_first_app\android\app
```

app 단위 build.gradle 파일 설정 변경

```text
plugins {
    id "com.android.application"
    id "kotlin-android"
    id "dev.flutter.flutter-gradle-plugin"
}

def localProperties = new Properties()
def localPropertiesFile = rootProject.file('local.properties')
if (localPropertiesFile.exists()) {
    localPropertiesFile.withReader('UTF-8') { reader ->
        localProperties.load(reader)
    }
}

def flutterVersionCode = localProperties.getProperty('flutter.versionCode')
if (flutterVersionCode == null) {
    flutterVersionCode = '1'
}

def flutterVersionName = localProperties.getProperty('flutter.versionName')
if (flutterVersionName == null) {
    flutterVersionName = '1.0'
}

// 추가하기
def keystoreProperties = new Properties()
def keystorePropertiesFile = rootProject.file('key.properties')
if (keystorePropertiesFile.exists()) {
    keystoreProperties.load(new FileInputStream(keystorePropertiesFile))
}

android {
    namespace "io.github.upj53.upj_manager"
    compileSdkVersion flutter.compileSdkVersion
    ndkVersion flutter.ndkVersion

    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }

    kotlinOptions {
        jvmTarget = '1.8'
    }

    sourceSets {
        main.java.srcDirs += 'src/main/kotlin'
    }

    defaultConfig {
        // TODO: Specify your own unique Application ID (https://developer.android.com/studio/build/application-id.html).
        applicationId "io.github.upj53.upj_manager"
        // You can update the following values to match your application needs.
        // For more information, see: https://docs.flutter.dev/deployment/android#reviewing-the-gradle-build-configuration.
        // 버전은 변경하기 않는다
        minSdkVersion flutter.minSdkVersion
        targetSdkVersion flutter.targetSdkVersion
        versionCode flutterVersionCode.toInteger()
        versionName flutterVersionName
    }

    // 추가하기
    signingConfigs {
        release {
            keyAlias keystoreProperties['keyAlias']
            keyPassword keystoreProperties['keyPassword']
            storeFile file(keystoreProperties['storeFile'])
            storePassword keystoreProperties['storePassword']
        }
    }

    buildTypes {
        release {
            // 변경하기
            signingConfig signingConfigs.release
        }
    }
}

flutter {
    source '../..'
}

dependencies {}
```

패키지명 바꾸기

> 패키지 추가하기
> flutter pub add change_app_package_name

```text
패키지명 바꾸기
flutter pub run change_app_package_name:main io.github.upj53.upj_manager
```

플러터 앱 빌드하기

> flutter build appbundle

업로드 버전은 항상 웹페이지보다 하나 더 많게 해야 한다.
