node() {
    stage("Checkout") {
        deleteDir()
        git "https://github.com/valikkr/Jenkins.git"
    }
    
    stage("Build") {
    sh "echo Building ${BUILD_ID} build"
    }
    stage("Testing"){
    sh "echo Testing on ${NODE_NAME}"
    sh "cat i.py"
    sh "python i.py"
    }
    stage("Delivery"){
    sh "echo Pulling on registry......"
    }
}
