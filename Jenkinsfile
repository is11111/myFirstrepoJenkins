pipeline {
    agent any
    
    

    stages {
        stage('Build') {
            steps {
                echo 'Build Start'
                
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: '02eb3dd3-86d7-4359-be72-b9f3948ca9b9', url: 'https://gitlab.com/bttraining/jenkinjavalab.git']])
                
                sh 'mvn -B -DskipTests clean package'
                
                echo 'Build Finished'
            }
        }
    } 
}