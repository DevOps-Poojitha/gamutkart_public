pipeline  {
  agent any
  stages  {
    stage("stage1")  {
      steps  {
         script  {
            bat  "mvn clean install"
            }
          }
        }
    stage("parallel stage")  {
    parallel  {
      stage("stage2")  {
        steps  {
          echo "On stage 2"
          sleep 5
          }
        }
      stage("stage3")  {
        steps  {
          echo "On stage 3"
          sleep 10
            }
          }
       }
     }
   }
}
