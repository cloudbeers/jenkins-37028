node('master') {
    stage name:"Checkout", concurrency:1

    checkout scm
    sh """set -x
          if [ -d .git ] ; then
              echo "checkout done"
              exit 0
          else
              echo "checkout anywhere but not here"
              exit 1      
          fi
       """
}
