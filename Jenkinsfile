pipeline{

    agent any
    tools{
        maven 'Maven'
    }
    stages{
        stage('github'){
            steps{
                   git credentialsId: 'ramzz_file', url: 'https://github.com/ramram64357-hub/java.git'
            }
        }
        stage('build'){
            steps{
                sh'mvn -- version'
            }
        }
        stage('test'){
            steps{
                sh'mvn clean compile'
            }
        }
        stage('deploy'){
            steps{
                sh'mvn test'
            }
        }
        stage('run'){
            steps{
                sh'mvn package'
            }
        }
        stage('run hellworld'){
            steps{
                sh'mvn exec:java'
            }
        }
    }
    post{
        success{
            echo" java successfully run"
        }
        failure{
            echo" java failure"
        }
    }
}
