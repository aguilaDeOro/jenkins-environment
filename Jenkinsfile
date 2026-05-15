pipeline {
  agent any
  environment {
    NAME = "jenkins"
    MACHINE = "Linux"
    CORAZON = "valiente"
  }
  stages {
    stage('Compiling') {   
      environment {
        AUTHOR='Apasoft'
      }    
      steps {
        echo "Compiling the code"
        sh 'javac Param.java'
        echo "The author is ${AUTHOR}"
        echo "Su corazon es ${CORAZON}"
      }
     }   
    stage('Execute'){
      steps{
        echo "Execute the program with a parameter "
        sh "java Param ${NAME}"
      }
    }
    stage('display the machine name'){
      steps{
        echo "And here I display the name of the machine "
        sh 'javac Machine.java'
        sh "java Machine ${MACHINE}"
      }
    }
  }
}
