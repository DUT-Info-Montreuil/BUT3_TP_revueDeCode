node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'M3';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=BUT3_TP_revueDeCode -Dsonar.projectName='BUT3_TP_revueDeCode' -Dsonar.projectKey=sqp_febcc9c729f6fc259e01eacd5820943c3a5c9765"
    }
}
}
