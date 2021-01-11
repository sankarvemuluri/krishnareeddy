node {
    state('scm'){
      git 'cloneurl'
    }
    stage('mvnepackage'){
      def mvnhome = too defined
      def mvncmd = "{mvnhome}/bin/mvn"
      sh "{mvncmd} clean package"
    stage('ddocker build')
      sh 'docker build -t sankarv/name .'
    stage('push docker image')
      sh "docker login -u username -p ${passwrod}"
      sh 'docker push sankar/name'
    stage('deploy in roductonn ')
      def dockerrun = 'docker run -it -p 8080:8080 jenkins/jenkns'
      sshagent ()
      sh "ssh -o StrictHostKeyChecking=no ec2-user@ipadddress ${dockerrun}"
}
    }
