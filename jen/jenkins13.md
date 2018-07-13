1.setup email notification.

For this first we download the emailnotifacation plugin, once download that goto manage jenkins and goto system configure here we configure the settings give smtp server and smtp port number and given mail and test the connection.before that goto gmail account and goto sign&amp;scutiry here we enable the smtp notification once enabled this, goto jenkins check the connection once it done.

Create one job here goto click on the add post build action once we done this configure we build the job means it will sent mail to recepient mail.

![email](https://github.com/malli2221/ops/blob/master/jen/jen11%202018-07-13%2017-57-05.png)

2. findbug, checkstyle,cobertura.

For this first we need to install the plugins once install the pulgin create one maven job then their we need to pass the maven goals like findbug,checkstyle once pass this plugin it will generate the code analysis report like graph.

What is the use of this plugin it will generate the code quality.

Cobetura: it is a plugin it is working has codequality means if we have 100 lines of code, we have to do the automation tesing those lines, using this pulgin we have check how many line was covered the automations tesing those kind of information we know.

3.dsl-job .

Today i leraned the maven job dsl .

def gitUrl = &#39;https://github.com/malli2221/mavenrepo.git&#39;

job(&#39;PROJ-unit-tests&#39;) {

    scm {

        git(gitUrl, &#39;master&#39;)

    }

    triggers {

        scm(&#39;\*/2 \* \* \* \*&#39;)

    }

    steps {

        maven{

           mavenInstallation(&#39;M2\_HOME&#39;)

                  goals(&#39;clean&#39;)

                  goals(&#39;compile&#39;)

                }

           }

}

![jen](https://github.com/malli2221/ops/blob/master/jen/jenkinst1%202018-07-13%2015-55-51.png)

mavenJob(&#39;example&#39;) {

    scm {

        github(&#39;https://github.com/malli2221/mavenrepo.git&#39;, &#39;master&#39;)

    }

    triggers {

        scm(&#39;\* \* \* \* \*&#39;)

    }

    goals(&#39;clean verify&#39;)

}

![jen](https://github.com/malli2221/ops/blob/master/jen/dsl1%202018-07-12%2017-24-25.png)
