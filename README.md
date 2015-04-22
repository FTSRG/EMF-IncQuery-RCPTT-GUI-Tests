# EMF-IncQuery-RCPTT-GUI-Tests

## Jenkins configuration

1. Modify pom.xml
  * You have to change the following properties:
    * autPath, for example: /usr/eclipse-IncQuery-AUT/
    * runnerPath, for example: /usr/rcptt.runner-incubation-1.5.6-N201504182315.zip
    
1. Create new Jenkins Job. 

Make these steps, use this GitHub repository:  
http://support.xored.com/support/solutions/articles/3000028645-use-jenkins-to-run-rcptt-tests-in-continuos-integration-environment-

To remove .git folder form workspace, use this shell command:

<code>rm -rf $WORKSPACE/.git/</code>

More commands:

<code>/usr/bin/metacity --display=$DISPLAY --replace --sm-disable & sleep 1</code>
<code>/usr/bin/metacity-message disable-keybindings</code>

To configure Xvnc:
<code>Xvnc :$DISPLAY_NUMBER -geometry 800x600</code>

