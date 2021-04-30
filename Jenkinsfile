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

           environment {
                  DISABLE_AUTH = 'true'
                  DB_ENGINE    = 'sqlite'
              }


          stages{

          stage('environment') {
                      steps {
                          echo "Database engine is ${DB_ENGINE}"
                          echo "DISABLE_AUTH is ${DISABLE_AUTH}"
                          bat 'set'
                      }
                  }





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




