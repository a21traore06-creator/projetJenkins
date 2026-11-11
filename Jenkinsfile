pipeline {
    agent any

    options {
        timestamps()
    }

    stages {

        stage('Cloner le dépôt') {
            steps {
                echo 'Dépôt cloné'
            }
        }

        stage('Vérification du dépôt') {
            steps {
                bat 'git status'
            }
        }

        stage('Afficher le contenu du projet') {
            steps {
                bat 'dir'
            }
        }

        stage('Déploiement local') {
            steps {
                bat 'echo Le fichier index.html est pret a etre affiche'
            }
        }

        stage('Fin du build') {
            steps {
                bat 'echo SUCCESS'
            }
        }
    }

    post {
        success {
            echo 'Build OK'
        }
        failure {
            echo 'Build KO'
        }
    }
}