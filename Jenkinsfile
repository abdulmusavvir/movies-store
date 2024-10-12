
// node(){
//     stage ('checkout'){
//         checkout scm
//     }
// }

// customizing the git clone command to specific credentials and branch

node(){
    stage('checkout'){
            git branch: 'develop'
            credentialsId: 'Jenkins-privatekey'
            url: 'https://github.com/abdulmusavvir/movies-store.git' 
    }
}
