node {
   stage 'Checkout'
   checkout scm

   stage 'Build'
   sh "./autogen.sh && make clean && make"

   stage 'Test'
   sh "make test"

   stage 'Archive'
   zip zipFile: 'apertium.zip', archive: true, dir: 'apertium'
}
