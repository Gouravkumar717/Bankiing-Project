pipeline {
    agent any
    tools {
        maven "M2_HOME"
    }
    stages {
        stage ("Clone and Build") {
            steps {
                // Use credentials and specify the correct branch
                git branch: 'main', url: 'https://github.com/Gouravkumar717/Bankiing-Project.git', credentialsId: 'git-cread'
                
                // Build the project with Maven
                sh "mvn -Dmaven.test.failure.ignore=true clean package"
            }
        }
    }
}
