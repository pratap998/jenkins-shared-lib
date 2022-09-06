@Library('jenkins-shared-lib@master')_
node
{
stage('Gitcheckout')
{
   sourcecheckout("https://github.com/pratap998/demo-app.js.git","master")
}
}
stage('Docker image')
{
   dokckerfile("docker build -t app-demo .")
}
}
