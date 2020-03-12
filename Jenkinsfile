def workspace

node
{
    stage('Checkout')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/qa']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'PAC1', url: 'https://github.com/lalithprasad12/ownmerge.git']]])

    }

    stage('Static Code Analysis')
    {
        echo "Static Code Analysis"
    }

     stage('Build')
    {
        echo "Build the code"
        sh label: '', script: 'mvn clean install'
    }

     stage('Unit Testing')
    {
        echo "Unit Testing"
    }

     stage('Deploy')
    {
        echo "Deploy the code"
        cleanWs()
    }

}
