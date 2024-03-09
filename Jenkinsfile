def firstName = null
pipeline {
  agent none
  stages {
    stage('input') {
      steps {
        script {
          firstName = input (
            message: 'What is your first name?', 
            ok: 'Submit', 
            parameters: [string(defaultValue: 'Gopala', name: 'FIRST_NAME', trim: true)]
          )
        }
      }
    }
    stage('output') {
      agent any
      steps {
        script {
          echo "Good Morning, $firstName"
          sh "bash display.sh $firstName"
        }
      }
    }
  }
}
