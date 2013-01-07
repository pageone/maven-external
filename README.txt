Install local files via mvn install:install-file -DlocalRepositoryPath=/Path/to/release

Example:
mvn install:install-file -Dfile=TapItAdView.jar -DgroupId=tapit -DartifactId=tapit -Dversion=1 -Dpackaging=jar -DlocalRepositoryPath=/Users/jon/code/p1v/maven-external/release

See http://maven.apache.org/plugins/maven-install-plugin/examples/specific-local-repo.html for more details.
