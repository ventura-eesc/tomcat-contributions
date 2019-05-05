# tomcat-contributions

  This shows to newbies how to make tomcat contributions from the tomcat git hub repository

  In the scope of the [EU-FOSSSA-2 Project](https://joinup.ec.europa.eu/collection/eu-fossa-2), [hackathon](https://eufossahackathon.bemyapp.com/), the memebers of the tomcat team give us a samll introduction. Here you will find my findings.


## Fork the repository

Go to the tomcat github repositori [https://github.com/apache/tomcat](https://github.com/apache/tomcat) and make a fork ussing you own git hub account

## Clone yout forked repository

```bash

git clone https://YOUR_GITHUB_USER_NAME@github.com/ventura-eesc/tomcat

cd tomcat

ant

cd tomcat/output/build

# This starts in to a shell
/bin/catalina.sh run

```

And voila! you have your tomcat working.

## Execute tests

Go to your tomcat-forked folder and execute:

```bash
ant test
```


Some considerations:
Use the build.properties.default to customize some aspects as:

```
# Number of parallel threads to use for testing. The recommended value is one
# thread per core.
# Note: Cobertura code coverage currently requires this to be set to 1. Setting
#       a value above one will disable code coverage if enabled.
test.threads=4
```

Or to avoid the tests related to the APR:

```
# Still requires APR/native library to be present
execute.test.apr=false
```

## How to install tomcat native

Mac OS X:

```bash
brew install tomcat-native
```

* [Here the downloading page](http://tomcat.apache.org/download-native.cgi)
* [Some docs](https://tomcat.apache.org/native-doc/)

To build from sources take a look on the: tomcat-native-1.2.8-src/native/BUILDING



```bash
In order for tomcat's APR lifecycle listener to find this library, you'll
need to add it to java.library.path. This can be done by adding this line
to $CATALINA_HOME/bin/setenv.sh

  CATALINA_OPTS="$CATALINA_OPTS -Djava.library.path=/usr/local/opt/tomcat-native/lib"

If $CATALINA_HOME/bin/setenv.sh doesn't exist, create it and make it executable.
```

