node {

    stage('Checkout')  
    {
        git credentialsId: 'ab141cd1-bb69-4f5c-a9a3-4e49b955aeff', url: 'https://github.com/edsherwin/webapp-shop.git'
    } 

    stage('Run Docker Compose File')
    {
        sh 'sudo docker-compose build'
        sh 'sudo docker-compose down'
        sh 'sudo docker-compose up -d'
    }
    
    stage('Push Docker Image to HUB')
    {
        sh 'sudo docker push edsherwin/deployapp_web'
    }
    
}
