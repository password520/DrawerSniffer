[![Release](https://jitpack.io/v/evilthreads669966/drawersniffer.svg)](https://jitpack.io/#evilthreads669966/drawersniffer)&nbsp;&nbsp;[![API](https://img.shields.io/badge/API-22%2B-brightgreen.svg?style=plastic)](https://android-arsenal.com/api?level=22)
# Drawer Sniffer
### A notification interception library for Android for snooping all interceptions in the notification drawer.

### User Instructions
1. Add the maven repository to your project's build.gradle file
```gradle
allprojects {
    repositories {
        ...
        maven { url 'https://jitpack.io' }
    }
}
```
2. Add the dependency to your app's build.gradle file
```gradle
dependencies {
    implementation 'com.github.evilthreads669966:drawersniffer:0.1'
}
```
3. Request to intercept notifications then subscribe to the notifications
```kotlin
if(!DrawerSniffer.hasPermission(this))
    DrawerSniffer.requestPermission(this)
DrawerSniffer.subscribe(this@MyService){ notif ->
    Log.d("DRAWER SNIFFER", notif.toString())
}
```
## License
```
Copyright 2020 Chris Basinger

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```