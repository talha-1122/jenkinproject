pipeline {
  
    agent {
        label 'Ansible-Node'
    }
    
    tools{
        maven "Maven-3.9.6"
    }

    stages {
        stage('Clone') {
            steps {
               git 'https://github.com/ashokitschool/maven-web-app.git'
            }
        }
        stage('Static Code Analysis'){
          steps {
            bat "mvn pmd:pmd"
            bat "mvn findbugs:findbugs"
          }
        }
        
        
    }
}
