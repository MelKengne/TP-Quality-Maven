pipeline {
    agent any

    tools {
        maven "Maven" 
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/MelKengne/TP-Quality-Maven.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Compilation de l\'application...'
                sh 'mvn clean compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Exécution des tests unitaires...'
                sh 'mvn test'
            }
        }
    }
}
