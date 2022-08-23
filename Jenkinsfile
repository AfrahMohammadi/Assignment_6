pipeline {
    agent any

    stages {
        stage('git repo & clean') {
            steps {
                //bat "rmdir  /s /q Assignment_6"
                bat "git clone https://github.com/AfrahMohammadi/Assignment_6.git"
                bat "mvn clean -f Assignment_6"
            }
        }
        stage('install') {
            steps {
                bat "mvn install -f Assignment_6"
            }
        }
        stage('tests') {
            steps {
                bat "mvn test -f Assignment_6"
            }
        }
        stage('package') {
            steps {
                 bat "mvn package -f Assignment_6"
            }
        }
    }
}
