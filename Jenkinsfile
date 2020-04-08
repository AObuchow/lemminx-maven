pipeline{
  agent any
  tools {
    jdk 'adoptopenjdk-hotspot-jdk8-latest'
    maven 'apache-maven-3.6.2'
  }
  environment {
    MAVEN_HOME = "$WORKSPACE/.m2/"
    MAVEN_USER_HOME = "$MAVEN_HOME"
  }
  stages{
    stage("Maven Build"){
        steps {
          withMaven {
            sh 'mvn -B verify --file lemminx-maven/pom.xml'
          }
        }
    }
  }
}
