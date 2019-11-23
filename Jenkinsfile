node('maven') {
      stage('Poll') {
       git 'https://github.com/alv1981/sonarmaven.git'
     }
      stage("build & SonarQube analysis") {
                withSonarQubeEnv(credentialsId:'sonar_token',installationName:'sonarqube-server') {
                sh 'mvn clean verify sonar:sonar 
                //  sh 'mvn clean verify sonar:sonar org.sonarsource.scanner.maven:sonar-maven-plugin:3.6.0.1398:sonar -Dsonar.projectBaseDir=/home/jenkins/workspace/linux_academi/sonarmaven -Dsonar.sources=. -Dsonar.host.url=http://10.168.0.11:9000 -Dsonar.projectName=sonarmaven -Dsonar.projectVersion=1.0 -Dsonar.projectKey=sonarmaven'   
                }
                
       }
}
       
