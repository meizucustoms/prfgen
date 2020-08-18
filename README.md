# prfgen
Generate proprietary-files.txt with SHA1SUM and modules easy

## Setup
```
$ git clone https://github.com/MeizuCustoms/prfgen.git prfgen
# NOTE: next steps are needed only if you have ~/bin directory
$ cp prfgen/prfgen ~/bin/prfgen
$ rm -rf prfgen
```
Then, open ~/bin/prfgen with your editor and change ```DT_VENDOR``` and ```DT_DEVICE``` variables to your device tree paths.

## Using
If you have modules in Android.mk, you should use ```--modulelist 'module list file'``` argument to create right proprietary-files.txt.

### Module list example
```
lib/libmeizu.so
vendor/etc/xiaomi_is_shit.conf
```

### Terminal example
```
# F = file, M = module
$ prfgen --modulelist modules.txt
[1/1758] 0% F
...
[1578/1758] 100% M
$
```

Hope, you will have fun with this shit.
