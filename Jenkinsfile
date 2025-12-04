pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                echo 'Récupération du code...'
            }
        }
        
        stage('Build') {
            steps {
                echo 'Compilation du projet...'
                sh 'mvn clean compile'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Exécution des tests...'
                sh 'mvn test'
            }
        }
        
        stage('Package') {
            steps {
                echo 'Création du package...'
                sh 'mvn package'
            }
        }
    }
    
    post {
        success {
            echo 'Build réussi! ✓'
        }
        failure {
            echo 'Build échoué! ✗'
        }
    }
}
