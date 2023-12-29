pipeline {
    agent any
    tools {
        mvn 'maven3.9'
    }

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                echo 'This is the first pipeline for this server'
            }
        }
        stage('Build') {
           steps {
                sh mvn package
            }        
        }
    }
}
