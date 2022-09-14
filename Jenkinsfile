pipeline {
    agent any
     environment { //variables

        AWS_ACCESS_KEY_ID     = credentials('AWS_ACCESS_KEY_ID')
        AWS_SECRET_ACCESS_KEY = credentials('AWS_SECRET_ACCESS_KEY')

    }
    stages {
        stage('sumbit stack') {
            steps {
                sh " aws cloudformation create-stack --stack-name movies --template-body file://elasticBeanstalk.yml --region 'us-east-1'"
            }
        }
    }
}
