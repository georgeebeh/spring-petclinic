pipeline {
    agent any
    tools {
        maven 'maven3.9'
    }

    stages {
        /*stage('SCM') {
            steps {
                git url: 'https://github.com/georgeebeh/spring-petclinic.git'
            }
        } */
        stage('build && SonarQube analysis') {
            steps {
                 withSonarQubeEnv('My SonarQube Server') {
                    // Optionally use a Maven environment you've configured already
                    withMaven(maven:'Maven 3.9') {
                        sh 'mvn clean package sonar:sonar'
                    }
                }
            }
        }
    }
}
