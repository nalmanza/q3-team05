 node ('master'){
  stage 'Build and Validate'
  checkout scm
  //sh 'npm install'
  //sh 'npm test'
  sh 'echo $JOB_NAME'

  stage 'REST Service Tests'
  def teamId = env.JOB_NAME.split("-")[1].substring(4)
  def port = "31"+teamId
  echo "Running build for team " + teamId
  sh 'echo /usr/local/share/SoapUI-5.2.1/bin/testrunner.sh -PTEAM='+teamId+' -PPORT='+port+' ./Q3-Training-Tests-soapui-project.xml'
 }

//PORT=3990 npm start &
//sleep 5
///usr/local/share/SoapUI-5.2.1/bin/testrunner.sh -PTEAM=0 -PPORT=3990 ./Q3-Training-Tests-soapui-project.xml
//echo -n "Stopping Node..."
//npm stop
//echo "Stopped Node."
//sleep 10

