# aws-eks-terraform-ansible
Create AWS EKS cluster using terraform and ansible. And Deploy an App.

#### Launch Amazon linux 2 and add this part in user-data:

```bash
#!/bin/bash
yum update
yum install git -y
amazon-linux-extras install ansible2 -y
ansible-galaxy collection install community.general
git clone https://github.com/yesidevelop/ansible-terraform-eks.git
cd ansible-terraform-eks && nohup ansible-playbook install_eks.yaml -vv &
```

Courtesy:
1. https://github.com/opszero/kubespot
2. https://github.com/ashutoshvct/aws-eks-terraform-ansible
3. https://github.com/testdrivenio/flask-vue-kubernetes


For adding new user to cluster:
https://aws.amazon.com/premiumsupport/knowledge-center/eks-kubernetes-object-access-error/
