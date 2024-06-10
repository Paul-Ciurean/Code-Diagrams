# This is the place where you will find the code for eraser.io

## P1:


```

Engineer [icon: user]
Terminal [icon: powershell]
Browser [icon: browser]
Users [icon: users]

AWS [icon: aws] {
  VPC [icon: aws-VPC]{
    EC2 [icon: aws-EC2] {
      Apache [icon: Apache]
      MySQL [icon: MySQL]
      PHP [icon: PHP]
    }
  }
}

Engineer > Terminal
Terminal > EC2 : SSH to

Browser < EC2
Users > Browser
EC2 

```

## P2:

```

Engineer [icon: user]
Terminal [icon: powershell]

AWS [icon: aws] {
  VM [icon: aws-EC2] {
    Run [icon: file]
    Script [icon: list]
    List [icon: typescript] {
      IAM [icon: aws-iam]
      S3 [icon: aws-S3]
      Lambda [icon: aws-Lambda]
      EC2 [icon: aws-EC2]
    }
  }
}

Engineer > Terminal 
Terminal > VM : SHH
Script > List
Run > Script

```

## P3: 

```

Engineer [icon: user]
powershell [icon: powershell]
aws {
  VPC Subnet [icon: aws-vpc] {
    Server 1 [icon: aws-ec2] {
      Ansible [icon: ansible]
      Playbook [icon: file-code]
    }
    Server 2 [icon: aws-ec2] {
      Nginx [icon: nginx]
    }
  }
}

Engineer > powershell
powershell > VPC Subnet : SHH
Ansible > Playbook : Execute
Playbook > Server 2 : Install


```

## P4: 

```

// Define infrastructure
Engineer [icon: user]
GitHub [icon: github]
Customers [icon: users]
Internet [icon: browser]
aws {
  eu-east-1 [icon: aws-vpc] {
    CodePipeline [icon: aws-codepipeline]
    S3 [icon: aws-s3]
    Lambda [icon: aws-lambda]
    R53 [icon: aws-route-53]
  }
  CloudFront [icon: aws-cloudfront]
  Certificate Manager [icon: aws-certificate-manager]
}
// Define connections
Engineer > GitHub : Pushes Code
GitHub > CodePipeline : Trigger Pipeline
CodePipeline > S3 : Upload file in S3
S3 > Lambda : Trigger Lambda
CloudFront <> S3 
Certificate Manager <> CloudFront : SLL Certificate
Lambda > CloudFront : Create Invalidation
R53 > CloudFront : Route Traffic
Customers > Internet
Internet > R53


```

## P5: 


```

Root-User [icon: user]
User1 [icon: user]
User4 [icon: user]
User5 [icon: user]


devops [icon: square] {
  User2 [icon: user]
  User3 [icon: user]
}

aws [icon: square] {
  User1 [icon: user]
}

app [icon: square] {}
database [icon: square] {}

Root-User > aws, devops, app, database, User4, User5

```

```

home [icon: folder]
dir1 [icon: folder] {
  f1.1 [icon: file]
}
dir2 [icon: folder] {
  dir1.1 [icon: folder] {
    dir2.2 [icon: folder] {
      dir10 [icon: folder]
      f3 [icon: file]
    }
  }
}
dir3 [icon: folder] {
  dir11 [icon: folder]
}
dir4 [icon: folder] {
  dir12 [icon: folder] {
    f4 [icon: file]
    f5 [icon: file]
  }
}
dir5 [icon: folder] {
  dir13 [icon: folder]
}
dir6 [icon: folder]
dir7 [icon: folder] {
  dir10.1 [icon: folder]
  f3.1 [icon: file]
}
dir8 [icon: folder] {
  dir9 [icon: folder]
}
f1 [icon: file]
f2 [icon: file]
opt [icon: folder] {
  dir14 [icon: folder] {
    dir10.2 [icon: folder]
    f3.2 [icon: file]
  }
}

home > dir1 > dir2 > dir3 > dir4 > dir5 > dir6 > dir7 > dir8 > f1 > f2 > opt

```


## P6: 


```


Engineer [icon: user]
Terraform [icon: terraform]
Customer [icon: user]
Browser [icon: internet-explorer]


AWS [icon: aws] {
  WafACL [icon: aws-waf]
  IGW [icon: aws-internet-gateway]
  CloudFront [icon: aws-cloudfront]
  Region [icon: aws-region] {
  StateFile [icon: aws-s3]
    VPC [icon: aws-vpc] {
      


      Pub-SG [icon: aws-security-group]
      Prv-SG [icon: aws-security-group]

      Internet-Facing [icon: aws-application-load-balancer]    
      Internal [icon: aws-application-load-balancer]

      WebASG [icon: aws-ec2-auto-scaling]
      AppASG [icon: aws-ec2-auto-scaling]

      RTPub [icon: aws-route-table]
      RTPrv [icon: aws-route-table]

      AZ1 [icon: aws-availability-zone] {
        NATGW1 [icon: aws-nat-gateway]
        Pub-Sub1 [icon: aws-public-subnet] {
          EC2-1 [icon: aws-ec2]
        }
        Prv-Sub1 [icon: aws-private-subnet] {
          EC2-2 [icon: aws-ec2]
        }
        Prv-Sub2 [icon: aws-private-subnet] {
          DB-Primary [icon: aws-rds]
        }
      }
      AZ2 [icon: aws-availability-zone] {
        NATGW2 [icon: aws-nat-gateway]
        Pub-Sub2 [icon: aws-public-subnet] {
          EC2-3 [icon: aws-ec2]
        }
        Prv-Sub3 [icon: aws-private-subnet] {
          EC2-4 [icon: aws-ec2]
        }
        Prv-Sub4 [icon: aws-private-subnet] {
          DB-RO [icon: aws-rds]
        }
      }
    }
  }
}


Engineer > Terraform > AWS
Customer <> Browser <> WafACL <> CloudFront <> IGW <> Internet-Facing <> WebASG <> Internal <> AppASG

WebASG > EC2-1, EC2-3
AppASG > EC2-2, EC2-4

RTPub > Pub-Sub1, Pub-Sub2
RTPrv > Prv-Sub1, Prv-Sub2, Prv-Sub3, Prv-Sub4

DB-Primary > DB-RO

Pub-SG > EC2-1, EC2-3
Prv-SG > EC2-2, EC2-4, DB-Primary, DB-RO

Pub-Sub1 > NATGW1 > Prv-Sub1 <> Prv-Sub2
Pub-Sub2 > NATGW2 > Prv-Sub3 <> Prv-Sub4



```



## P7: 

```

Part 1:


Engineer [icon: user]
CLI [icon: aws-command-line-interface]
Docker-image [icon: docker]
LocalHost [icon: internet-explorer]



Engineer > CLI: Connect
CLI > Docker-image: Run
Docker-image > LocalHost: Deploy website
Engineer <> LocalHost: Connect


Part 2:


Engineer [icon: user]
CLI [icon: aws-command-line-interface]
Docker-image [icon: docker]
User [icon: user]
Internet [icon: internet-explorer]


AWS [icon: aws] {
  ECR [icon: aws-elastic-container-registry]
  ECS [icon: aws-elastic-container-service]
  ALB [icon: aws-application-load-balancer]
  Domain-Name [icon: aws-route53]
}



Engineer > CLI: Connect
CLI > AWS, Docker-image :Create
Docker-image > ECR: Push
ECR > ECS: Create
ECS > ALB: Create Service
ALB > Domain-Name: Attach
User <> Internet: Connect 
Internet <> Domain-Name

```