# zipfile-transfer-ubuntu-aws
make a zip file and transfer that file to ubuntu machine in AWS

# create a folder in local ubuntu machine
mkdir local_share

# create a folder in remove ubuntu machine in aws
mkdir aws_share

# Mount foulders 
sudo sshfs ubuntu@<amazon account>:/home/ubuntu/aws_share local_share -o IdentityFile=/mnt/d/Murdoch/sydney_key.pem -o allow_other

# Transfer file
rsync --info=progress2 /mnt/e/www.zip local_share/


