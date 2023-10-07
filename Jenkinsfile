pipeline{
    agent any 

    environment {
        SSH_CRED = credentials('SSH_CRED')
    }
    stages{
        stage('performing a dryrun'){
            steps{
                sh '''
                env
                ansible-playbook robo-dryrun.yml -e COMPONENT=mongodb -e ansible_user=${SSH_CRED_usr} -e ansible_password=${SSH_CRED_PSW}
                '''
            }        
        }
    }
}