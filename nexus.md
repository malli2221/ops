Nexus :

what is the use of nexus:

 Nexus is a repository manager, it stores &quot;artifacts&quot;.

we&#39;re usually talking about tens to hundreds of developers (sometimes thousands of developers) split into different groups each with a distinct focus.

For example, think about a large, international bank. Such an organization will likely employ thousands of developers spread throughout the world,There might be a hundred developers in San Francisco focused on web development, with tens of developers in New York focused on market feed and data integration. Maybe there is a group that focuses on back office operations in Toronto, and a group dedicated to international clients in Dubai, and another development group in Bangalore.

Repository Managers

This brings us to the final component of efficient development infrastructure - repository managers

**Repository Managers:** You can think of a repository like you would think of a library. It is a server that stores and retrieves files, which we refer to as artifacts. When you write a piece of software, you are often depending on external libraries.

What is Nexus? for the Non-programmer

think of it as a library. You can ask it for &quot;artifacts&quot;, it will store and retrieve them and assign a standard coordinate system to the artifacts it stores. If you are developing software, having this facility available allows you to catalog and store your own artifacts using the same &quot;numbering&quot; system that the library uses. When a group develops a new system or a library, they submit it to the repository manager. Other groups then have a standard way to access these libraries.





  nexus is central repository tool here we have  save the war/jar in to the nexus reposiotry, once jenkins generate the war/jar it will stored into nexus, for this we need to do some comfiguration, first download the nexus and install the nexus in our local machine then start the nexus.

Go to jenkins -&gt; go to manage jenkins-&gt; goto system config-&gt; select the sonatype nexus here we have to given the  nexus url and user name and passwd this the way we need to integrate the jenkins with nexus.

Repository: once launch the nexus, go to repository here we need to create the repository once create the repository it will generate the url using that url we need to into pom xml,

configarions:

 in pom.xml we create distributedmanagement tag under the this tag we have to mention the id and repo name and repository url we have given.once we done those configrure go to jenkins to create the job and build the job using maven goals like &quot;deploy&quot;, it build the job and delpoy the war into paticular file.

&lt;repository&gt;

            &lt;id&gt;deployment&lt;/id&gt;

            &lt;name&gt;Internal Releases&lt;/name&gt;

            &lt;url&gt;http://localhost:8081/repository/sample-rel/&lt;/url&gt;

        &lt;/repository&gt;

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus%20o%202018-07-16%2011-16-39.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus%202018-07-11%2011-24-21.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus2%202018-07-11%2011-24-04.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus3%202018-07-11%2011-24-40.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus4%202018-07-11%2011-27-22.png)
