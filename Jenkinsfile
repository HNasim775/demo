pipeline {
    agent any
    stages {
        stage("Clone") {
            steps {
                echo 'Cloning repository...'
                git branch: 'main', URL: https://github.com/HNasim775/demo.git
            }
        }
        stage("Empty current directory and git clone") {
            steps {
                echo 'Emptying current directory...'
                rm -rf ./
                echo 'Cloning repository...'
                https://github.com/HNasim775/demo.git
            }
        }
        stage("Build") {
            steps {
                echo 'Building...'
                clean install compile test package verify 
            }
        }
        stage("Change directory and build") {
            steps {
                echo 'Changing directory...'
                cd .\demo
                echo 'Building...'
                mvn clean install
            }
        }
        stage("Run") {
            steps {
                echo 'Running application...'
                java -jar /var/jenkins_home/workspace/MonPremierMAVEN/target/demo-1.0-SNAPSHOT.jar
            }
        }
        stage("Final Echo") {
            steps {
                echo 'Pipeline execution completed!'
            }
        }
    }
}