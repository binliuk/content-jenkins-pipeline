pipeline{
  agent any
  stages{
   stage('buid') {
     steps {
       sh 'javac -d . src/*.java'
       sh 'echo Main_class: Rectangulator > MANIFEST.MF'
       sh 'jar -cvmf MANIFEST.MF rectangle.jar *.class'
     }
  }
 }
}
