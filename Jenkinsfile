@Library('jenkins-shared-lib')_

stages {
  stage('Clone')
    steps {
        script "git clone "
    }
    stage('image')
    steps {
        script "docker build -t app.demo ."
    }
}
    
