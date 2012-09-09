# Jenkins Workshop
This is the Jenkins Continuous Integration workshop run by Matthew McCullough.

This latest version of this page can be found at <https://github.com/matthewmccullough/jenkins-workshop>

## Resources
* Download the free [O'Reilly Jenkins eBook](http://www.wakaleo.com/books/jenkins-the-definitive-guide).
* Review Matthew's [curated Jenkins bookmarks](http://delicious.com/matthew.mccullough/jenkins).

## Set up  Supporting Tools
* Git
    * Test if you already have Git installed by typing `git --version`
    * If needed, install Git from platform-specific binary installers
    * After install, test that Git is working by running `git --version`
* Maven
    * Available as *Auto install* option in Jenkins Management page
    * Or install manually
    * Can have multiple versions in Jenkins administration
* JDK
    * Available as *Auto install* option in Jenkins Management page
* Sonar
    * Manually install
    * Only used in today's workshop if already installed
* Gradle
    * Available as *Auto install* option in Jenkins Management page
    * Can also be auto-downloaded via Gradle wrapper
    * 1.0-rc-2
* Ant
    * Available as *Auto install* option in Jenkins Management page
    * 1.8.3

## Set up Jenkins
* Download Jenkins WAR from local content server or ['http://jenkins-ci.org'](http://jenkins-ci.org)
* Run `java -jar jenkins.war` which runs on port 8080
* Alternatively, run on a different port `java -jar jenkins.war --httpPort=8090`
* Test Jenkins is running by opening [`http://localhost:8080`](http://localhost:8080)

## Echo Job
* Create a new Freestyle job named `echojob`
* Add an *Execute shell* build step or *Execute Windows batch command* as appropriate for your OS.
* In the build step, echo some text with `echo MyBuildWorked`

## Jenkins Plugins
* 543 Plugins
* https://github.com/jenkinsci

## SCM Configuration
* The SVN plugin is preinstalled
* Manually install the Git plugin and restart Jenkins
    * Click the "Manage Jenkins" link
    * Click the "Manage Plugins" link
* Review ~20 others that I typically use

## SVN Checkout
* We'll use the built-in SVN plugin
* Create a new Freestyle job named `svncheckout`
* Add source code URL `http://svn.apache.org/repos/asf/commons/proper/logging/trunk`
* Add an *Execute shell* build step or *Execute Windows batch command* as appropriate for your OS.
* In the build step, echo the contents of the `LICENSE.txt` file.
    * Add script contents: `cat LICENSE.txt`

## Poll SCM
* Create a new Freestyle job named `pollscm`
* Turn on the *Source Code Management* radio button labeled *Git*
* Add Repository URL `https://github.com/matthewmccullough/hellogitworld/trunk`
* Turn on the *Build Trigger* labeled *Poll SCM*.
* Set the frequency to `* * * * *`
    * This indicates *every one minute of every day*
* Matthew will commit a change to cause the students SCM polling to find an update
* Click the *Git Polling Log* link to view the history of polling

## SVN Checkout, Ant Build
* Create a new Freestyle job named `svnantbuild`
* Turn on the *Source Code Management* radio button labeled *Subversion*
* Add Repository URL `https://github.com/apache/commons-io/tags/commons-io-2.1/`
* Yes, this is a Subversion checkout from GitHub

## Git Source Code Jenkins Setup
* Path to a local repo
* Remember .git at end of local file path
* Set up a new Job
* `file://<YOURPATH>`

## Git Checkout, Ant Build
* Set up an Ant build with automatic install
* `https://github.com/apache/commons-io`
* Check out branch `commons-io-2.1`
* Ant manual install
    * <http://ant.apache.org/bindownload.cgi>
    * Add to PATH environment variable
    * Test from command line with `ant`

## Set up a Maven Multi-Module Build
* Git hosted source
* `https://github.com/wakaleo/game-of-life`

## Advanced Git Configuration
* Git
    * Which branches to build
    * Merging branches as a pre-build and post-build step
    * Publishing result branches on success
* Parameters
    * Can pass through SHA1

## Compile Time Plugins
* Compiler warnings
* Violations plugin

## Email Notification
* Basic and Advanced
* SMTP: smtp.gmail.com
* User: workshopsender@gmail.com
* Password: workshop12

## Remote Trigger URLs
* Secret URL to invoke a build
* http://localhost:8080/job/GradleTest/build?token=1111
* Can be CURLed

## Archive
* Choose which artifacts of the build are saved permanently
* Glob pattern

## Fingerprints
* Choose which items to fingerprint
* Look up a fingerprint

## Collectors
* Junit
* TestNG
* Compiler warnings
* Parsing TXT, XML files

## Monitoring
* JUnit report collector
* Code coverage graph

## Post-build Steps
* Promote
* Announce
* Blame developer with commits
* Send mail on success or failure

## Project Dependencies
* Dependency graphs of projects
* GraphViz CLI tool `dot`

## Radiators
* Dashboard
* Adding more columns to primary view
** Cron schedule
** Type
* Filtering primary view (tabs)

## Slaves
* Types
    * Interactive JNLP
    * Headless JNLP
    * SSH
    * EC2
* Usage graph (do you need more nodes)

## Build Promotions
* Automatic promotion?
* Manual promotion (mark as success)

## Pipelines
* Plugin for showing connection from one job to another

## Command Line
* Download the JAR
* Get help `java -jar jenkins-cli.jar -s http://localhost:8080/ help`
