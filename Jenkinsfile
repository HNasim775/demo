pipeline {
    agent any
    stages {
        stage("Clone") {
            steps {
                echo 'Cloning repository...'
                // Ajoutez ici la commande pour cloner le référentiel Git
                // Exemple : git clone <URL_DU_REPO>
            }
        }
        stage("Empty current directory and git clone") {
            steps {
                echo 'Emptying current directory...'
                // Ajoutez ici la commande pour vider le dossier courant
                // Exemple : rm -rf ./*
                echo 'Cloning repository...'
                // Ajoutez ici la commande pour cloner le référentiel Git
                // Exemple : git clone <URL_DU_REPO>
            }
        }
        stage("Build") {
            steps {
                echo 'Building...'
                // Ajoutez ici les commandes pour construire votre application
                // Exemple : mvn clean install
            }
        }
        stage("Change directory and build") {
            steps {
                echo 'Changing directory...'
                // Ajoutez ici la commande pour vous déplacer dans le dossier cloné
                // Exemple : cd <NOM_DU_DOSSIER_CLONE>
                echo 'Building...'
                // Ajoutez ici les commandes pour construire votre application à partir du dossier cloné
                // Exemple : mvn clean install
            }
        }
        stage("Run") {
            steps {
                echo 'Running application...'
                // Ajoutez ici les commandes pour lancer votre application
                // Exemple : java -jar <NOM_DU_JAR>
            }
        }
        stage("Final Echo") {
            steps {
                echo 'Pipeline execution completed!'
            }
        }
    }
}