# sage9-ciricleci-wpengine
Deploys a Sage 9 project from Github to WPEngine via CircleCI

Can use a free tier CircleCI account. 

Requires adding an environmental variable to your CircleCI job: 
1. Go to Jobs > [Job Name] > [Gear Icon] > Environmental Variables
2. Add key WPENGINE_DEPLOY_KEY
3. Add the private ssh key linked to an authorized WPEngine git identity
