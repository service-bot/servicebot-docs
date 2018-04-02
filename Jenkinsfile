pipeline {
  agent any
  stages {
    stage('Build Docs') {
      steps {
        sh 'mkdocs build '
      }
    }
    stage('Upload To S3') {
      steps {
        withAWS(credentials: 'aws', region: 'us-east-1') {
          s3Upload(bucket: 'docs.servicebot.io', acl: 'PublicRead', workingDir: 'site', includePathPattern: '**/*')
          cfInvalidate(distribution: 'EX1TSDTX65OVL', paths: '*')
        }
        
      }
    }
  }
}
