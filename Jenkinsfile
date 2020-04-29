timestamps {
    node('windows') {
        stage('checkout'){
            git credentialsId: 'e5639047-d868-4a9b-b444-253dbb0f7752', url: 'https://github.com/Sakha8990/ibm-devops.git'
        }
        stage('Hello') {
            bat label: '', script: 'echo "[INFO] This is running on Windows"'
        }
    }
        
    node('master') {    
        stage('calling shell'){
                sh label: '', script: '''#!/bin/bash
                    echo "[INFO] Directly excuting it from Jenkins"
                    echo "[INFO] Directly excuting it from Jenkins" > jenkins.txt
                    echo ${param1} >> jenkins.txt
                    echo ${WORKSPACE} >> jenkins.txt
                    echo ${choice} >> jenkins.txt
                    echo ${GIT_BRANCH}'''            
        }
        
        stage('echo') {
                echo 'This is Second Stage!'
        }
    }
}

