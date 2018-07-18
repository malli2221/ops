mavenJob('BigParser_BE_websockets-Deploy_QA'){
description('I ll do BE websockets continuous deployment of all components available in Bigparser_Backend')  

  logRotator {
       daysToKeep(60)
       numToKeep(20)
      Today : 19-7-2018

dsl job : today i have to take one job in bigparser (BigParser\_BE\_websockets-Deploy\_QA) i created   job using groovy script.

mavenJob(&#39;BigParser\_BE\_websockets-Deploy\_QA&#39;){

description(&#39;I ll do BE websockets continuous deployment of all components available in Bigparser\_Backend&#39;)

  logRotator {

       daysToKeep(60)

       numToKeep(20)

    }

  scm {

   git {

     remote {

       url(&quot;git@github.com:BigParser/BigParser\_WebSockets\_Server\_BE.git&quot;)

     }

      branch(&quot;\*/master&quot;)

   }

 }

  triggers {

        scm(&#39;H/2 \* \* \* \*&#39;)

    }

  wrappers {

    environmentVariables{

    propertiesFile(&#39;/var/lib/jenkins/scripts/qa/email\_recipient&#39;)

  }

}

  preBuildSteps{

    shell{

      command(&#39;bash /var/lib/jenkins/scripts/qa/qa\_tag\_details/tag\_details\_Websockets\_BE.sh&#39;)

    }

  }

  goals(&#39;clean package&#39;)

  postBuildSteps{

    shell{

      command(&#39;bash /var/lib/jenkins/scripts/qa/backend/qa\_backend\_websockets\_deploy.sh ${RELEASE\_ID}&#39;)

    }

  }

  publishers{

        extendedEmail {

         recipientList(&#39;$BACKEND\_RECIPIENT&#39;)

          replyToList(&#39;$DEFAULT\_REPLYTO&#39;)

          contentType(&#39;text/html&#39;)

          defaultSubject(&#39;$DEFAULT\_SUBJECT QA Environment&#39;)

          defaultContent(&#39;${SCRIPT,template=&quot;qa-be-email-html.template&quot;} \nBackend Chatbot data deployed&#39;)

          triggers {

            always {

              sendTo {

                developers()

                recipientList()

              }

            }

          }

        }

}

}

Jenkins :

Parametarized job :

we need to pass the parametra and build the job,why we need use this parametra means, you need to

build your job in paticular server means this senario we use this,for this we need to install parametra

plugin, once install pass the parametra like (dev, stg, qa,pro)this we need to pass the parametra,

once pass the peramatra then given the github url then given to maven golas once you done this save the job.when ever you need to build the job means it will ask the parametra.

![tar](https://github.com/malli2221/ops/blob/master/imgt/para%202018-07-17%2018-48-43.png)



Tag :

why we need to use the tag means ever new release will going to release we need to create tag,

when ever we have to do commit for paticular commit id we need create a tag once we create tag for the commit id then push the tag into github then we need to take the github url, using this url we will create the  job in our jenkins, in jenkins we need to select the git parametra then given the tag name then given the branch after that pass maven golas then select the buildwithparametra using the tag name.

![tag](https://github.com/malli2221/ops/blob/master/imgt/tag%202018-07-17%2018-49-34.png)

Maven dsl job:

using groovy script i create one job and this job i have to given the checkstyle and findbug goals regarding codestatic analysis.

mavenJob(&quot;CodeStaticAnalysis&quot;) {

description(&quot;Code static job through DSL&quot;)

scm {

  git {

    remote {

      url(&quot;https://github.com/malli2221/mavenrepo.git&quot;)

      credentials(&#39;malli2221&#39;)

    }

     branch(&quot;\*/master&quot;)

  }

}

  triggers{

       cron (&#39;\*/30 17 17 7 2&#39;)

        }  mavenInstallation(&#39;default&#39;) // Select which installation of Maven to uses

rootPOM(&#39;pom.xml&#39;)

goals(&#39;clean compile findbugs:findbugs checkstyle:checkstyle&#39;)

publishers {

  checkstyle(&#39;\*\*/target/checkstyle-result.xml&#39;) // Publish the checkstyle report

  }

publishers {

  findbugs(&#39;\*\*/target/findbugsXml.xml&#39;)

}

}

![find](https://github.com/malli2221/ops/blob/master/imgt/findbug%202018-07-17%2018-47-59.png) 
