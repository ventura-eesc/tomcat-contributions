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

