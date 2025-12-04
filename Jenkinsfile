pipeline {
  agent any
  stages { 
   stage('clone project 1') {
      steps {
           git branch:'master' , url:'https://github.com/monisha166/sBoot.git'
       }
   }
   stage('clean project test') {
      steps {
           sh 'mvn clean'
       }
   }
   stage('compile') {
      steps {
           sh 'mvn compile -DskipTests'
       }
   }
   stage('test') {
      steps {
           sh 'mvn test -DskipTests'
       }
   }
   stage('build') {
      steps {
           sh 'mvn clean install -DskipTests'
       }
   }
  }
}
