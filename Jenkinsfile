pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh '''#!/bin/bash
                echo 'In C or Java, we can compile our program in this step'
                echo 'In Python, we can build our package here or skip this step'
                '''
            }
        }
        stage('Test') {
            steps {
                sh '''#!/bin/bash
                echo 'Test Step: We run testing tool like pytest here'

                # TODO fill out the path to conda here
                # sudo /PATH/TO/CONDA init
                #sudo /opt/conda/bin/conda init

                # TODO Complete the command to run pytest
                # sudo /PATH/TO/CONDA run -n <Envinronment Name> <Command you want to run>
                #sudo /opt/conda/bin/conda run -n <Envinronment Name> pytest
                #sudo /opt/conda/bin/conda create -n my_env python=3.8 -y
                #sudo /opt/conda/bin/conda activate my_env



                #sudo /opt/conda/bin/conda install pytest numpy pandas scikit-learn -y

                python --version
                pip --version
                python -m pip install pytest numpy pandas scikit-learn
                pytest

                echo 'pytest not runned'
                #exit 1 #comment this line after implementing Jenkinsfile
                '''

            }
        }
        stage('Deploy') {
            steps {
                echo 'In this step, we deploy our porject'
                echo 'Depending on the context, we may publish the project artifact or upload pickle files'
            }
        }
    }
}
