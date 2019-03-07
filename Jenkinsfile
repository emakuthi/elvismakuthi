node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files')
{
sh "ls -l"
}

stage('Build docker image')
{

sh "docker build -t elvismakuthi:version1 ."
}

stage('Docker login to hub and push the image')
{
sh "docker login -u 'emakuthi' -p 'Baraka2013' "
sh "docker tag elvismakuthi:version1 emakuthi/elvimakuthi:version1"
sh "docker push emakuthi/elvismakuthi:version1"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
