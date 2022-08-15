pipeline {
    agent any
    stages {
        stage('unittest') {
            steps {
                 echo 'RUN UNIT TEST'
                 sh '''
                    python3 -m pytest test_calculator.py --junit-xml=report.xml 

                '''
             }
        }
}
post {
      always {
        junit 'report.xml'
      }
   } 
}
