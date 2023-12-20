pipeline { 

  agent any
  stages {
    stage('Test') {
           steps {
                                bat './gradlew test'
                 }
            }

    stage('Generate Cucumber Reports') {
                steps {
                bat './gradlew cucumber'
                }
            }
        }

    }
}

}