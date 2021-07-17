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
        post {
        always {
          emailext attachLog: true, body: '''Hi,

          Please Ignore this mail.

         Regards,
         Jenkins''', subject: 'Sample SCM Pipeline Run', to: 'shabhareesh456@gmail.com'
        }
    }
}
