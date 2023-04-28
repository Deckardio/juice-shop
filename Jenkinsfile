pipeline {
  agent any
  stages {
    stage('scan') {
      steps {
        sh "docker run -v ${WORKSPACE}:/src --workdir /src returntocorp/semgrep semgrep --config p/ci --config p/security-audit --config p/secrets --output scan_results.json --json"
      }
    }
  }
}
