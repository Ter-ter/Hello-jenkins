pipeline {
    agent any

    //tools {
        // Install the Maven version configured as "M3" and add it to the path.
        //maven "M3"
    //}

    stages {
        stage('Git') {
            steps {
                // Get some code from a GitHub repository
                sh "pwd"
                sh "sshpass -v -p \"root\" ssh -v -o \"StrictHostKeyChecking=no\" root@172.20.10.3 'rm -rvf /mnt/www/html/test/'"
                sh "git clone https://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@github.com/Ter-ter/Hello-jenkins.git temp"
                sh "mv -n temp/* ."
                sh "rm -rf temp"

                // Run Maven on a Unix agent.
                
                
                //sh "sshpass -p \"root\" ssh -p 22 -o StrictHostKeyChecking=no root@192.168.1.170"

                // To run Maven on a Windows agent, use
                //dir('Jenkins') {
                //    bat "mvn -Dmaven.test.failure.ignore=true clean"
                //}
                
            }
