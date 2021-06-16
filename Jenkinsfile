pipeline {
       agent any {

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Code sync') {
          steps {
                git branch: 'master', url: 'https://github.com/aksinha0908/simple-java-maven-app'
           }
        }
        stage('Build') {
            steps {
                echo "Code Build Process"
        }
    }
        stage("Test") {
            steps {
                    echo "Test the executions process"
            }
        }
        stage("Deploy") {
            steps {
                    echo "Software deployment process"
            }
        }
    }
    post {
        always {
            
            mail bcc: '', body: '''Hello,

Welcome to Jenkins E-mail alert

Thanks,
Amit Kumar Sinha''', cc: '', from: '', replyTo: '', subject: 'Jenkins Job', to: 'amitkumar.sinha@sasken.com'
        }
    }
}
