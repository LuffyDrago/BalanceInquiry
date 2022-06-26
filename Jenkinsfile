pipeline {
    agent any
     
    
    stages {
        stage('Run and Compile Code') {
             when {
                branch 'main'
            }
            steps {
                echo 'Running build automation'
                
                sh 'micro-gw build BalanceInquiry --deployment-config conf/deployment-config.toml' 
                archiveArtifacts artifacts: '**/target/*.jar'
            }
        }
        

    }
}
