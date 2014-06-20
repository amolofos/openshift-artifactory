openshift-artifactory
============================
The OpenShift `jbossews` cartridge documentation can be found at:

http://openshift.github.io/documentation/oo_cartridge_guide.html#tomcat

Build
============================
Assuming that user has a openshift account and has setup already the command line tools.

1. rhc create-app artifactory jbossews-2.0
2. git clone https://github.com/amolofos/openshift-artifactory.git artifactory
3. cd artifactory
4. git remote add openshift ssh://53a4976e5973cabd5600022c@artifactory-needingmeds.rhcloud.com/~/git/artifactory.git/
5. git fetch openshift
6. git merger openshift/master
7. git add new files/commit
8. git push (to github)
9. git checkout openshift/master
10. git push openshift
11.rhc set-env ARTIFACTORY_HOME="${OPENSHIFT_DATA_DIR}/artifactory" -a artifactory 

Changelog
============================
2014-06-20 Deployed artifactory-3.2.1.1 as artifactory.war


