# jenkins-starter
how to install jenkins in our ec2 instance or windows or any os

# first we need install jdk


sudo apt update
sudo apt install fontconfig openjdk-17-jre
java -version
openjdk version "17.0.13" 2024-10-15
OpenJDK Runtime Environment (build 17.0.13+11-Debian-2)
OpenJDK 64-Bit Server VM (build 17.0.13+11-Debian-2, mixed mode, sharing)


# now we we install jenkins because jenkins use java 



sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
echo "deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc]" \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
sudo apt-get update
sudo apt-get install jenkins


# how to check that jenkins application is run on which port 
-- jenkins always run on port 8080


ps -f | grep jenkins


# how to get password of jenkins administrator password

sudo cat /var/lib/jenkins/secrets/initialAdminPassword
 --copy the initial password--

-- do install as normal steps which steps we use in daily purpose---


jenkins -----|--- jenkins worker 1
             |
             |
             |--- jenkins worker 2
             |
             |
             |--- jenkins worker 3



# always install docker in ec2 master node

sudo apt -get update
sudo apt install docker.io

# dockers run on a daemon process


sudo su -
usermod -aG docker jenkins
usermod -aG docker ubuntu
systemctl restart docker







             








