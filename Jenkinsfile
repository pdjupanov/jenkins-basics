pipeline {
    agent any

    tools {
        //Install the configured Maven version as M399 --> Maven 3.9.9
        maven "M399"
    }

    stages {
        stage ('Test maven version') {
            steps {
                sh 'echo Print Maven version'
                sh 'mvn -version'
            }
        }
        stage ('Build app') {
            steps {
                //Run maven package CMD
                sh "mvn clean package -DskipTests=true"
            }
        }
        stage ('Test app') {
            steps {
                sh "mvn test"
            }
        }
    }
}
