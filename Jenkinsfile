 pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ PES1UG20CS581.cpp'
        build job: 'PES1UG20CS581 PES1UG20CS581.cpp'
        echo 'Build the stage successfully '
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS581.out'
        echo 'Test Stage is Passed '
      }
    }
    stage('Deploy') {
      steps {
        echo 'Deployed  '
      }
    }
  }
  post{
    failure{
        echo "Pipeline failed "
    }
  }
}
