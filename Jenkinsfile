pipeline{
  agent any
  tools{
    maven 'Maven'
  }
  stages{
    stage('Checkout'){
      steps{
        git branch:'master',
          url:'https://github.com/Ranjana2225/1BI23CS174_finaltest.git'
    }
    }
    stage('Build'){
      steps{
        sh 'mvn clean package'
      }
    }
    stage('Test'){
      steps{
        sh 'mvn test'
      }
    }
    stage('Run application'){
      steps{
        sh 'java -jar target/1BI23CS174_finaltest-1.0-SNAPSHOT.jar'
      }
    }
  }
  post{
    success{
      echo 'Build and deployment success'
    }
    failure{
      echo 'Build failed'
    }
  }
}
