# EMF-IncQuery-RCPTT-GUI-Tests

## Jenkins configuration

1. Modify pom.xml
  * You have to change the following property
    * runnerPath, for example: /usr/rcptt.runner-incubation-1.5.6-N201504182315.zip
      * you can download it from here: https://eclipse.org/rcptt/download/
      * you will need the nightly build of "Test Runner"
    * the aut is automatically generated, add features and plugins, if you want to test new ones (in  application/product.product file)
    
1. Create new Jenkins Job. 

  Make these steps from step 3, you can use this GitHub repository:  
   http://support.xored.com/support/solutions/articles/3000028645-use-jenkins-to-run-rcptt-tests-in-continuos-integration-environment-

  To remove .git folder form workspace, use this shell command (if you don't add this build step, all tests will fail):

  <code>rm -rf $WORKSPACE/.git/</code>
  
  Remove this line from rcpttTests/pom.xml if you dont want coverage information with JaCoCo Jenkins Plugin:
  	<vmArg>-javaagent:/usr/jacoco/lib/jacocoagent.jar=destfile=/var/lib/jenkins/jobs/EMF-IncQuery-RCPTT-GUI-Tests/workspace/target/jacoco.exec</vmArg>

  More commands:

  <code>/usr/bin/metacity --display=$DISPLAY --replace --sm-disable & sleep 1</code>
  <code>/usr/bin/metacity-message disable-keybindings</code>

  To configure Xvnc (in Jenkins configuration):
  
  <code>Xvnc :$DISPLAY_NUMBER -geometry 800x600</code>


