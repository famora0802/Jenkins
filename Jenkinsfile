pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Commandes de build ici
            }
        }
        stage('Test') {
            steps {
                echo 'Testing...'
                // Exécution du script Python EasyTest.py
                script {
                    def pythonScript = 'EasyTest.py'
                    def command = "python ${pythonScript}"
                    def result = bat(script: command, returnStatus: true)
                    if (result != 0) {
                        error "Python script failed with status ${result}"
                    }
                }
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploying...'
                // Commandes de déploiement ici
            }
        }
        stage('Notify') {
            steps {
                echo 'Notifying...'
                // Commandes de notification ici
            }
        }
    }
}