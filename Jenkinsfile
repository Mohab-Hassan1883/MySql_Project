node {
  def remote = [:]
  remote.name = 'root'
  remote.host = 'machine IP'
  remote.user = 'root'
  remote.password = 'machine Passwd'
  remote.allowAnyHosts = true
  
  stage('clone Repo') {
  
    sshCommand remote: remote, command: 'git clone https://github.com/Mohab-Hassan1883/Mysql_project.git'
    }
    stage('SSH')
    {
    sshCommand remote: remote, command: 'docker-compose -f /root/Mysql_project/docker-compose.yml  down'
    sshCommand remote: remote, command: 'docker-compose -f /root/Mysql_project/docker-compose.yml  up -d'
    sshCommand remote: remote, command:'rm -rf Mysql_project'}
  }

