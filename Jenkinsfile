def ImageName = 'abdulmusavvirrohe/movies-store'

node(){
    stage('Code Checkout'){
        checkout scm
    }
    def imageTest = docker.build("${ImageName}-test","-f Dockerfile.test .")
    stage('Unit Test'){
        imageTest.inside(){
            sh 'ls node_modules/'
            sh 'npm run lint'
        }
    }
    stage('Integration Test'){
        sh 'docker run --rm ${ImageName}-test npm run test'
    }
    stage ('Code Coverage'){
        sh 'docker run --rm ${ImageName}-test npm run coverage-text'
    }
}

