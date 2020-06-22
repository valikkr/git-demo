node() {
    stage("Checkout") {
        deleteDir()
        git "https://github.com/valikkr/Jenkins.git"
    }
    
    stage("Build") {
    sh "echo Building ${BUILD_ID} build"
    sh "sudo su"
    sh "apt-get -y update"
    sh "apt-get -y install python3.6" 
    }
    stage("Testing"){
    sh "echo Testing on ${NODE_NAME}"
    sh "cat i.py"
    sh "python i.py"
    sh "cat b.py"
    sh "python --version"
    }
    stage("Delivery"){
    sh "echo Pulling on registry......"
    }
}
