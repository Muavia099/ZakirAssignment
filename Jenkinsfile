pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Muavia099/ZakirAssignment.git', branch: 'main'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying..'
                sshPublisher(
                    publishers: [
                        sshPublisherDesc(
                            configName: 'Zakir',
                            transfers: [sshTransfer(sourceFiles: '**/*', remoteDirectory: '/myapp')],
                
                        )
                    ]
                )
            }
        }
    }
}
