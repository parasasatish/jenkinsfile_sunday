pipeline
{
 tools
  {
   git 'g'
   maven 'm2'
   jdk 'j'
  }
agent none
stages
{
 stage('validate')
{
 sh 'mvn validate'
}
satge('compile')
{
sh 'mvn compile'
}
stage('test')
{
sh 'mvn test'
}
stage('package')
{
sh 'mvn package'
}
}
}
