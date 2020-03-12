def workspace

node
{
    stage('Checkout')
    {
        checkout([$class: 'GitSCM', branches: [[name: '*/master']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: 'PAC1', url: 'git@github.com:lalithprasad12/maven.git']]])
        workspace=pwd()

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
