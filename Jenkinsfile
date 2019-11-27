pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                    '''
                withAWS(region:'us-east-2') {
                // do something
                s3Download(file:'file.txt', bucket:'jenkinsproject1', path:'path/to/source/file.txt', force:true)
                s3Download(file:'targetFolder/', bucket:'jenkinsproject1', path:'path/to/sourceFolder/', force:true)
                }               
            }
        }
    }
}
