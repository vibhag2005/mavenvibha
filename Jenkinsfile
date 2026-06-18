pipeline{
 agent any
 tools{
 maven 'maventest'
 }
 stages{
  stage('Checkout'){
   steps{
    git branch:'master', url:'https://github.com/vibhag2005/mavenvibha.git'
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
  stage('Run Application'){
  steps{
  sh 'java -jar target/mavenvibha-1.0-SNAPSHOT.jar
  }
  }
  }
  post{
  success{
  echo 'build successfull'
  }
  failure{
  echo 'build failure'
  }
  }
  }
  
