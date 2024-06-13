pipeline {
    agent any
    stages  {
        stage ('run script'){
            steps {sh "sh run.sh"}
    }
        stage ('generate artifacts'){
    steps {
        sh '''
        #!/bin/bash
        for i in {1..5}; do echo "This is file \$i" > file\$i.txt; done
        '''}
        }
    }
    post {
        always {
            archiveArtifacts artifacts: '*.txt', followSymlinks: false
        }
    }
} 
    

























