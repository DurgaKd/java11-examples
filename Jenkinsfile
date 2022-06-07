node('MASTER') {
    stage('scm') {
        git 'https://github.com/DurgaKd/java11-examples.git'
    }
    stage('build') {
        sh 'mvn package'
    }
    stage('postbuild') {
        archive '**/*.jar'
        junit '**/TEST-*.xml'
    }
}