pipeline
{
    agent any

    tools{
        gradle "gradle-7.5"
        }

    stages
    {
        stage("Deploy to QA"){
            steps{
                echo("deploy to qa")
            }
        }
        stage('runSuiteXml') {
            steps {
                catchError(buildResult: 'SUCCESS', stageResult: 'FAILURE') {
                    git 'https://github.com/ankitagarwal03/gradleDemo'
                    sh "clean runSuiteXml"
                }
            }
        }
        stage("Deploy to Stage"){
            steps{
                echo("deploy to Stage")
            }
        }
    }
}