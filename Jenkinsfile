pipeline
{
    agent any
    stages
    {
        stage('Continuous Download')
        {
            steps
            {
                git 'https://github.com/kanamandarajesh/maven.git'

            }
        }
        stage('Continuous Build')
        {
            steps
            {
                sh 'mvn package'
            }
        }
        stage('Continuous Deploy')
        {
            steps
            {
                deploy adapters: [tomcat7(credentialsId: '163a1995-8583-453d-8c5d-c57f0ae8bafe', path: '', url: 'http://192.168.199.134:8080')], contextPath: 'TestApp', war: '**/*.war'
            }
        }
    }
}    
