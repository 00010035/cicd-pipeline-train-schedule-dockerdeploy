pipeline {
    agent any
    stages {
        
        stage('Enter'){
            steps{
                echo 'Entering to my-project'
                sh 'cd my-project'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
        stage('Build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build --no-daemon'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip'
            }
        }
    }
}
