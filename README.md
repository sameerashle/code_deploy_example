Instructions
============
1.) Pass this info in userdata while setting up instance or do this post installation.

 yum update -y
 yum install awscli wget ruby -y
 cd /home/ec2-user/
 wget  https://aws-codedeploy-$(curl -s 169.254.169.254/latest/meta-data/placement/availability-zone | sed 's/.$//').s3.amazonaws.com/latest/install
 chmod +x ./install
 ./install auto", 
service codedeploy-agent restart
