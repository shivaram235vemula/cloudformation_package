# cloudformation_package

1.Here we are building a code pipeline that gets the template with local urls.
2.In the build stage packages using aws cli cloudformation command to create an output template.
3.Stores in s3 which has the local urls replaced with s3 paths .
4.Ultimately deploys them.

This is the sample command:

aws cloudformation package --template-file ${PathToProductTemplate} --region us-east-1 --output-template-file ${CFProductStackname}.yml --s3-bucket ${S3Bucket} --s3-prefix codepipeline --kms-key-id ${S3KMSKeyARN}
