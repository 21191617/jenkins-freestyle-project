pipeline {
    agent any
    stages  {
        stage ('run script'){
            steps {"sh run.sh" }
    }
        stage ('generate artifacts'){
    steps {
        sh '''
        #!/bin/bash
        for1 in {1..5}: do echo "This is file\$i.text; done
        '''}
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '*.txt', followSymlinks: false
        }
    }
} 
    

























}