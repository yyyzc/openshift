pipeline{
  agent any
  stages{
    stage("start build"){
      steps{
        openshiftBuild bldCfg: 'flask-app-jenkins', commitID: 'master', namespace: 'flask-app', showBuildLogs: 'true'
      }
    }
    stage("start deploy"){
      steps{
        openshiftDeloy depCfg: 'flask-app-jenkins', namespace: 'flask-app'
      }
    }
  }
}
