pipeline {
  agent any
  stages{
    stage('Main CI stage') {
      steps {
        // stop running kestrel service
        sh ("sudo systemctl stop kestJen.service")
        // stop running nginx service
        sh ("sudo service nginx stop")
        // publish web app
        sh ("dotnet publish --configuration release")
        // restart kestrel service
        sh ("sudo systemctl start kestJen.service")
        // restart nginx service
        sh ("sudo service nginx start")
        // startup dotnet webapp
        sh ("cd /home/ubuntu/Documents/iggv")
        sh ("dotnet run & exit")
      }
    }
    // 
    // stage('') {
    //   when {
    //     anyOf {
    //       branch 'dev'
    //     }
    //   }
    //   steps {
        
    //   }
    // }
  }
  post {
    always {
      deleteDir()
    }
  }
}
