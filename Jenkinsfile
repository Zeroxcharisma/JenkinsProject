pipeline {
    agent any
    tools { 
      maven 'MAVEN_HOME' 
      jdk 'JAVA_HOME' 
    }
    stages {
        stage('Git Clone') {
            steps {
                git 'https://gitlab.com/Zeroxcharisma/springprojectpiplinetest.git'
            }
        }
         stage('Maven Test') {
            steps {
                sh 'mvn test'
            }
        }
         stage('Maven build') {
            steps {
               sh 'mvn package'
            }
        }
        stage('Maven deploy') {
            steps {
               echo "deploying the war file to the server"
            }
        }
    }
}
