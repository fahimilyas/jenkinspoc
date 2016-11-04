 node{
  
  stage ('Checkout from SCM')
  {
    echo 'Checkout code from version control'
  }
  stage ('Build Project')
  {
    echo 'Building the solution file'
  }

 
  
  parallel firstStep: {
   stage ('Run Unit Test')
   {
    node('linux-only'){
     echo "Hello World 1"
     sleep time: 2, unit: 'MINUTES'
    }
   }
  }, secondBranch: {
   stage ('Run Integration Test') 
   {
     echo "Hello World 2"
     sleep time: 1, unit: 'MINUTES'
   }
  }
  stage ('Zip Artifact')
  {
    echo 'Zipping artifacts'
  }
  stage ('Deploy to QA')
  {
    echo 'Deploying to QA'
  }
  stage ('Deploy to Staging')
  {
    echo 'Deploying to Staging'
  }
  stage ('Deploy to Production')
  {
    echo 'Deploying to Production'
  }
  
  
  
  
 }
