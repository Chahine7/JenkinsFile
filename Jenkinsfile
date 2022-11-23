pipeline {
agent any
tools{ jdk 'jdk11'}
environment { JAVA_HOME = 'C:\\Program Files\\Java\\jdk-13.0.2' }
stages {
stage ('Compile Stage') {
steps {
withMaven(maven : 'maven') {
bat 'mvn clean compile'
}
}
}
stage ('Testing Stage') {

steps {
withMaven(maven : 'maven') {
bat 'mvn test'
} }}
stage ('Install Stage') {
steps {
withMaven(maven : 'maven') {
bat 'mvn install'
} } } }
}
