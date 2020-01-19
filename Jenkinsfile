node {
   // Mark the code checkout 'stage'....
   stage 'Checkout'
   
   git url: 'https://github.com/bogo-devops/game-of-life.git'


   // Mark the code build 'stage'....
   stage 'Build'
      mvn clean package
   step([$class: 'JUnitResultArchiver', testResults: '**/target/surefire-reports/*.xml'])
}
