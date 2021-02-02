node{
    stage('Git Clone'){
        git 'https://github.com/saurabhgore-code/sagorerepo.git'
    }
    stage('Maven Package'){
        def mvnHome = tool name: 'sagore-maven', type: 'maven'
        sh "${mvnHome}/bin/mvn package"
    }
    stage('Deployment'){ 
        sh 'cp target/*.war /opt/tomcat/webapps'
    }    
}
