def ImageName = 'abdulmusavvirrohe/movies-store'

node(){
    stage('Code Checkout'){
        checkout scm
    }
    def imageTest = docker.build("${ImageName}-test","-f Dockerfile.test .")
    stage('Quality Test'){
        imageTest.inside{
            sh 'npm run lint'
        }
    }
}
