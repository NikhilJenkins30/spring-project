node {
    checkout scm
    stage('Compile_and_Package') {
    bat 'mvn clean package'
                                }
 stage('Unit_Test') {
   bat 'mvn surefire:test'
   step([$class: 'Publisher'])
                    }
 stage('Compile_Analysis') {
    withSonarQubeEnv {
        bat 'mvn sonar:sonar'
                    }
                            }
}