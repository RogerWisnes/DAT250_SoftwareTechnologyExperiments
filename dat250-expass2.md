# DAT250: Software Technology Experiment Assignment 2
## Task statement:
### Introduction
The goal of this assignment is to make some initial experiment with the Java Persistence Architecture (JPA). This will include setting up a database for experimentation and study object-relational mapping.

### Installation: Derby Database

Download and install the Apache Derby database by going through the tutorial which can be found here: http://db.apache.org/derby/papers/DerbyTut/index.html

### Experiment 1: Application using JPA
Setup a Java application which uses JPA for storing entities in a database based on the following tutorial:
https://www.vogella.com/tutorials/JavaPersistenceAPI/article.html#installation

You may also use the Maven project found at the following repo, as a starting point:
https://github.com/lmkr/dat250-jpa-examples/tree/master/eclipselink/jpa-basic

Find a way to inspect the database tables being created - either from the IDE or by logging into the database server.

### Experiment 2: Banking/Credit Card example JPA
Try to implement the domain model for credit cards corresponding to the small assignment that was introduced in the last lecture video on object-relationship mapping. Does the tables created correspond to your initial answer to the exercise.

# Hand-in report
### Technical problems
Through this experiment I encountered three main problems:

**Problem 1:**
During installation of Derby, when configuring JDK, the path and java_home did not work toghether. I quickly found out that there was some mismatch in java-version, so this should be a quick fix (since I encountered the same problem in assignment 1). However, this time the problem did not disappear. 

I set the path to point to the java_home-variable, and set the java_home to point to jdk-14, but still, when I executed "java -version" in cmd / PS it clearly stated that I had jdk-1.8 and nothing worked as it should.

After ages of searching online, I figured that I had an unused system variable that pointed to the wrong java-version. This variable was listed before java_home (in path), and thereby interferred with the connection between path and java_home. Moving java_home further up in the variable-list (above the other one), fixed this problem.

**Problem 2:**
As if the first problem did not waste enough time, when I finally got to Experiment 1, I soon enough encountered a new problem. Following the given tutorial, I was told to import three .jar-files to a lib-folder, and adding them to classpath. This prooved to be a lot more frustrating than I anticipated.

- Eclipse's tutorial states the following: "To add JAR file located in the project to its classpath, right-click on the JAR file and select Build Path > Add to Build Path", and so I did. This, however, did not add the jar-files to classpath, but instead to module-path. This did not work. When I finaly found this issue, I went into settings and moved the files to classpath. Problem solved.

- Or so I thought. Now I got an error stating that the import javax.persistence(...) could be found in two of the jar-files, and just choosing one of them seemed to be impossible. Moving some of the jar-files back to module-path fixed **this** issue, but produced a wide variety of other error-messages. Once again, I had to pray to the great god of Google, and make great sacrifices of time. However, it seemed that all fixes I could find required me to have a maven-project, but following the tutorial, I had a standard java-project. The fix for this problem ended up being to delete the javax-jar, and reimport it to lib.

- Finally the code itself gave no errors, so I could compile the code for the first time. Result: java.lang.NoClassDefFoundError. Again: All fixes I could find required a maven-project so that I could easier use dependensies. Now I gave up hope on the JPA-tutorial, and converted to a maven-project. Now I could follow the instructions given at the github-repo that was given in the assignment-description. But to no avail. I still got the same error. All fixes I could find was just as disappointing as the previous one. After too much time wasted, I ended up starting from scratch with a completely new maven-project. 

- Still, I got the same error, but the road to that error was shorter. I therefore deleted the project again, redownloaded the jar-files, gave up Eclipse, and tried once again with IntelliJ. Finally, absolutely everything in the simpleDB-tutorial worked.

**Problem 3:**
Described in pending issues.

### Link to code
Link to last code for experiment 1:
https://github.com/RogerWisnes/de.vogella.jpa.eclipselink

### Database-inspection
I tried setting up Apache Derby database-tool in IntelliJ, but I encountered a new problem where I could not connect to the database. I did not have the time to work any further on this issue.

### Pending issues
At last, the pending issue would indirectly be considered time. Because of the two major issues described previously, I did not get the chance to complete the assignment.

Still working on experiment 1, I completed the tutorial, and was going to start on inspecting the database, but I could not connect to it.
As a result, I could not start on experiment 2, and I could not complete experiment 1.
