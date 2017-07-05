pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        parallel(
          "Build": {
            bat 'http://srvfr01-0066.france.contentia.org:5555/invoke/com.sag.wx.dep.pub/buildProjectAutomatorAssets?environment=${BUILD_ENVIRONMENT}&password=manage&source=D%3A%5CCI%5Ccandidate%5C${BUILD_SOURCE}&targetPwd=${TARGETPWD}'
            
          },
          "Build2": {
            bat 'test'
            
          }
        )
      }
    }
  }
}