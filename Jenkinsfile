pipeline{
   agent any
   options {
       buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
}
   stages{
     stage('shell') {
        steps {
           sh 'java -version'
       }  
   }
     stage('maven build') {
        when {
          branch "local_release_branch"
        }
        steps {
           sh 'mvn install'
        }  
}
}
}
