
pipeline {
    agent any  // Specifies that the pipeline can run on any available agent (node)
 options {
        skipStagesAfterUnstable()
    }
    stages {
        stage('Test') {  // Defines a stage named 'Test'
            steps {
                bat './gradlew test'  // Executes the Gradle test using the bat step (for Windows)
            }
        }
    }

