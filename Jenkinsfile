pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Установите нужные инструменты для сборки, если они еще не установлены
                sh 'g++ -o HelloWorld simpleCode/simpleCode.cpp'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'HelloWorld', onlyIfSuccessful: true
        }
    }
}
