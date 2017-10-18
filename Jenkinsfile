pipeline {
    agent {
        docker {
            image 'maven:3-alpine' 
            args '-v /root/.m2:/root/.m2' 
        }
    }
    stages {
        stage('Build') { 
            steps {
                dir(path: 'microservices/spring/webfinger')
                sh 'mvn clean package' 
            }
        }
    }
}
