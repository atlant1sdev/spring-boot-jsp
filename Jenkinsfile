pipeline{ 
agent any

  tools {maven "3.8.5"}

stages {
    stage('Git'){
    steps {
        git 'https://github.com/atlant1sdev/spring-boot-jsp/'
      }
    }
  stage('Testing') {
    steps {
      // One or more steps need to be included within the steps block.
      sh 'mvn test'
    }
  }
  stage('packaging') {
  steps {
    // One or more steps need to be included within the steps block.
    sh 'mvn package'
  }
}
stage('Copying package'){
    steps{
        cp -r /var/lib/jenkins/workspace/nodepipeline/dist/keyshell/* /var/www/html/

    }
}


}
}
