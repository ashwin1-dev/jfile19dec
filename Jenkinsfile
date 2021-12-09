pipeline {
    agent any
    
     stages {
         stage('install httpd server') {
             
             steps{
              sh ' sudo yum remove httpd -y'     
              sh ' sudo  rm  -rf  /var/www/html'
              sh 'sudo yum install httpd -y'
                  }
                                       }
         
         stage('start the service') {
             steps{
                 sh 'sudo  mkdir /var/www/html '
             sh 'sudo systemctl start httpd'
                  }
                                     }
         
         stage('deploying web page'){
             
             steps{
             sh 'sudo  git clone https://github.com/ashwin1-dev/9dec.git  /var/www/html  '
                    }
                                    }
     }
}
