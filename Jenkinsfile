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
                // Exécuter le build Maven with the release flag
                bat 'mvn clean package -Dmaven.compiler.release=14'
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
