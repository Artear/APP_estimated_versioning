# APP_release_versioning

## Android
### Install
```
cd #project#
mkdir 'am_gradle'
curl -o './am_gradle/release_versioning.gradle' -k 'https://raw.githubusercontent.com/Artear/APP_release_versioning/v1.1/release_versioning.gradle'
```
### .gitignore
```
/am_gradle/build
```
### Implementation

1. open **build.gradle**
2. add extra properties and from **release_versioning.gradle**

	```
	ext {
	    release_versioning_code = 0
	    release_versioning_name = "1.0.0"
	    release_versioning_branch = "master"
	}
	apply from: './../am_gradle/release_versioning.gradle'
	```
3. set versionCode and versionName
	```
	defaultConfig {
		applicationId "..."
		...
		versionCode release_versioning_code
		versionName "v${release_versioning_name}"
		...
	}
	```