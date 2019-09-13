pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh './gradlew check'
            }
        }
        stage('Build') {
            steps {
                sh './gradlew build'
            }
        }
        stage('Deploy') {
            steps {
                sh './gradlew publish'
            }
        }
    }
}

def runGradleTask(task){
    if (isUnix()) {
        sh "./gradlew $task"
    } else {
        bat "gradlew $task"
    }
}
