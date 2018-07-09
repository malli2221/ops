Maven:

Requirement: before install maven we need jdk in our local system.

Maven environment setup:  first we have to download the maven.tar.gz then extraxt the file then using the file we have set the env setup.

using expport variable we will set the environment setup.

 export M2\_HOME=/opt/install/maven 3.5.5

  export PATH=$M2\_HOME/$PATH:

Pom contains the goals and plugins

groupid: this is an id of project group, this is unique an organization or a project.

Artifactid: this is an id of project, this is generally name of the project.

Version: this is the version of the project, it is used with in artifact repository to seprate the version from each other.

We need to check the effective form in out current project using the command like &quot;mvn help:effacctive-pom &quot;.



Maven build lifecycle:

validate: using this goal we will validate entire project is correct and necessary information is availble or not.

compile: using this goal we will compile the entire project code compilation is done in this phase.

Test: using this goal we will tests the compilatiion is done in this testing framwork.

Package: this phase creates the jar/war/ear package as we mentioned inthe packaging in pom.xml

install: using this goal install the packages in local/remote maven repository.

Deploy: using this goal copy the final copy to remote repository.

Command : mvn archetype:generate using this command we will download the maven dependent plugin download to our local maven repositoory.

What is a maven repository:

in maven repository is a directory where all the projects jars, libary jar, plugins or any other project specifcation artifacts are stored and can be used by maven.

Maven repository is three type:

1.local

2.central

3.remote.

Local: maven local repositiry is folder it is localted in our localmachine when every the first time we will run mvn command first it will download the all dependencies plugin into our local machine.when reuse the same plugin in any other project simple it will goto .m2 folder and using the locally stored plugins.

Central repository : central reposotiry is provided by maven community, it contains a large number of commonly  used libraries.



Remote: sometime maven does not find the a mentioned denpendency in central repository as well . It stop the build process and output error message to console output. For this senario devlopers own custom repository contaning required libaries or other project jar.

Maven project structure:

1. source ; innside the source we haveing main and java :  src/main/java

2 . source : contains test java code files under the package structure: src/main/test/

3. pom.xml.

What is the snapshot:

snapshot is a version it indicates the current development copy.

Maven integrate with jenkins:

in jenkins we have to integrate the maven to jenkins, for this first we have to set the environment variable in our linux machine using export keyword after that to jenkins there to manage jenkins got o gobal configure there we have to given the maven local path.
