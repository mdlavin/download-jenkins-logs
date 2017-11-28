Jenkins Log Downloader
======================

Sometimes you want to analyze all of the logs in your Jenkins server with your
favorite Linux CLI text seraching tools. Here is a CLI for downloading Jenkins
logs for all builds in a server into a directory for easy analysis.

Running the downloader
----------------------

To run the downlaoder, just tell it how to access your Jenkins server and where
to put the logs:

     $ download-jenkins-logs -u $JENKINS_USERNAME -p $JENKINS_PASSWORD -U $JENKINS_URL -t jenkins-logs 

Alternatively, the Jenkins connection information can be pulled from environment
variables:

      $ export JENKINS_USERNAME=<your-username>
      $ export JENKINS_PASSWORD=<your-password>
      $ export JENKINS_URL=https://<your-jenkins-server>.com
      $ download-jenkins-logs

When the `-t` option is missing, it will default the `jenkins-logs` directory.

How to install
--------------

Assuming you have node installed, you can install this tool with:

    $ npm install -g download-jenkins-logs