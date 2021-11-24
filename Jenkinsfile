pipeline {
    agent any
     parameters {
        choice(name: 'Option', choices: ['Bat', 'PowerShellScript', 'Exe'], description: 'Choose Which File you want to RUN')
     }
     stages {
          stage ('printing name') {
              steps {
                  script {
                    def Option = "${params.Option}"
                    if(Option == "Bat") {
                        
                       bat '''C:\\temp\\first_basic_batch'''   
                       return
                    } else if (Option == "PowerShellScript") {

                       powershell '''C:\\temp\\build.ps1'''
                       return
                    }
                    
                     else if (Option == "Exe") {

                       powershell '''C:\\temp\\Hello_world.exe'''
                       return
                    }
                  }
              }
              
          }
     }
}