pipeline{
  agent any
  stages{
    stage("Checkout"){
      steps{
        git "https://github.com/igaryanthakur/Last-jenkins.git"
      }
    }
    stage("Publish"){
      steps{
        publishHTML([
          allowMissing:true, 
          alwaysLinkToLastBuild:false,
          keepAll:false,
          reportDir:".",
          reportFiles:"index.html",
          reportName:"Last of Jenkins"
          ])
      }
    }
  }
}
