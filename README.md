# Configuration-management-with-Helm
**** Installing jenkins on EC2 Amazon Web Service ****
Create an EC2 instance
using xlarge instance, atleast 6 Cpu and 10gb memory
download the jenkins shell script and install on the script space when creating Ec2, name your jenjins script ie Jenkinserver
SSH into your terminal using the key pair
Use the LTS (Long time Support Release)
++++++++++++++++++++++++++++++++++++++++++++++++++++
sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
sudo yum upgrade
# Add required dependencies for the jenkins package
sudo yum install fontconfig java-17-openjdk
sudo yum install jenkins
sudo systemctl daemon-reload

In your terminal, do
chmod +x jenkinserver
Then run Ls to check your server
On the jenkinServer run jDK script for latest release
copy your host ip on google to access the ui of the jenkinserver
then type cat /usr/jvm/java-11-openjdk-amd64
tis will give a login password and username
create a repository on github 
configure your webhook from github, 

on your AWS,create a kubernete cluster, on you k8s cluster, create an helm chart
run helm create jenkinserver, this will create 

nginx-demo/
├── charts
├── Chart.yaml
├── templates
│   ├── deployment.yaml
│   ├── _helpers.tpl
│   ├── hpa.yaml
│   ├── ingress.yaml
│   ├── NOTES.txt
│   ├── serviceaccount.yaml
│   ├── service.yaml
│   └── tests
│       └── test-connection.yaml
└── values.yaml

3 directories, 10 files
 create a yaml files for NOTES.txt
  serviceaccount.yaml
   service.yaml
    tests
    test-connection.yaml
     values.yaml

verify the helm chart, run helm lint .

run  helm install my-release alex.li/tree    to check the helm tree

