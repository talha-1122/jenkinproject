pipeline {
  
    agent {
        label 'Talha-Node'
    }
    
    tools{
        maven "Maven-3.9.6"
    }

    stages {
        stage('Cloning') {
            steps {
               git 'https://github.com/ashokitschool/maven-web-app.git'
            }
        }
        stage('Analysis of static code'){
          steps {
            bat "mvn pmd:pmd"
            bat "mvn findbugs:findbugs"
          }
        }
        
        
    }
}
