pipeline {
    agent any
    tools{

        maven "MAVEN3"
        jdk "OracleJDK8"
    }
    environment {
        SNAP_REPO = 'LBA-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin123'
        RELEASE_REPO = 'LBA-release'
        CENTRAL_REPO = 'LBA-maven-central'
        NEXUSIP = '172.31.20.153'
        NEXUSPORT= '8081'
        NEXUS_GRP_REPO = 'LBA-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build'){
            steps {
                sh 'mvn -s settings.xml -DskipsTests install'
            }
        }

    }
}