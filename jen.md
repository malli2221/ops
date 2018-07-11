Jenkins:

1.Run jenkins war on the top of a tomcat server.

 First i install java then i install maven after that i install tomcat on top the tomcat server i deploy the jenkinswar file, then configure the jenkins, on top of tomcat server.

https://www.howtoforge.com/tutorial/how-to-install-jenkins-with-apache-on-ubuntu-16-04/

2. Install any five plugin and use them.

 pulgins : 1. green ball plugin

        2.deploy to container

                    3. git

                    4.maven

                     5.diskspace

3. Install a plugin manually.

I installed &quot;nexus platform plugin&quot; first go to internet and download the plugin and go to manage jenkins here select the advanced tab browse the hpi file and upload that.

4.Create a freestyle job to print &quot;Hello world&quot;

 using helloworld program i created one job.using that git hub url i given in that job after that i build the job.

5.Create a job to clone your jenkins repo and cat a file from it.

 a. create new job in that job seclt copy from existing job option then save,it will clone the exsting job.

. List of the file inside directory.

 Workspace-helloworld-&gt; helloworld.java, README.md, text.

 i created one job like &quot;hello&quot; in this job using existing helloworld job clon e here







6. Increase and decrease number of executors and observe the build queue.

go to manage jenkins -&gt; go to configure system -&gt; build excutor (here we need to modified that excutor)

![build](https://github.com/malli2221/ops/blob/master/imgr/jenkins1%202018-07-11%2014-25-29.png)





7. unix based autuhentication pupose.

Go to manage jenkins -&gt; configure global security

8. matrix based authentication= for this i created one user after that go to manage jenkins -&gt; go to configure global security -&gt; here i selected that matrix based authentication here i added the user.

9. project based matrix= go to configure global security -&gt; here select the &quot;jenkins  user own data base&quot; again we need to select the &quot;project based matrix autorization stratefy&quot;.

We created one new job configure the job at that time we need to select the &quot;enable project-based secutiry&quot;





10.role based user authentication and autharization = for this we need to install the plugin  &quot;role based authorization strategy&quot;  then go to user

11. setup email notification.



12. integrate the slack to jenkins.

 First we need to install slack notification plugin then. Then go to slack click on setting-&gt; click add apps-&gt; here we need to select the jenkins and click on addconfigure then system generate the token, then go to jenkins here here click on the system configure then we need to integrate the slack to jenkins using the token id, then check the connection it working or not need to check testconnection.

![slack](https://github.com/malli2221/ops/blob/master/imgr/jenkins%2022018-07-11%2015-13-08.png)

13.Add a slave to your jenkins, restrict some of the job to your slave.

Go to manage jenkins-&gt; manage nodes click on the new node here we need to give remote directory , create lable name and remote machine ip address then save the setting and go to node  and lanuch the agent it will lanuch the connection, go to jenkins create new job and here we need to pass the slave jenkins lable name (lable-2)

![slave](https://github.com/malli2221/ops/blob/master/imgr/jenkins%2052018-07-11%2017-26-19.png)

14. Install below plugins ?

            Maven integration plugin

- Checkstyle Plug-in
- FindBugs Plug-in
- Static Analysis Collector Plug-in
- Cobertura Plugin

15. Install below softwares under Global tool configuration?

   I installed maven and integrate to jenkins, i download jdk 8 then using export keyword set the environment.

Using apt-get install git install the git.

16.Setup CodeStability Job?

 Here i choose the maven project using that i created one new job in jenkins here i pass the git url and pass maven goals has clean compile. I test that job.

I created the pom.xml

 &lt;project&gt;

&lt;modelVersion&gt;4.0.0&lt;/modelVersion&gt;

&lt;groupId&gt;com.jdevs&lt;/groupId&gt;

&lt;artifactId&gt;studentapp&lt;/artifactId&gt;

&lt;version&gt;2.5-SNAPSHOT&lt;/version&gt;

&lt;packaging&gt;war&lt;/packaging&gt;

&lt;/project&gt;

 ipass this pom.xml using maven golas clean and compile.
