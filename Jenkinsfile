pipeline {
     agent {
         label 'reactjs'
     }
     stages {
        stage("Build") {
            steps {
                sh "npm install"
                sh "CI=false npm run build"
            }
        }
        stage("Deploy") {
            steps {
                sh "rsync -rav --delete build/* administrator@172.16.0.235:/var/www/html/react-pipeline/maruhan-japanbank-21094031-reactjs"
                sh "echo maruhanjapanbank.mobiloitte.org"
                
            }
        }
    }
}
