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