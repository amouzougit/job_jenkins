pipeline {
    agent any
        tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven"
    }
    stages {
        stage('Clonage du dépôt') {
            steps {
                // Cloner le dépôt Git
                git branch: 'master', url: 'https://github.com/amouzougit/job_jenkins.git'
            }
        }

        stage('Build') {

            steps {
                
                // Exécuter le build Maven
                bat 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Exécuter les tests Maven
                bat 'mvn test'
            }
        }
    }
}