pipeline{
  agent any
  environment {                 
    AWS_ACCESS_KEY_ID=${env.AWS_ACCESS_KEY_ID}
    AWS_SECRET_ACCESS_KEY=${env.AWS_SECRET_ACCESS_KEY}
    AWS_DEFAULT_REGION="eu-central-1"
  }
  stages{
    stage('Terraform init'){
      steps{
        sh 'terraform init'
      }
  }
  stage('Terraform init'){
    steps{
      sh 'terraform init'
    }
  }
 }
}
