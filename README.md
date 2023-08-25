steps:
1. label node for db volume >>> zone=eu-north-1a
2. create volume for db container with a tag >>> aws ec2 create-volume --availability-zone=eu-north-1a --size=3 --volume-type=gp2
3. create secret for db and rabbitmq password >>> echo -n "vprodbpass" | base 64 && echo -n "guest" | base 64