node('gol') {
   stage('SCM') {
    git 'https://github.com/spring-projects/spring-petclinic.git'
}
   stage('Build-maven'){
       sh label: '', script: 'mvn package'
   }
   stage('publish junit Results'){
       junit 'spring-petclinic/target/surefire-reports/*.xml'
   }
   stage('archive the artifact'){
       archive 'spring-petclinic/target/spring-petclinic-2.3.1.BUILD-SNAPSHOT.jar'
   }
}
