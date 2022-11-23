pipeline {
agent any
tools{ jdk 'jdk13'}
environment { JAVA_HOME = 'C:\\Program Files\\Java\\jdk-13.0.2' }
stages {
stage ('Compile Stage') {
steps {
withMaven(maven : 'apache-maven-3.8.6') {
bat 'mvn clean compile'
}
}
}
stage ('Testing Stage') {

steps {
withMaven(maven : 'apache-maven-3.8.6') {
bat 'mvn test'
} }}
stage ('Install Stage') {
steps {
withMaven(maven : 'apache-maven-3.8.6') {
bat 'mvn install'
} } } }
