pipeline{
  agent any
  stages{
    stage("Checkout"){
      steps{
        git url:"https://github.com/igaryanthakur/Last-jenkins.git", branch:"master"
      }
    }
    stage("Build Image"){
      steps{
        bat "docker build -t web ."
      }
    }
    stage("Stopping old containers"){
      steps{
        bat "docker stop mycont || exit 0"
        bat "docker rm mycont || exit 0"
      }
    }
    stage("Run Image - Containarize"){
      steps{
        bat "docker run -d -p 7000:80 --name mycont web"
      }
    }
  }
}
