pipeline{
    agent {
      label "Node1"
    }
    tools {
        maven 'Maven3'
    }
    stages {
        stage('Build Maven') {
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/pgnaik/MyApp1.git']])
                bat "mvn clean package"
                
            }
        }
    }
}

