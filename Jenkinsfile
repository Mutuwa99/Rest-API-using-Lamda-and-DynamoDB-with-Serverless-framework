pipeline {
    agent any

    environment {
        SONAR_SCANNER_HOME = tool 'sonarqube'
        // Other environment variables...
    }

    stages {
        stage('SonarQube Analysis') {
            steps {
                script {
                    // Run the SonarQube Scanner analysis
                    sh "${SONAR_SCANNER_HOME}/bin/sonar-scanner -Dsonar.projectKey=isaya -Dsonar.sources=. -Dsonar.host.url=http://54.227.109.162:9000 -Dsonar.login=sqp_73910cf48fb5b28718c4932858642fc01a090b56"
                }
            }
        }
        // Other stages...
    }

    post {
        success {
            echo 'SonarQube Analysis successful!'
        }
        failure {
            echo 'SonarQube Analysis failed!'
        }
    }
}
