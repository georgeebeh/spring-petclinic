pipeline {
    agent any
    tools {
        maven 'maven3.9'
    }

    stages {
        stage('SonarQube analysis 1') {
            steps {
                sh 'mvn clean package sonar:sonar -Dsonar.token=SONAR_TOKEN'
            }
        }
        /*stage('build && SonarQube analysis') {
            steps {
                 withSonarQubeEnv('Sonar Scanner') {
                    // Optionally use a Maven environment you've configured already
                    withMaven(maven:'Maven 3.9') {
                        sh 'mvn clean package sonar:sonar'
                    }
                }
            }
        }*/
    }
}
