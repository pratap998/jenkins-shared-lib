@Library('jenkins-shared-lib@master')_
node
{
stage('Gitcheckout')
{
   sourcecheckout("https://github.com/pratap998/demo-app.js.git","master")
}
}
stage ('preparation') {
      steps {
        script {
          docker build -t app-demo .
             }
      }
    }
