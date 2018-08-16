sudo apt-get -y update
sudo apt install awscli -y
sudo aws s3 cp s3://aws-codedeploy-us-west-1/latest/install . --region us-west-1
sudo chmod +x ./install
sudo sed -i "s/sleep(.*)/sleep(10)" install
sudo apt-get install -y ruby
sudo ./install auto
sudo service codedeploy-agent start
sudo service codedeploy-agent status

