pipeline{
  agent any
  stages
  {
    stage("git")
    {
      steps{git 'https://github.com/pradyumn12j/ant.git'}
    }

    stage("test")
    {
      steps{withAnt(installation: 'Home_ant', jdk: 'HOME_JAVA') {
    sh 'ant build'
}}
    }
    
  }
}