pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Building..."'
                sh 'chmod +x scripts/Linux-Build.sh'
                sh 'scripts/Linux-Build.sh'
                archiveArtifact artifacts: 'bin/Debug/*', fingerprint: true
            }
        }
        stage('Run') {
            steps {
                sh 'echo "Running ..."'
                sh 'chmod +x scripts/Linux-Run.sh'
                sh 'scripts/Linux-Run.sh'
            }
        }
    }
}