
pipeline
{
    agent any
    stages
    {
         stage('ContinuousDownload_Master')
        {
            steps
            {
                script
                {
                    try
                    {
                       git 'https://github.com/selenium-saikrishna/maven.git'
                    }
                    catch(Exception e1)
                    {
                        mail bcc: '', body: 'Jenkins was not able to download code from remote repo', cc: '', from: '', replyTo: '', subject: 'Download failed', to: 'gitadmin@gmail.com'
                        exit(1)
                    }
                }

            }
        }

        stage('ContinuousBuild_Master')
        {
            steps
            {
                script
                {
                    try
                    {
                        sh 'mvn package'
                    }
                    catch(Exception e2)
                    {
                        mail bcc: '', body: 'Jenkinsis unable to create an artifact from code', cc: '', from: '', replyTo: '', subject: 'Build failed', to: 'Devteam@gmail.com'
                        exit(1)
                    }
                }

            }
        }
}

