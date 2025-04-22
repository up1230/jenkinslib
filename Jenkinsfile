#!groovy

@Library('jenkinslib')

def tools = new org.devops.tools()

pipeline {
    agent any
    parameters { 
        string(name: 'DEPLOY_ENV', defaultValue: 'staging', description: '')
        booleanParam(name: 'DEBUG_BUILD', defaultValue: true, description: '')
    }
    stages {
        stage('Get paras') {
            steps {
                echo "Hello World!"
                input cancel: 'NO', message: 'Do you wanna keep printing?', ok: 'YES', parameters: [choice(choices: ['NO', 'YES'], description: '''NO for abort
YES for continue''', name: 'choice you decision')], submitter: 'admin'
                println("${demopara}")
                println("${DEPLOY_ENV}")
                println("${DEBUG_BUILD}")
                println(tools.printMes("this is github share lib!"))
            }
        }
    }
}
