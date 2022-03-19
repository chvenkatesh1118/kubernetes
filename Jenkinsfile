pipeline{
 agent any
  stages{
   stage{
     steps{
      sh 'docker pull nginx'
     }
   }
    stage{
        steps{
         sh 'docker run -itd -p 81:80 nginx'
        }
      }
  }
}