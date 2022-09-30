pipeline {
    agent any
    stages {
        stage("run frontend") {
            steps {
                echo 'Executing yarn...'
                nodejs('node-1.5.1') {
                    sh 'yarn install yarn'
                }
            }
        }
        stage("run backend") {
            steps {
                echo 'Executing gradle...'
                withGradle() {
                    sh './gradlew -v'
                }
            }
        }
        stage("deploy") {
            steps {
                echo 'deploying the application...'
                
            }
        }
    }
}