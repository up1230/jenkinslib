#!groovy

@Library('jenkinslib') _

pipeline {
    stages {
        stage('Stage Nmae: Get paras') {
            steps {
                script{
                    printMes("My local mvn version is:", "red")
                    mavenHome = tool "M3"
                    sh "${mavenHome}/bin/mvn -v"
                }
            }
        }
    }
}
