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
          env.DOCKERFILES        = dockerfiles
          env.GITHUB_REPO        = github_repo.toLowerCase()
          env.DOCKER_TAG         = docker_tag.toLowerCase()
        }
      }
    }
    stage('Container build') {
        when {
            allOf {
            expression { dockerfiles }
            branch "master"
            }
        }
        steps {
            script {
                dockerBuild.login()
                dockerBuild.build(env.DOCKER_TAG)
                dockerBuild.push(env.DOCKER_TAG)
            }
        }
    }
