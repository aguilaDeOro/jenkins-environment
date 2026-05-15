pipeline {
  agent any
  environment {
    NAME = "jenkins"
    CORAZON = "valiente"
    FUERZA = "infinita"
    MACHINE = """${
        sh (
                returnStdout: true, 
                script: 'uname -n'
        )
    }"""
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
        echo "Su fuerza es ${FUERZA}"
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
