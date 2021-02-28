# terraform-aws-asg-elb
terraform-aws-asg-elb

#### Requirements
#### Please user terraform 0.14.7 or above

### please copy paste the below code
```
module "wordpress" {
    source = "aaronyildiztas/asg_elb/aws"
    aws_region       = "us-east-1"
    desired_capacity = 1
    max_size         = 1
    min_size         = 1
    key_name         = "wordpress_key"
    key_location     = "~/.ssh/id_rsa.pub"
    app_name = "hello_world"
    ssh_cidr_blocks  = [
        "127.0.0.1/32",
        "0.0.0.0/0"
  ]
}
```
### Please run
```
terraform init
terraform apply
```
