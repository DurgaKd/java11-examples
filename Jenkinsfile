pipeline{
    agent { label 'MASTER'}
    stages {
        stage('scm') {
            steps {
                git branch: 'master' , url : 'https://github.com/DurgaKd/java11-examples.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }
    }
    post {
        success {
            archive '**/*.jar'
            junit '**/TEST-*.xml'            
        }
    }
}