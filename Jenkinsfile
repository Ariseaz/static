pipeline {
     agent any
     stages {
         stage('Upload to AWS') {
             steps {
                  withAWS(region:'us-east-1',credentials:'aws-static') {
                  sh 'echo "Uploading content to AWS S3 Bucket"'
                      s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, file:'index.html', bucket:'azudacitystatic')
                  }
             }
         }
     }
}
