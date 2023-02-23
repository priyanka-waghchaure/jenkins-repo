pipeline{
    agent any
    stages{
        stage("clone"){
            steps{
                sh "rm -rf /root/.m2/repository"
                sh "git clone https://github.com/priyanka-waghchaure/game-of-life.git"
            }
        }
        stage("build"){
            steps{
                sh "mvn -f /root/.jenkins/workspace/pipeline3/game-of-life/pom.xml install"
                }
        }
        stage("deploy"){
                steps{
                      sh "cp -r /root/.jenkins/workspace/pipeline3/game-of-life/gameoflife-web/target/gameoflife.war /data/server/apache-tomcat-9.0.71/webapps"
                }
            }
        
    }
}
