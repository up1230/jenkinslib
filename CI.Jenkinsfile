pipeline {
    agent any
    stages {
        stage('Stage Nmae: Get paras') {
            steps {
                script{
                    mavenHome = tool "M3"
                    sh "${mavenHome}/bin/mvn -v"
                }
            }
        }
    }
}
