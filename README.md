# 🚀 Next.js Deployment with Docker & Ansible

This project demonstrates how to build and deploy a **Next.js application** using **Docker** and automate the process with **Ansible**.

---

## 📁 Project Structure

nextjs_ansible_docker/ ├── Dockerfile ├── deploy-nextjs.yml ├── hosts.ini ├── package.json ├── pages/ └── README.md


---

## ✅ Prerequisites

- [Docker Desktop](https://www.docker.com/products/docker-desktop/)
- [Ansible](https://docs.ansible.com/)
- Python modules: `requests`, `docker`
- Ansible Collections:
  ```bash
  ansible-galaxy collection install community.docker ansible.posix


## Step-by-Step: Running Your Next.js App with Docker
1. Navigate to your project folder

cd nextjs_ansible_docker

2. Build the Docker image

docker build -t nextjs-app .

This will use the Dockerfile to build an image named nextjs-app.

3. Run the Docker container

docker run -p 3000:3000 nextjs-app

This maps port 3000 from your container to your host machine.

Open your browser and visit: http://localhost:3000

## Automate with Ansible

Run the Ansible Playbook

ansible-playbook -i hosts.ini deploy-nextjs.yml --ask-become-pass
--ask-become-pass prompts for your system password (sudo)

Deploys and builds the Docker image using Ansible

Ensures consistent setup using Ansible automation

💡 Takeaway
Using Docker allows your app to run seamlessly across environments by packaging all dependencies. With Ansible, deployment becomes reproducible, automated, and scalable.

📌 Author
Made with ❤️ by Neeraj Wadhwani