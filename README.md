## static website for test.

### デプロイ(バケット名をパラメータ指定してください)
```
aws cloudformation deploy \
  --template-file s3-static-website.yaml \
  --stack-name s3-static-site \
  --region ap-northeast-1 \
  --parameter-overrides BucketName=<your-unique-bucket-name-12345>

```

### URL確認
```
aws cloudformation describe-stacks \
  --stack-name s3-static-site \
  --region ap-northeast-1 \
  --query "Stacks[0].Outputs" \
  --output table
```

