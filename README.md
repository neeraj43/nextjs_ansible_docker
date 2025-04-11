# nextjs_ansible_docker

## Step-by-Step: Run the Dockerfile
# Navigate to the project folder (where Dockerfile is)

cd nextjs_ansible_docker

# Build the Docker image

docker build -t nextjs-app .
This will use the Dockerfile to create an image named nextjs-app.

# Run the container

docker run -p 3000:3000 nextjs-app
This maps container port 3000 (where Next.js runs) to your local 3000.

# Run Ansible Script (password will be system passsword)

ansible-playbook -i hosts.ini deploy-nextjs.yml --ask-become-pass 

It will deploy your code on Docker Desktop .Have fun

# TakeAway

We can use Dockerfile to run this application irrespective of the enviroment.
It provides complete enviroment with needed resouces.


