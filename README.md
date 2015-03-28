# ec2-instance-info
A Bash script to get EC2 instance metadata while you're on the instance, as YAML.

This is similar to [the native query tool](https://aws.amazon.com/code/1825) (download it [here](http://s3.amazonaws.com/ec2metadata/ec2-metadata)), but ignores stuff you probably don't care about, outputs pure YAML, and is easier to read.

```shell
ubuntu@ip-172-31-6-155:~$ ./instance-info

# There are other metadata elements: do curl -s http://169.254.169.254/latest/meta-data/ to list them.
# You can also do curl -s http://s3.amazonaws.com/ec2metadata/ec2-metadata | bash to get the output of AWS's tool.

ami-id:                       ami-3a50120d
hostname:                     ip-172-31-6-155.us-west-2.compute.internal
instance-id:                  i-2d933013
instance-type:                m3.medium
local-hostname:               ip-172-31-6-155.us-west-2.compute.internal
local-ipv4:                   172.31.6.155
public-hostname:              ec2-54-148-181-211.us-west-2.compute.amazonaws.com
public-ipv4:                  54.148.181.211
public-keys/:                 0=cdoherty
security-groups:              cdoherty-demo
placement/availability-zone:  us-west-2c
services/:                    domain
```
