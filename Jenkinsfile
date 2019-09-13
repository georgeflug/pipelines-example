pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                bat 'gradlew check'
            }
        }
        stage('Build') {
            steps {
                bat 'gradlew build'
            }
        }
        stage('Deploy') {
            steps {
                bat 'gradlew publish'
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
