pipeline{
  agent any
  stages{
       stage ('Sourcecode'){
          steps {
                   git 'https://github.com/kodalib4u/game-of-life-1.git'
                   }
       }
       stage ('build the code'){
         steps {
                   sh 'mvn clean package'
                   }
       }
       stage ('Archiving and Test Results'){
         steps {
                   junit '**/surefire-reports/*.xml'
                   archiveArtifacts artifacts: '**/*.war', followSymlinks: false
                   }   
       }
  }
}
