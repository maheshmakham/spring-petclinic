node('master'){
    stage('vcs'){
        git 'https://github.com/maheshmakham/spring-petclinic.git'
    }
    stage('build'){
        sh label: '', script: 'mvn package'
    }
    stage('post-build'){
        archive 'target/*.jar'
        junit 'target/surefire-reports/*.xml'
    }
}   