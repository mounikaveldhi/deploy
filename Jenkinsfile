node('A')
{
    stage('scm'){
        git credentialsId: 'jenkins', url: 'https://github.com/wakaleo/game-of-life.git'
    }
    stage('build'){
        sh label: '', script: 'mvn package'
    }
    stage('delpoy'){
        sh label: '', script: 'ansible-playbook /home/jenkins/tmct/goi.yml'
    }
}
