pipeline{

    agent {

        label 'master'

    }

    environment{

        //Docker Hub

        docker_hub_account = "josemartinho13"

        repo_name = "docker-image-upload"

        image_tag = "latest"

        docker_hub_login = credentials('josemartinho')

    }

    stages{

        stage("Build Image"){

            steps{

                script{

                    //Assemble Image Name

                    image_full_name = "${docker_hub_account}/${repo_name}:${image_tag}"

                    echo "Image name: ${image_full_name}"



                    //Build Image



                }

            }

        }

        stage("Publish Image"){

            steps{

                //docker login

                bat "docker login -u ${docker_hub_login_USR} -p ${docker_hub_login_PSW}"

                echo "Passou"

                //Publish image



            }

        }

    }

}