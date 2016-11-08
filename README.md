# salt-aws-provisioning

Install Salt client-server architecture first

Then install salt-cloud 

    wget -O - https://repo.saltstack.com/apt/ubuntu/14.04/amd64/latest/SALTSTACK-GPG-KEY.pub | sudo apt-key add -
    echo "deb http://repo.saltstack.com/apt/ubuntu/14.04/amd64/latest trusty main" > /etc/apt/sources.list.d/saltstack.list
    apt-get update
    apt-get install salt-cloud
    
    
Under /etc/salt/cloud.providers.d folder add 'ec2-us-west-2.conf' conf file

                            &

Under /etc/salt/cloud.profiles.d add 'ec2_us_west-2.conf' conf file

Then run 

        salt-cloud -p INSTANCE_TYPE INSTANCE_NAME

