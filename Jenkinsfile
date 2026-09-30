pipeline{

    agent any
    tools{
        maven 'Maven'
    }
    stages{
        stage('github'){
            steps{

            }
        }
        stage(build){
            steps{
                sh'mvn -- version'
            }
        }
        stage{
            steps{
                sh'mvn clean compile'
            }
        }
        stage ('deploy'){
            steps{
                sh'mvn test'
            }
        }
        stage (run){
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
