Prerequisites
=============


### Installation 

####  Java 8
1. Install latest 8.x [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html) (not JRE)
2. Java Cryptography Extension (JCE)

    Download  "Java Cryptography Extension (JCE) Unlimited Strength Jurisdiction Policy Files" for 8 and install from [here](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
    Copy `local_policy.jar` and `US_export_policy.jar` to the `$JAVA_HOME/jre/lib/security` 
    for Mac: `/Library/Java/JavaVirtualMachines/jdk1.8.0_101.jdk/Contents/Home/jre/lib/security/`
    (Note: these jars will be already there so you have to overwrite them)

> test JCE is installed with `groovy TestUCE.groovy` command.

### Docker
1. Install Docker CLI and Docker Engine (Mac or Linux only)
2. Install OpenShift 3 CLI

### brew
Install kafkacat
```bash
# Mac distribution
$ brew install kafkacat
# Debian-based distributions such as Ubuntu:
$ apt-get install kafkacat
```
jmeter
```bash
brew install jmeter
```

### SDKMAN
get SDKMAN! from sdkman.io 

> On Windows: install SDKMAN via Git-Bash command prompt.

> And add respective executable paths to Windows PATH Environment variable.

Install following software 

    sdk i <software> <version>
     groovy 2.4.7
     grails 3.2.0
     kotlin 1.1-M01
     maven 3.3.9
     gradle  3.1
     springboot 1.4.1.RELEASE

```
spring install org.springframework.cloud:spring-cloud-cli:1.2.0.BUILD-SNAPSHOT
```

 
#### Infra Setup
Setup [Infrastructure](./infra) software. 

 