node('docker') {
  // This displays colors using the 'xterm' ansi color map.
  ansiColor('xterm') {
    checkout scm

    def image = docker.build("codetroopers/website:${env.BUILD_ID}")
    image.withRun('npm run build')
//            {
//      sh 'npm run build'
//      sh 'npm run lint --silent'
//      sh 'npm run stylelint --silent'
//    }
  }
}