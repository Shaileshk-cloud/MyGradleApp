pipeline{
     agent any
     tools{
         maven 'Maven'
     }
     stages{
         stage('Checkouts'){
            steps{
                git branch :'master',url:'https://github.com/Shaileshk-cloud/MyGradleApp.git'
            }
         }
         stage('Build'){
            steps{
                sh 'gradle build'
            }
         }
         stage('Test'){
             steps{
                sh 'gradle test'
             }
         }
         stage('run application'){
            steps{
                sh 'gradle run'
            }
         }
         }
       post{
           success{
                echo 'pipeline successful'
           }
           failure{
              echo 'pipeline failure'
           }
       }
 }
