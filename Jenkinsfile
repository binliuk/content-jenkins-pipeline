pipeline{
  agent any
  stages{
   stage('buid') {
     steps {
       sh 'javac -d . src/*.java'
       sh 'echo Main-Class: Rectangulator > MANIFEST.MF'
       sh 'jar -cvmf MANIFEST.MF rectangle.jar *.class'
     }
  }
   stage('run'){
     steps{
      sh 'java -jar rectangle.jar $BUILD_NUMBER 9'
    }
   }
 }
}
