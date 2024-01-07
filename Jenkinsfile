pipeline {
    agent any  // Specifies that the pipeline can run on any available agent (node)

    stages {
        stage('Test') {  // Defines a stage named 'Test'
            steps {
                bat './gradlew test'  // Executes the Gradle test using the bat step (for Windows)
                 archiveArtifacts 'build/reports/tests/*'
                 bat './gradlew cucumber'
            }
        }
        stage('Code Analysis') {  // Defines a stage named 'Test'
                    steps {
                        bat './gradlew sonarqube'
                    }
                }
        stage('Build') {
                    steps {
                        generateJar()
                        generateDocumentation()
                        archiveArtifacts 'build/libs/*.jar'
                        archiveArtifacts 'build/docs/*'
                    }
                }
    }

