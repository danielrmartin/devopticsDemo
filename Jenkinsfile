pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        writeFile file: "application.sh", text: "echo Built ${BUILD_ID} of ${JOB_NAME}"
        gateProducesArtifact file: 'application.sh', label: "application.sh:${BUILD_ID}"
      }
    }
  }
}
