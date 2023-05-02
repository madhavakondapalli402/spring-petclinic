pipeline {
   environment {
     git_url = "https://github.com/madhavakondapalli402/spring-petclinic.git"
     git_branch = "main"
   }

 agent {label 'PROD'}
 
  stages {
    stage('Pull Source') {
      steps {
        git branch: "${git_branch}", url: "${git_url}"
      }
     }
    
    stage('Maven Build') {
     steps { 
       sh "if [ -f \"pom.xml\" ];then mvn -B -f pom.xml clean package && cp target/*.jar .;else echo \"This is not a Java Project\";fi"
     }
    }
 //    stage('Docker Image Build') {     
 //       steps {
   //           sh 'sudo docker build -t demo-image . '
     //          }
       //      }
        //stage('Docker image push') {
          // steps {
                // sh 'aws ecr get-login-password --region ap-south-1 | sudo docker login --username AWS --password-stdin 738275578260.dkr.ecr.ap-south-1.amazonaws.com'
            //     withCredentials([usernamePassword(credentialsId: '53365e69-a023-4603-85f7-b233c2786e87', passwordVariable: 'Password', usernameVariable: 'Username')]) {
              //   sh "sudo docker login -u ${env.Username} -p ${env.Password}"
                // sh "sudo docker image tag demo-image demo-image:${BUILD_NUMBER}"
                // sh "sudo docker image tag demo-image salilkul87/demo-image:${BUILD_NUMBER}"
                // sh "sudo docker image push salilkul87/demo-image:${BUILD_NUMBER}" 
            //   } 
            // }  
         // }
    }
}
