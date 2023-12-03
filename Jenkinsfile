node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'M3';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=BUT3_TP_revueDeCode -Dsonar.projectName='BUT3_TP_revueDeCode'"
    }
}
}
