
Joda-Time
=========
Joda-Time is a date and time library that vastly improves on the JDK.

See the home page for more details:
http://joda-time.sourceforge.net/

The source code is held primarily at GitHub:
https://github.com/JodaOrg/joda-time

Related projects at GitHub:
https://github.com/JodaOrg/joda-time-hibernate
https://github.com/JodaOrg/joda-time-jsptags
https://github.com/JodaOrg/joda-time-i18n

Other related projects:
http://joda-time.sourceforge.net/related.html

Flightstats Build Instructions
- download tzdata file (from http://www.iana.org/time-zones, grab the "data" tgz)
- note exact file size of the tgz
- edit src/conf/MANIFEST.MF and
  - update all 2014? to the latest (eg. 2014i->2014j)
  - Update the OlsonDatabase-FileSize to be the size of the new tgz file
  - edit pom.xml to make the same version change (2014i->2014j)
- cd to src/main/java/org/joda/time/tz/src
- untar the tzdata.tar.gz into this directory, overwriting the existing files. Ignore any new files untarred, they can be deleted.
- Commit the changes
- At the root, type "mvn package"


