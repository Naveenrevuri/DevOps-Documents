# Step 1: Setup Linux VM (Amazon Linux AMI)

## Launch EC2 Instance

1. Login into AWS Console
2. Go to EC2 Service
3. Click Launch Instance
   - AMI: Amazon Linux
   - Instance Type: t2.medium
4. Create / Select Key Pair
5. Launch Instance

# Step-2 : Install Docker In Linux VM
```bash
sudo yum update -y 
sudo yum install docker -y
sudo service docker start
sudo usermod -aG docker ec2-user
exit
```
# Step-3 : Make SSH connection again and Verify docker installation
```bash
docker -v
```
# Step-4 : Run SonarQube using docker image
```bash
docker run -d --name sonarqube -p 9000:9000 -p 9092:9092 sonarqube:lts-community
```
# Step-5: Enable 9000 port number in Security Group Inbound Rules & Access Sonar Server
```bash
 - URL : http://public-ip:9000/
```
# step-6:Sonar-Dashboard
1)manual
2)plan-api
3)generate token
# step-7:Git Install 
```bash
sudo yum install git -y
```
Git-version
```bash
git --version
```
# step-8:Git Clone
```bash
git clone https://github.com/Naveenrevuri/plans-Api.git
cd plans-Api
```

# step-9:Maven Install
```bash
sudo yum install maven -y
```
Maven version
```bash
mvn -v
```
#step-10:Sonar Run With Token
```bash
mvn clean verify sonar:sonar \
-Dsonar.projectKey=Plans-Api \
-Dsonar.host.url=http://13.126.193.119:9000 \
-Dsonar.login=YOUR_TOKEN
```


