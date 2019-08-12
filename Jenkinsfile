node {
    def app

    stage('Clone repository') {
        checkout scm
        echo "Cloning the Repository to our Workspace"
    }
    
    stage('Build') {
        sh 'cd hello-world'
        sh 'composer install'
        echo "Building Application"
    }
}
