Write to RDS table with Lambda in a VPC

1. push pymysql.zip file to your s3 bucket. You can create one through aws cli:
```
aws s3api create-bucket \
    --bucket my-bucket-raf-test \
    --region eu-central-1 \
    --create-bucket-configuration LocationConstraint=eu-central-1
```

2. change bucket name in template.yml before deploying with cloud formation
