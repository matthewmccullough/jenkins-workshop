# Jenkins Workshop

## Resources
* Free [O'Reilly Jenkins eBook](http://www.wakaleo.com/books/jenkins-the-definitive-guide)

## Set up  Supporting Tools
* Git
    * Install Git*
    * Test that Git is working by running `git --version`
* Maven
    * Auto install option in Management console
    * Or install manually
    * Can have multiple versions in Jenkins administration
* JDK
    * Also available via auto-install
* Sonar
    * Manually install
* Gradle
    * Auto-install
    * Or run from wrapper
    * 1.0-milestone-6
* Ant
    * Auto install
    * 1.8.2

## Set up Jenkins
* Download Jenkins WAR*
* Run `java -jar jenkins.war` which runs on port 8080
* Alternatively, run on a different port `*java -jar jenkins.war --httpPort=8090`
* Test Jenkins is running by opening `http://localhost:8080`

## Echo Job
* New Job
* Freestyle
* echo "My Build Worked"

## SVN Checkout
* Built-in SVN plugin
* http://svn.apache.org/repos/asf/commons/proper/logging/trunk
* Freestyle project*
* Echo the contents of the LICENSE.txt

## Poll SCM
* Set to * * * * *
* Matthew will commit

## Jenkins Plugins
* 492 Plugins
* https://github.com/jenkinsci

## SCM Configuration
* Install Git
* SVN preinstalled
* 20 others

## SVN Checkout, Ant Build
* Add a Freestyle project
* Git version control
* https://github.com/apache/commons-io/tags/commons-io-2.1


## Git Source Code Jenkins Setup
* Path to a local repo
* Remember .git at end of local file path
* Set up a new Job
* `file://<YOURPATH>`

## Git Checkout, Ant Build
* Set up an Ant build with automatic install
* https://github.com/apache/commons-io
* Check out branch `commons-io-2.1`
* Ant manual install*
    * http://ant.apache.org/bindownload.cgi
    * Add to PATH environment variable
    * Test from command line with `ant`

## Set up a Maven Multi-Module Build
* Git hosted source
* https://github.com/wakaleo/game-of-life

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
* Password: workshop1

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
