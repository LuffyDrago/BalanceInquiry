pipeline {
    agent any
     
    
    stages {
        stage('Run and Compile Code') {
             when {
                branch 'main'
            }
            steps {
                echo 'Running build automation'
                sh 'echo "vic" | sudosudo chmod -R 777 workspace/wso2am-micro-gw-toolkit-linux-3.2.0/bin/micro-gw'
                sh "micro-gw build BalanceInquiry --deployment-config /BalanceInquiry/conf/deployment-config.toml"
//               micro-gw build BalanceInquiry --docker --docker-image BalanceInquiry:v1 --docker-base-image wso2/wso2micro-gw:3.2.0
//                 micro-gw build BalanceInquiry --deployment-config /BalanceInquiry/conf/deployment-config.toml
//                 micro-gw build BalanceInquiry --deployment-config /BalanceInquiry/conf/deployment-config.toml  --micro-gw  /BalanceInquiry/conf/micro-gw.conf
//                 archiveArtifacts artifacts: '**/target/*.jar'
            }
        }
        

    }
}
