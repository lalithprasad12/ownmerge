def workspace

node
{
    stage('Checkout')
    {
        echo "Checkout QA"

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
