pipeline {
    agent any
    tools { 
        maven 'maven_3_5_0' 
        jdk 'java 8 oracle' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                ''' 
            }
        }

           
        stage ('Compile Stage') {

            steps {
              
                    sh 'mvn clean compile'
            }
        }

        stage ('Testing Stage') {

            steps {
               
                    sh 'mvn test'
                
            }
        }  
        
    }
}

 