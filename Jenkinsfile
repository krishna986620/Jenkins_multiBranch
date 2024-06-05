node('master') 
 {
stage('continuous Download')
     {
    git 'https://github.com/krishna986620/testing.git'
}
stage('continuous Build')
{
sh 'mvn package'
}
stage('continuous Deploy')
{
deploy adapters: [tomcat9(credentialsId: '6d508a22-9e3b-4b21-87b4-7633a64e05b3', path: '', url: 'http://172.31.14.134:8080')], contextPath: 'qaenv', war: '**/*.war'
}
stage('continuous testing')
{
sh 'echo "Testing passed"'
}
stage('continuous Delivery')
{
deploy adapters: [tomcat9(credentialsId: 'dbe8e850-50ec-4a9f-8dd0-0f8f82833117', path: '', url: 'http://172.31.9.216:8080')], contextPath: 'prodenv', war: '**/*.war'
}
}
