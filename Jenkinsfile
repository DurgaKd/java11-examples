node('MASTER') {
    stage('scm') {
        git 'https://github.com/DurgaKd/java11-examples.git'
    }
    stage('build') {
        sh 'mvn package'
    }
     stage('postbuild') {
        junit '**/TEST-*.xml'
        archive '**/*.jar'
    }
}