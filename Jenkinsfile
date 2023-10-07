pipeline {
    agent any

    environment {
        SSH_CRED = credentials('SSH_CRED')
    }

    stages {
        stage('Lint Checks') {
            steps {
                sh '''
                echo ***** Starting lint checks *****
                # Add your lint checks here
                echo ***** Lint checks completed *****
                '''
            }
        }

        stage('Performing a Dryrun') {
            steps {
                sh '''
                
                '''
            }
        }

        stage('Main Branch') {
            when {
                branch 'main'
            }
            steps {
                sh '''
                echo The name of the branch job running against is ${BRANCH_NAME}
                '''
            }
        }
    }
}



//env ansible-playbook robo-dryrun.yml -e ENV=dev -e COMPONENT=mongodb -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW}