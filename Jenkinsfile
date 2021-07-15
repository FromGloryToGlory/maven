
pipeline
{
    agent any
    stages
    {
         stage('ContinuousDownload_Loans')
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

    }

}


