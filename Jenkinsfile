pipeline {
    agent any
     
    
    stages {
        stage('Run and Compile Code') {
             when {
                branch 'main'
            }
            steps {
                echo 'Running build automation'
                
                bat 'micro-gw build --deployment-config conf/deployment-config.toml  --micro-gw  conf/micro-gw.conf' 
//                 micro-gw build BalanceInquiry --deployment-config /BalanceInquiry/conf/deployment-config.toml
//                 micro-gw build BalanceInquiry --deployment-config /BalanceInquiry/conf/deployment-config.toml  --micro-gw  /BalanceInquiry/conf/micro-gw.conf
//                 archiveArtifacts artifacts: '**/target/*.jar'
            }
        }
        

    }
}
