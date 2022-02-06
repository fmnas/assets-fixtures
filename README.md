# assets-fixtures
Test assets for fmnas/fmnas-site

## Fetching the assets
```shell
rsync -vaiP --delete kimgil5@forgetmenotshelter.org:/home/kimgil5/newsite/public/assets/stored/ testing/; rm testing/.gitignore
```

## Adding a test fixture
```shell
TAG=`TZ='America/Los_Angeles' date "+%y%m%d%H%M"` $SHELL -c 'git commit -am "Test fixture $TAG"; git tag -f -a $TAG -m "Test fixture $TAG" && git push -f origin $TAG && echo "Created tag $TAG" && git push'
```
