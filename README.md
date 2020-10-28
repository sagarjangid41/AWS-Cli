# AWS-Cli Commands
<h1> 1. create a key pair </h1>
<b>aws ec2 create-key-pair --key-name sws</b>
<h1> 2. create security groups </h1>
<b>aws ec2 create-security-group --group-name "sws123"  --description "cil12"    </b>
<h1> 2.1 outgress rules  </h1>
<b>aws ec2 authorize-security-group-egress --group-name "sws123" --ip-permissions IpProtocol=tcp,FromPort=0,ToPort=65535,IpRanges=[{CidrIp=0.0.0.0/0}]   </b>
<h1> 2.2 ingress rules </h1>
<b> aws ec2 authorize-security-group-ingress --group-name "sws123" --ip-permissions IpProtocol=tcp,FromPort=0,ToPort=65535,IpRanges=[{CidrIp=0.0.0.0/0}]  </b>
