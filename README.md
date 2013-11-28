gradle-android-signing
======================

Help handle android signing config

With this gradle script, you can store you signing keystore and password seprate from source code.
Now, script support two search folder:
* project rootDir, etc. trunk
* gradleUserHomeDir, etc.C:\Document and settings\UserName\.gradle

Properties filename is: *signing.properties*

File content:


STORE_FILE=keystore_file_path

STORE_PASSWORD=keystore_password

KEY_ALIAS=key_alias

KEY_PASSWORD=key_password
