node {
  try {
    stage('checkout') {
      checkout scm
    }
    stage('prepare') {
      sh "git clean -fdx"
    }
    stage('compile') {
      sh "gcc hellome.c"
    }
    stage('test') {
      sh "./a.out"
    }
    stage('package') {
      sh "tar -cvzf hellome.tar.gz hellome.c"
    }
    stage('publish') {
      echo "uploading files for assgn..."
    }
  } finally {
    stage('cleanup') {
      echo "cleaning up..."
    }
  }
}
