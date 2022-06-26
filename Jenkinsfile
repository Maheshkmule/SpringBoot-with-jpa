pipeline{
agent any
stages 
{
stage('Build') 
{
steps{
echo "Building the Code.........."
checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Maheshkmule/SpringBoot-with-jpa.git']]])
}
}
stage('Test') 
{
steps{
echo "Testing the Project.........."
bat "mvn test"
}
}
stage('Compile') 
{
steps{
echo "Compiling the Project.........."
bat "mvn compile"
}
}

stage('Deploy') 
{
steps{
echo "Deploying the Project.........."
}
}
}
}
