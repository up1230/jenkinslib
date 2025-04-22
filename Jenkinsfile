#!groovy

@Library('jenkinslib')

def tools = new org.devops.tools() _
global()

pipeline {
    agent any
    parameters { 
        string(name: 'DEPLOY_ENV', defaultValue: 'devdef', description: '')
        booleanParam(name: 'DEBUG_BUILD', defaultValue: false, description: '')
    }
    stages {
        stage('Stage: Get paras') {
            steps {
                echo "Hello World from Github!"
                input cancel: 'Backup', message: 'Do you wanna keep printing?', ok: 'Continue', parameters: [choice(choices: ['NO', 'YES'], description: '''NO for abort
YES for continue''', name: 'choice you decision')], submitter: 'admin'
                println("${demopara}")
                println("${DEPLOY_ENV}")
                println("${DEBUG_BUILD}")
                println(tools.printMes("this is from github share library!"))
            }
        }
    }
}
