pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                // Установите нужные инструменты для сборки, если они еще не установлены
                sh 'g++ -o HelloWorld main.cpp'
            }
        }
    }
    post {
        success {
            archiveArtifacts artifacts: 'HelloWorld', onlyIfSuccessful: true
        }
    }
}
