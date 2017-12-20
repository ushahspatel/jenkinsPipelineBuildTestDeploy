node('master') {
  
   stage('Git Checkout'){
     checkout([$class: 'GitSCM', branches: [[name: '*/master']], browser: [$class: 'GithubWeb', repoUrl: 'https://github.com/ushahspatel/jenkinsPipelineBuildTestDeploy/blob/master/Jenkinsfile'], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[url: 'https://github.com/ushahspatel/jenkinsPipelineBuildTestDeploy.git']]])
   }

   stage('Maven Build'){
      echo 'Maven Project Compile'
      maven 'clean install'
      junit 'target/surefire-reports/**/*.xml'
   }
  
   stage 'Deploy'
        echo 'Deploying Docker Image'


   stage 'Testing'
        echo 'Reporting Getting Creating'

   stage 'Job Status Report'
        echo 'Sending Notification'
}
