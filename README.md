# sage9-ciricleci-wpengine
Deploys a Sage 9 project from Github to WPEngine via CircleCI

Can use a free tier CircleCI account. 

Requires adding an environmental variable to your CircleCI job: 
1. Go to Jobs > [Job Name] > [Gear Icon] > Environmental Variables
2. Add key WPENGINE_DEPLOY_KEY
3. Add the private ssh key linked to an authorized WPEngine git identity

Essentially this runs a git checkout on your Github project, a git checkout on your WPEngine install, rsyncs code from the first to the second, and pushes back up to WPEngine. 

It uses a free tier CircleCI account which means containers are not persistant, they are created on a push and destroyed after a short time. The entire build process to spin up a containter, run checkouts, copy files, and push takes about five minutes. 
