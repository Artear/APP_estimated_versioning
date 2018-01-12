# APP_release_versioning

Get commant
```
echo "python $(pwd)/release_versioning" | pbcopy | pbpaste
```

Run
```
cd #project folder#
python #commant# | python -m json.tool
```

Android
```
cd #project#
mkdir 'am_gradle'
curl -o './am_gradle/release_versioning.gradle' -k 'https://raw.githubusercontent.com/Artear/APP_release_versioning/v1.1/release_versioning.gradle'
```
