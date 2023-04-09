pipeline {
    agent any

tools{
maven 'maven_3.9.1'


}

    stages {
        stage('GitHub Sourcesss') {
            steps {
                echo 'Brining code from Git'
                    git branch: 'release/devl', credentialsId: '7690fd09-25d3-4d30-bfd3-27fa31e5560b', url: 'git@github.com:Gitnoobmaster/webapp.git'
            }
        }
        stage('Maven Build') {
            steps {
                echo 'Building code now'
                sh  "mvn clean package" } 
                }
        stage('Test - Sonar') {
            steps {
                echo 'Testing phase'
                sh "mvn sonar:sonar" }
            }
    }

}