pipeline {
    agent any
     
    
    stages {
        stage('Run and Compile Code') {
             when {
                branch 'main'
            }
            steps {
                echo 'Running build automation'
                echo 'workspace'
                sh 'echo workspace/wso2am-micro-gw-toolkit-linux-3.2.0/bin/micro-gw'
                sh "${env.workspace}/wso2am-micro-gw-toolkit-linux-3.2.0/bin/micro-gw micro-gw build BalanceInquiry --deployment-config /BalanceInquiry/conf/deployment-config.toml"
              
            }
        }
          
        stage('Tag Image') {
            when {
                branch 'master'
            }
            steps {
                script {                       

                        sh "docker tag kcbbalanceinquirymock:latest kcbbalanceinquirymock"
                        
                        
                }
            }
        }
        
        stage('Deploy Balance-Inquiry Service') {
             when {
                branch 'master'
            }
            steps {
                script {
                         
                        echo 'Running build automation'
                        withKubeConfig([credentialsId: 'kubeconfigs', serverUrl: 'https://192.168.0.65:6443']) {


                            sh "mvn --settings configuration/settings.xml fabric8:deploy -Pkubernetes-deployment -DskipTests -Dfabric8.generator.spring-boot.name='${repo_name}:${env.tag}'" 
       
                        }
                    
                    
                }
                
            }
        }
        

    }
}
