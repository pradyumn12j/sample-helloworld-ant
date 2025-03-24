pipeline{
  agent any
  stages
  {
    stage("git")
    {
      steps{git 'https://github.com/pradyumn12j/sample-helloworld-ant.git'}
    }

    stage('Verify Workspace') {
            steps {
                sh 'ls -l'  // List files in the workspace to verify if build.xml exists
            }
        }

    stage("build")
    {
      steps{withAnt(installation: 'Home_ant', jdk: 'HOME_JAVA') {
    sh 'ant -f build.xml -v'
}}
    }

    
  }
}