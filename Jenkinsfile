pipeline {
    environment {
        git_url = "https://github.com/madhavakondapalli402/spring-petclinic.git"
        git_branch = "main"
    }
agent {label 'client3'}
//agent any

stages {
    stage('Pull Source') {
        steps {
            git credentialsId: '7d2579d6-a6e0-4e88-bc95-6eced99485a5', branch: 'main', url: 'https://github.com/madhavakondapalli402/spring-petclinic.git'
        }
    }
    stage('Maven Build') {
        steps {
            sh "if [ -f \"pom.xml\" ];then mvn -B -f pom.xml clean package && cp target/*.jar .;else echo \"This is not a Java Project\";fi"
        }
    }
    //stage('Docker Image Build') {
      //  steps {
        //    sh 'sudo docker build -t demo-image .'
       // }
    //}
    //stage('Docker image push') {
      //  steps {
        //    // sh 'aws ecr get-login-password --region ap-south-1 | sudo docker login --username AWS --password-stdin EC2-hostname' 
          //  withCredentials([usernamePassword(credentialsId: 'adc7e61a-2794-4830-b47c-6a1c50cabddd', passwordVariable: 'Password', usernameVariable: 'Username')]) {
            //    sh "sudo docker login -u ${env.Username} -p ${env.Password}"
              //  sh "sudo docker image tag demo-image demo-image:${BUILD_NUMBER}"
                //sh "sudo docker image tag demo-image hemasanku27/demo-image:${BUILD_NUMBER}"
                //sh "sudo docker image push hemasanku27/demo-image:${BUILD_NUMBER} "
               // }
           // }
        //}
    }
} 
