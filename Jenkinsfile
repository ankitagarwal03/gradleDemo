pipeline
{
    agent any
    stages
    {
//         stage('Test') {
//             steps {
//                 bat "gradle clean test"
//             }
//         }

        stage("Deploy to QA 1"){
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