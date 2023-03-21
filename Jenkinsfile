pipeline {
  agent any
  stages {
    stage('Stage1') {
      parallel {
        stage('Stage1') {
          steps {
            sh 'cut -d: -f1,3 /etc/passwd > /tmp/users'
          }
        }

        stage('stage1-2') {
          steps {
            sh 'cut -d: -f1,3 /etc/group > /tmp/groupes'
          }
        }

      }
    }

    stage('Stage2') {
      steps {
        sh 'cut -d: -f4 /etc/passwd | sort|uniq > /tmp/group_prim'
      }
    }

  }
}
