pipeline {
    agent any
     
    
    stages {
        stage('Run and Compile Code') {
             when {
                branch 'main'
            }
            steps {
                echo 'Running build automation'
                sh 'micro-gw build BalanceInquiry --deployment-config  --micro-gw configuration/micro-gw-config' 
//                 archiveArtifacts artifacts: '**/target/*.jar'
            }
        }
        
       

        
//         stage('Login kubernetes') {
//            steps {
//                withKubeConfig([credentialsId: 'kubeconfigs', serverUrl: 'https://192.168.0.65']) {
//                     sh ''
//                }
                   
                  
               
//            }
//        }

        

        
//         stage('Build balance-inquiry image') {
//              when {
//                 branch 'master'
//             }
//             steps {
//                 echo 'Running build automation'
                
//                 sh 'mvn --settings configuration/settings.xml fabric8:build -Pkubernetes-deployment -DskipTests -Dfabric8.generator.spring-boot.name=USER_NAME'
               
                
                
//             }
//         }
        
//         stage('Tag and Push Image to DockerHub') {
//             when {
//                 branch 'master'
//             }
//             steps {
//                 script {
//                     docker.withRegistry('https://registry.hub.docker.com', 'docker_hub_login') {
//                         app.push("${env.BUILD_NUMBER}")
//                         app.push("latest")
//                     }
//                 }
//             }
//         }
        
//         stage('Deploy Balance-Inquiry Service') {
//              when {
//                 branch 'master'
//             }
//             steps {
//                 echo 'Running deploy automation'
//                 sh 'mvn fabric8:deploy -kubernetes'
                
                
//             }
//         }
     
    }
}