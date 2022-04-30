node {
    stage('checkout') {
        git branch: 'dev',
       credentialsId: 'github-sree',
       url: 'https://github.com/github-sree/k8s-learning-frontend.git'
    }
    stage('ng dist build') {
        sh 'npm install --save'
        sh 'ng build'
    }

    stage('docker build & push') {
        sh 'docker build -t sreedocker0798/k8s-learning-frontend:1.0.0 .'
        sh 'docker push sreedocker0798/k8s-learning-frontend:1.0.0'
    }


}
