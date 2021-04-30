pipeline{
   agent any

   parameters {
           string(name: 'Greeting', defaultValue: 'karna', description: 'How should I greet the world?')
            choice(
                   name: 'myParameter',
                   choices: "Option1\Option2",
                   description: 'interesting stuff' )
             }
       }
          stages{
           stage('Example') {
           when { expression { return params.myParameter == "Option1"}}
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

        }


        post{
             always{
             echo"this is post"

             }
             }




        }




