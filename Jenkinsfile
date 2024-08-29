pipeline
{
    agent any
    stages
    {
       stage('Continuous Testing')
        {
            steps
            {
                sh 'java -jar /var/lib/jenkins/workspace/MultiBranch-Pipeline_master/testing.jar'
            }
        }
        stage('Continuous Delivery')
        {
            steps
            {
                deploy adapters: [tomcat7(credentialsId: '163a1995-8583-453d-8c5d-c57f0ae8bafe', path: '', url: 'http://192.168.199.133:8080')], contextPath: 'ProdApp', war: '**/*.war'
            }
        }
    }
}
