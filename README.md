# AWS-Cli Commands
<h1> 1. Create Key Pair </h1>
<b>aws ec2 create-key-pair --key-name sws</b>
<h1> 2. Create Security Groups </h1>
<b>aws ec2 create-security-group --group-name "sws123"  --description "cil12"    </b>
<h1> 2.1. Outgress/Outbound rules  </h1>
<b>aws ec2 authorize-security-group-egress --group-name "sws123" --ip-permissions IpProtocol=tcp,FromPort=0,ToPort=65535,IpRanges=[{CidrIp=0.0.0.0/0}]   </b>
<h1> 2.2. Ingress/Inbound Rules  </h1>
<b>aws ec2 authorize-security-group-ingress --group-name "sws123" --ip-permissions IpProtocol=tcp,FromPort=0,ToPort=65535,IpRanges=[{CidrIp=0.0.0.0/0}]  </b>
<h1> 3. Launch Instance </h1>
<b>aws ec2 run-instances --image-id ami-0e306788ff2473ccb --instance-type t2.micro --key-name sws --security-groups sws123 --count 1 <b>
<h1> 4. Create EBS Volume    </h1>
<b>aws ec2 create-volume --availbility-zone ap-south-1a --no-encrypted --size 1 </b>
<h1> 5. Attach EBS Volume to Instance</h1>
<b>aws ec2 attach-volume --instance-id {} --volume-id {} --device /dev/xvdf  </b>
<h1> 6. Cloud Front setup </h1>
<b>aws cloudfront create-distribution  --origin-domain-name {} --default-root-object {}</b><br>
