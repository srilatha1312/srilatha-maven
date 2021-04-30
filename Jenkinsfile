pipeline{
   agent any

   parameters {
           string(name: 'Greeting', defaultValue: 'karna', description: 'How should I greet the world?')
            choice(
                   name: 'myParameter',
                   choices: "Option1\nOption2",
                   description: 'interesting stuff' )



                   choice(
                         name: 'Env',
                         choices: ['DEV', 'QA', 'UAT', 'PROD'],
                         description: 'Passing the Environment'
                       )

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


               stage('Environment') {
                     steps {
                       echo " The environment is ${params.Env}"
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




