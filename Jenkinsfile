pipeline {
    agent any

    stages {
        stage('Build Project A') {
            when {
                changeset "A/**"
            }
            steps {
                echo 'Detected changes in Project A. Building...'
                dir('A') {
                    bat 'echo "Running build for A..."'
                }
            }
        }

        stage('Build Project B') {
            when {
                changeset "B/**"
            }
            steps {
                echo 'Detected changes in Project B. Building...'
                dir('B') {
                    bat 'echo "Running build for B..."'
                }
            }
        }

        stage('Build Project C') {
            when {
                changeset "C/**"
            }
            steps {
                echo 'Detected changes in Project C. Building...'
                dir('C') {
                    bat 'echo "Running build for C..."'
                }
            }
        }
    }

    post {
        cleanup {
            cleanWs()
        }
    }
}