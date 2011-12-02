# Jenkins Workshop

## Set up  Supporting Tools
* Git
* Maven
    * Auto install option in Management console
    * Head start by copying .m2/repository from USB
* JDK
    * Also available via auto-install
* Sonar
* Gradle

## Set up Jenkins
* Install Git plugin
* Remember .git at end of local file path

## SCM
* Git
* SVN preinstalled
* 20 others

* Git
    * Which branches to build
    * Merging branches as a pre-build and post-build step
    * Publishing result branches on success

## Compile Time Plugins
* Compiler warnings


## Archive
Choose which results of the build are saved permanently

## Fingerprints
* Choose which items to fingerprint
* Look up a fingerprint

## Collectors
* Junit
* TestNG
* Compiler warnings
* Parsing TXT, XML files

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
* Interactive JNLP
* Headless JNLP
* SSH
* EC2

* Usage graph (do you need more nodes)

## Monitoring
* JUnit report collector
* Code coverage graph

## Build Promotions
* Automatic promotion?
* Manual promotion (mark as success)

## Pipelines
* Plugin for showing connection from one job to another
