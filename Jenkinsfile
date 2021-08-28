pipeline{
    agent none
    stages{
        stage("Run ansible playbook"){
            agent none
            steps{
                script{
                    // sh 'echo $ECR_CREDS > keyfile.json'
                    sh 'ansible-playbook /path/to/ansible-playbook.yml -i /path/to/hosts_list -u AUTO_USER --private-key=/path/to/private-key'
                }
            }
        }
    }
    post{
        failure{
            script{
                mail (to: sekhar.sourav8@gmail.com,
                subject: 'Job failed',
                body: 'Ansible pipeline failed')
            }
        }
    }
}