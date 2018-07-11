Nexus :

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

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus%202018-07-11%2011-24-21.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus2%202018-07-11%2011-24-04.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus3%202018-07-11%2011-24-40.png)

![nexus](https://github.com/malli2221/ops/blob/master/imgr/nexus4%202018-07-11%2011-27-22.png)
