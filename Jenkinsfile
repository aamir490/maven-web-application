//================================================== S C R I P T E D W AY ===========================================================
// 
////  SCRIPTED way pipeline :------------------------------------------------------------------------------------------------
//

/*
//   ( by defult master intance s)
node('master'){
}
*/

// =========================================== > S T A R T 

node{ // starting node

// Becz 'maven' not installed in jenkins server we are create variable:-
def mavenHome = tool name: "maven3.9.2"


//CHECKOUT STAGE - 1 
stage('checkoutcode'){
    git credentialsId: '1d83fec6-ba02-4af5-86f5-711354aaa0d2', url: 'https://github.com/aamir490/maven-web-application.git'
}

//BUILD STAGE - 2 
stage('Build'){
    sh "$mavenHome/bin/mvn clean package"
}
/*
//GENERATE SONARQUBE REPORT - 3 
stage('SonarQube Report'){
    sh "$mavenHome/bin/mvn sonar:sonar"
}

//UPLOAD ARTIFACT TO NEXUS - 4 
stage('Upload Artifact to Nexus'){
    sh "$mavenHome/bin/mvn deploy"
}

//DEPLOY APP INTO TOMCAT SERVER - 5 
stage('Deploy App to TomCat '){
    sshagent(['22a1799e-75e6-4c28-b250-9f2408d1abaf']) {
      sh "scp -o StrictHostKeyChecking=no target/maven-web-application.war ubuntu@43.205.217.173:/opt/apache-tomcat-9.0.76/webapps"
}
}
*/

}// closing node

// =========================================== > E N D
//====================================================================================================================================
