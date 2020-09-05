pipeline {
    agent any
    stages {
        stage('Testing') {
            steps {
                echo 'Running build automation'
            }
        }
        stage ('Build') {
            steps {
                sh './gradlew build --no-daemon'
            }   
        }
        stage ('Post Build') {
            steps {
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        } 
    }
}
