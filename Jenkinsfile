pipeline {
    agent any
    tools {
        gradle 'Gradle'
    }
    stages {
        stage('clone repository') {
            steps {
                git branch: 'master', url:'https://github.com/faisoabdirisak/java-todo.git'
            }
        }
        stage('Build the project') {
            steps {
                sh 'gradle build'
            }
        }
        stage('Tests') {
            steps {
                sh 'gradle test'
            }
        }
    }
}
