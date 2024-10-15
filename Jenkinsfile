def ImageName = 'abdulmusavvirrohe/movies-store'

node(){
    stage('Code Checkout'){
        checkout scm
    }
    def imageTest = docker.build("${ImageName}-test","-f Dockerfile.test .")
    stage('Unit Test'){
        imageTest.inside(){
            sh 'npm run lint'
        }
    }
    stage('Integration Test'){
        sh 'docker run --rm ${ImageNmae}-test npm run test'
    }
}
