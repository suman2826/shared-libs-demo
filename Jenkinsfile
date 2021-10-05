@Library('jenkins-shared-library')  _
// welcomeJob()

// library identifier: 'jenkins-shared-library@main',
//     retriever: modernSCM([
//       $class: 'GitSCMSource',
//       remote: 'https://github.com/suman2826/jenkins-shared-libs.git'
// ])
// jenkinsForJava()

pipeline {
       agent any
      
       stages {
           stage("Tools initialization") {
               steps {
                     echo "${env.foo}"
                   echo "suman"
                     welcomeJob()
                     echo "${env.foo}"
//                      loadUtility()
                      echo "inside loadutility"
                      step{
                         checkout scm
                        def rootDir = pwd()
                        echo "${rootDir}"
                        def obj = load "${rootDir}/utilities.groovy"
                     //   def obj = load "vars/utilities.groovy"
                        echo "here"

                       echo "${obj.firstJob()}"
                      }
               }
           }
           
           
           stage("Running Testcase") {
              steps {
                   echo "completed"
               }
           }
           
       }
   }
