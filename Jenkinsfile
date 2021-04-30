pipeline{
   agent any

   parameters {
           string(name: 'Greeting', defaultValue: 'Hello', description: 'How should I greet the world?')
       }
          stages{
           stage('Example') {
               steps {
                   echo "${params.Greeting} World!"
               }
           }


               stage("build"){
                   steps{
                       echo"build successfull"
                   }
               }
               stage("test"){
                   steps{
                       echo"test successfull"
                   }
               }

               stage("deploy"){
                   steps{
                    echo"deploy sucessfull"
                    }
               }
        }  }
 
