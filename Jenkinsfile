node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv(sonar) {
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
