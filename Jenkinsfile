pipeline {
    agent any
    
    stages {
        stage('Retrieve Services') {
            steps {
                powershell '''
                # Define the PowerShell script to get services
                $services = Get-Service | Select-Object DisplayName, Status, ServiceType
                
                # Output the services
                Write-Output "Services:"
                $services
                '''
            }
        }
    }
}

