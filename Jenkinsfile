node() {
    stage("Checkout") {
        deleteDir()
        git "https://github.com/valikkr/Jenkins.git"
    }
    
    stage("Build") {
    sh "echo Building ${BUILD_ID} build"
    uses: actions/setup-python@v1
    with:
     python-version: '3.8'
     architecture: 'x64'
     - name: Install requirements
   # Устанавливаем зависимости
     run: pip install -r requirements.txt
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
