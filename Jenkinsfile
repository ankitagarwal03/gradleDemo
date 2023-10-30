pipeline
{
    agent any
    stages
    {

            stage('Gradle Build') {
                  steps {
                    sh './gradlew clean runSuiteXml'
                  }
            }
            stage("Deploy to QA 1"){
                steps{
                    echo("deploy to qa")
            }
        }

        stage("Deploy to Stage"){
            steps{
                echo("deploy to Stage")
            }
        }
    }
}