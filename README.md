gradle-android-signing
======================


# Usage

## 1.Create signing.properties

With this gradle script, you can store you signing keystore and password seprate from source code.
Now, script support two search folder:
* project rootDir, etc. trunk
* gradleUserHomeDir, etc.C:\Document and settings\UserName\.gradle

Properties filename is: *signing.properties*

## 2.Config signing.properties

Config signing.properties use your keystore info as below format:

```
STORE_FILE=keystore_file_path
STORE_PASSWORD=keystore_password
KEY_ALIAS=key_alias
KEY_PASSWORD=key_password
```

## 3.Call the script from each sub-modules build.gradle

Add the following at the end of each build.gradle that you wish to siging:
```
apply from: 'https://raw.github.com/JiyongShi/gradle-android-signing/master/gradle-android-signing.gradle'
```

## 4.Build release with signing
```
gradle clean build
```
or
```
gradle clean assembleRelease
```

# License
```
Copyright 2013 Shi Jiyong (SHIJIYONG@HOTMAIL.COM,JIYONG.SHI@GMAIL.COM)
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
