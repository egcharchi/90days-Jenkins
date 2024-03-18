pipeline{ /
    agent any
    tools{
        nodejs 'nodejs'
    }
    stages{
        stage('Clone Repository 1'){
            steps{
                git 'https://github.com/egcharchi/90days-Jenkins.git'
            }

        }
        //stage('Get latest commit') {
          //  steps {
            //    sh '''
                //   export COMMIT=$(git log --oneline | awk '{print $1}' | head -n 1)
                //   echo $COMMIT
                //   '''
           // }
        //}
        stage('Build'){
            steps{
                //Building - Installation of dependencies
                sh 'npm install'
                sh 'npm install body-parser'
                sh 'npm install ejs'
                sh 'npm install express'
                sh 'npm install mongodb'
                sh 'npm install mongoose'
                sh 'npm install multer'
                sh 'npm install uuid'
               
            }
        }
        stage('Test'){
            steps{
                //Testing
                sh 'npm test' 
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                //Deployment onto server
            }
        }
    }
}