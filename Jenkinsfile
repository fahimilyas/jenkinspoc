 node{
  
  step{
   stage ('Checkout')
   {
      echo 'Checkout code from version control'
   }
  }
  
  parallel firstStep: {
   stage ('Build and Test 1')
   {
     echo "Hello World 1"
     sleep time: 2, unit: 'MINUTES'
   }
  }, secondBranch: {
   stage ('Build and Test 2') 
   {
     echo "Hello World 2"
     sleep time: 1, unit: 'MINUTES'
   }
  }
 }
