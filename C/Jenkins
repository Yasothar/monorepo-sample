pipeline {
    agent any

    stages {
        stage('Detect and Build Project C') {
            when {
                // This stage ONLY runs if changes occurred inside the 'C/' directory
                changeset "C/**"
            }
            steps {
                echo 'Changes detected in Project C. Starting build...'
                // Simulate your build commands here (e.g., npm run build, mvn clean package)
                dir('C') {
                    sh 'echo "Building Project C..."'
                    // If on Windows, use: bat 'echo Building Project C...'
                }
            }
        }
    }
    
    post {
        always {
            cleanWs() // Clean workspace after completion
        }
    }
}