Install local files via mvn install:install-file -DlocalRepositoryPath=/Path/to/release

Example:
mvn install:install-file -Dfile=TapItAdView.jar -DgroupId=tapit -DartifactId=tapit -Dversion=1 -Dpackaging=jar -DlocalRepositoryPath=/Users/jon/code/p1v/maven-external/release

See http://maven.apache.org/plugins/maven-install-plugin/examples/specific-local-repo.html for more details.

To deploy an open source maven project, add:
<distributionManagement>
  <snapshotRepository>
    <id>gh-pages</id>
    <url>file:///Users/jon/code/p1v/maven-external/release</url>
  </snapshotRepository>
</distributionManagement>

(or just a repository section if it's a release version) and run:
mvn source:jar deploy
