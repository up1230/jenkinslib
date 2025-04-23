#!groovy

@Library('jenkinslib') _

def tools = new org.devops.tools()
global()

pipeline {
    agent any
    parameters { 
        string(name: 'DEPLOY_ENV', defaultValue: 'devdef', description: '')
        booleanParam(name: 'DEBUG_BUILD', defaultValue: false, description: '')
    }
    stages {
        stage('Stage Name: Get paras') {
            steps {
                script{
                    tools.toolprint("Hello World from Github!", "red")
                }
                input cancel: 'Backup', message: 'Do you wanna keep printing?', ok: 'Continue', parameters: [choice(choices: ['NO', 'YES'], description: '''NO for abort
YES for continue''', name: 'choice you decision')], submitter: 'admin'
                
            }
        }
        stage('Stage Name: print mes'){
            steps{
                printMes("my var DEPLOY_ENV is : ${DEPLOY_ENV}", "green")
            }
        }
    }
}
