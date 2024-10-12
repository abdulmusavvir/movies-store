
// node(){
//     stage ('checkout'){
//         checkout scm
//     }
// }

// customizing the git clone command to specific credentials and branch

node(){
    stage('checkout'){
            git branch: 'develop'
            credentialsId: '1d192c85-7a4a-4494-b009-d9ac77c3a8ec'
            url: 'https://github.com/abdulmusavvir/movies-store.git' 
    }
}
