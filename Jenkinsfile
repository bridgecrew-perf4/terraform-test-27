pipeline{
  agent any
  environment {                 
    AWS_ACCESS_KEY_ID=credentials('AWS_ACCESS_KEY_ID')
    AWS_SECRET_ACCESS_KEY=credentials('AWS_SECRET_ACCESS_KEY')
  }
  stages{
    stage('Terraform init'){
      steps{
        sh 'terraform init'
      }
  }
  stage('Terraform apply'){
    steps{
      sh '''
      export AWS_ACCESS_KEY_ID=${env.AWS_ACCESS_KEY_ID}
      export AWS_SECRET_ACCESS_KEY=${env.AWS_SECRET_ACCESS_KEY}
      terraform apply --auto-approve
      '''
    }
  }
 }
}
