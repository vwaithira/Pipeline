node {

stage('Clone Repository')
{
checkout scm
}

stage('Show me the files'){
sh "ls -l"
}

stage('Build docker image'){

sh "docker build -t vivtest:latest ."
}

stage('Docker login to hub and push the image'){

sh "docker login -u 'vmungai' -p 'CIra123!' "
sh "docker tag vivtest:latest vmungai/pipe:latest"
sh "docker push vmungai/devrev:latest"
}

stage('Apply changes to the environment') {
sh "ls -l"
}


}
