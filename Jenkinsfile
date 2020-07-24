def buildApp()  {
  echo 'building the application...'
}

def testApp() {
  echo 'testing the application...'
}

def deployApp() {
  echo "deploying the application...'
}

return this

pipeline {
  agent any 
  stages {
    stage("init") {
      steps {
        script {
          gv = load "script.groovy"
        }
      }
    }
    stage("build") {
      steps {
        script {
          gv.buildApp()
        }
      }
    }
    stage("test") {
      steps {
        script {
          gv.testApp()
        }
      }
    }
    stage("deploy") {
      steps {
        script {
          gv.deployApp()
        }
      }
    }
  }
}
