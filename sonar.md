# Step 1: Setup Linux VM (Amazon Linux AMI)

## Launch EC2 Instance

1. Login into AWS Console
2. Go to EC2 Service
3. Click Launch Instance
   - AMI: Amazon Linux
   - Instance Type: t2.medium
4. Create / Select Key Pair
5. Launch Instance

## Connect to Server

```bash
ssh -i "your-key.pem" ec2-user@public-ip
