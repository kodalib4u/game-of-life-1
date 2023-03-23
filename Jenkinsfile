node {
   stage ('Sourcecode'){
     git 'https://github.com/kodalib4u/game-of-life-1.git'
   }
   

  stage('Build the code'){
    sh 'mvn clean package'
  }

  stage('Archiving and Test Results') {
                junit '**/surefire-reports/*.xml'
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
        }

}
