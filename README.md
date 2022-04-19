Write to RDS table with Lambda in a VPC

1. push pymysql.zip file to your s3 bucket. You can create s3bucket through aws cli:

```
aws s3api create-bucket \
    --bucket my-bucket-test \
    --region eu-central-1 \
    --create-bucket-configuration LocationConstraint=eu-central-1
```

2. upload a file to the bucket:
```
aws s3 --region eu-central-1 cp pymysql.zip s3://my-bucket-test --acl public-read
```

3. change bucket name in template.yml before deploying with cloud formation
