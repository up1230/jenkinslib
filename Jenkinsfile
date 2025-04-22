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
        stage('Stage Nmae: Get paras') {
            steps {
                script{
                    tools.printMes("Hello World from Github!", "red")
                }
                input cancel: 'Backup', message: 'Do you wanna keep printing?', ok: 'Continue', parameters: [choice(choices: ['NO', 'YES'], description: '''NO for abort
YES for continue''', name: 'choice you decision')], submitter: 'admin'
                script{
                    tools.printMes("this is var DEBUG_BUILD: ${demopara}", 'blue')
                    tools.printMes("this is var DEBUG_BUILD: ${DEPLOY_ENV}", 'blue')
                    tools.printMes("this is var DEBUG_BUILD: ${DEBUG_BUILD}", 'blue')
                    tools.printMes("this is from github share library!", 'green')
                }
                
            }
        }
    }
}
