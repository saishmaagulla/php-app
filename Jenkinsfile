pipeline{
     environment {
     FOO = "foo"
     GIT_SHA = sh (
         script: "git log -1 --pretty=%h",
         returnStdout: true
         ).trim()
   }
 agent any
 stages{
      stage('build') {
        steps{
        echo 'this is build step'
          sh """
          
          echo ${FOO}
          echo "${GIT_SHA}"
          """
        }
      }
    }}
