node {
  stage 'Checkout'
  git 'ssh://git@github.com:ponnu777/demo-git.git'
 
  stage 'Docker build'
  docker.build('demo')
 
  stage 'Docker push'
  docker.withRegistry('https://122910936396.dkr.ecr.us-east-1.amazonaws.com', 'ecr:us-east-1:GitHUB-angel-ecr') {
    docker.image('demo').push('latest')
  }
}
