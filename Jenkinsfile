pipeline {
    agent any
    stages {
        stage('Example') {
            steps {
                echo "Running ${env.BUILD_ID} on ${env.JENKINS_URL}"
                bat '''javac Test.java
                       java Test'''
            }
        }
    }
}
