# Running this Implementation:
## Setup (For Windows 10 version 2004 and higher):
Open terminal as administrator, run command `wsl --install`

Open wsl

Clone this repository using `git clone https://github.com/jsongi/CS182Project1.git`

Go into the cloned repository directory using `cd CS182Project1`

### Installations for Java, Javac, and Maven
Run these commands:
```
sudo apt install openjdk-19-jre-headless
wget https://dlcdn.apache.org/maven/maven-3/3.9.6/binaries/apache-maven-3.9.6-bin.tar.gz
tar -xvf apache-maven-3.9.6-bin.tar.gz
mv apache-maven-3.9.6 /opt/
M2_HOME='/opt/apache-maven-3.9.36
PATH="$M2_HOME/bin:$PATH"
export PATH
```
Note: If unable to locate package, run `sudo apt update` and try again.

### Running the PUT:
Run these commands:
```
mvn clean
mvn package
javac -cp .:$(scripts/classpath.sh) SimpleTest.java
bin/jqf-random SimpleTest testSimpleTest 10
```

