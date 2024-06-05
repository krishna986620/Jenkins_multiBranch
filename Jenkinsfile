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
}
