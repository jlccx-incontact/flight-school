node("master"){
  stage('scm'){
    //checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'ee0a6a76-2943-4c98-af71-4553720a6e3b', url: 'git@github.com:jlccx-incontact/cicd-selfserviceportal.git']]])
    git poll: true, url: 'https://github.com/jlccx-incontact/flight-school.git'
    sh "printf 'The code downloaded is:\n | ls''"
  }
  stage("unit tests"){
    sh 'echo "running unit tests."'
    sh 'npm run unit-tests'
  }
  stage("deploy tests"){
    sh "printf 'running post-deploy tests'"
  }
}