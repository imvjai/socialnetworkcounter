node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Maven';
    withSonarQubeEnv() {
      #sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=vjai"
      sh "${mvnHome}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=vjai"
    }
  }
}
