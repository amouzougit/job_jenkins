pipeline {
    agent any

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
