pipeline{
  agent any
  environment{
    PYTHON_PATH =''C:\Users\LENOVO\AppData\Local\Programs\Python\Python311;C:\Users\LENOVO\AppData\Local\Programs\Python\Python311\Scripts'
      }
  stage{
  stage('checkout'){
    steps{
      checkout scm
    }
  }
    stage('build'){
      steps{
        bat '''
        set PATH=%PYTHON-PATH%;%PATH%
        pip install -r requirement.txt
        '''
      }
    }
    stage('Sonarqube-Analysis'){
      environment{
          SONAR-TOKEN=credentials('sonar-token')
        step{
          set PATH
        }
      }
    }
  }
 
}
