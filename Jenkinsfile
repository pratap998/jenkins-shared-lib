@Library('jenkins-shared-lib')_

stages {
  stage('Clone')
    steps {
        script "git clone https://github.com/pratap998/demo-app.js.git"
    }
    stage('image')
    steps {
        script "docker build -t app.demo ."
    }
}
    
