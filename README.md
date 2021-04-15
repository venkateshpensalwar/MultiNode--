# MultiNode-Kubernetes-Cluster

## Objective

Create ansible roles to setup multinode kubernetes cluster over AWS cloud.

## Steps to use roles to setup cluster over cloud

Install Following packages in controller node
- python2 or python3
- ansible

Using pip to install following packages
- boto or boto3


After that, you need user credentials for accessing AWS. As ```ec2.py``` make an API call to AWS for your requirement. so we need to set 2 environment variable in the following file

```
Create one file at  '~/'    with name ".boto"

// add following data in file 

[Credentials]
aws_access_key_id = <your_access_key_here>
aws_secret_access_key = <your_secret_key_here>

```

1. Download both ec2 file.

        Both File should be execuatable

            chmod +x file name (ec2.ini and ec2.py)


2. Add ```inventory``` as inventory directory in Ansible.cfg
3. Use ```EC2.yml``` file to provision instance using EC2 role.
4. Use ```kubernetes_cluster.yml``` to Configure kubernetes cluster over AWS cloud internally they useing respective roles.

## Note: if you wanted to see provisoned EC2 instance Run Following command 
````
./ec2.py
 ````
