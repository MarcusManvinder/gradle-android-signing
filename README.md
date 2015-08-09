# gradle-android-signing

## Usage

### 1. Create signing.properties

Create `signing.properties` file either in your project root directory (next to
your `build.gradle`), or globally in your gradle home directory
(`$HOME/.gradle`).

Don't add it to your version control if you decided to keep it inside the project.

```
storeFile=keystore_file_path
storePAssword=keystore_password
keyAlias=key_alias
keyPassword=key_password
```

### 2. Include signing gradle script

Add the following line to the end of your `build.gradle`:

```
apply from: 'https://raw.github.com/trikita/gradle-android-signing/master/gradle-android-signing.gradle'
```

### 3. Build and sign your app

```
gradle clean build
```

If your only want to build the release variant and sign it (without linting
etc) - run `gradle assembleRelease`.
