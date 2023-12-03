node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
/*  mode maven
    def mvn = tool 'M3';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=BUT3_TP_revueDeCode -Dsonar.projectName='BUT3_TP_revueDeCode'"
    }*/
    /* mode sonar directement
    def scannerHome = tool 'SonarScanner';
    withSonarQubeEnv() {
      sh "${scannerHome}/bin/sonar-scanner"
    }*/
    def mvn = tool 'M3';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=BUT3_TP_revueDeCode -Dsonar.projectName='BUT3_TP_revueDeCode' -Dsonar.token=sqp_d33c7c79e67576d831c73a4ee98b08a56371d595
  }
}
