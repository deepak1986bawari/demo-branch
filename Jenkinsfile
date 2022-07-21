pipeline {
agent { node { label 'master' } }
tools {
        maven 'maven-3.8.6' 
        jdk 'Jdk-9.0.4'
    }
stages {
         stage('Code validate') {
            steps {
                 sh 'mvn validate'
       }
}
        stage('Code Compile') {
            steps {
                sh 'mvn compile'
            }
    }
        stage('Code Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Code Package') {
            steps {
                sh 'mvn package'
            }
        }    
    }
}
