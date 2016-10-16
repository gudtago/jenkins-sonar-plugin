Jenkins SonarQube Plugin
====================

[![Build Status](https://travis-ci.org/SonarSource/sonar-scanner-jenkins.svg?branch=master)](https://travis-ci.org/SonarSource/sonar-scanner-jenkins)

Project homepage: http://redirect.sonarsource.com/plugins/jenkins.html

Continuous inspection: http://nemo.sonarsource.org/dashboard/index/org.jenkins-ci.plugins:sonar

Issue tracking: http://jira.sonarsource.com/browse/SONARJNKNS


If you're wanting to make changes, please clone the git repository at

git://github.com/SonarSource/jenkins-sonar-plugin.git

With jenkins-sonar-plugin, you can configure SonarQube instances and run a SonarQube Scanner analysis in several ways:
* By injecting the SonarQube configuration as environment variables and using them in any job step (such as Maven, Ant, Gradle, ...);
* Using the Sonar Scanner job;
* Using SonarQube Scanner for MSBuild's 'begin analysis' and 'end analysis' jobs;


'SonarQube Scanner' and 'SonarQube Scanner for MSBuild' are managed as installable tools. List of available versions is retrieved
automatically by Jenkins/Hudson from a json file hosted on their respective update site:
* http://hudson-ci.org/updates/hudson.plugins.sonar.SonarRunnerInstaller.json
* http://mirrors.jenkins-ci.org/updates/updates/hudson.plugins.sonar.SonarRunnerInstaller.json
* http://mirrors.jenkins-ci.org/updates/updates/hudson.plugins.sonar.MsBuildSonarQubeRunnerInstaller.json

For Jenkins, the files are automatically updated when a new version of Sonar Scanner or SonarQube Scanner for MSBuild is published,
thanks to crawlers written in groovy:
* https://github.com/jenkinsci/backend-crawler/blob/master/sonarrunner.groovy
* https://github.com/jenkinsci/backend-crawler/blob/master/msbuildsonarquberunner.groovy

For Hudson, it seems it is a manual process and we should ask on the hudson dev mailing list
for someone to update the json file.
