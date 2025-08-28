week-03-cloud-automation/day15_aws_cli.md

# Day 15: AWS CLI Basics

```bash
aws s3 ls
aws ec2 describe-instances



### `week-03-cloud-automation/day16_s3_upload.py`
```python
# Day 16: Upload file to S3
import boto3

s3 = boto3.client("s3")
bucket = "my-genai-bucket"
s3.upload_file("week-01-linux-basics/day01_file_ops.sh", bucket, "day01.sh")
print("Uploaded to S3")


week-03-cloud-automation/day17_ec2_control.py

# Day 17: Start EC2
import boto3
ec2 = boto3.client("ec2")
ec2.start_instances(InstanceIds=["i-1234567890abcdef"])
print("EC2 started")


week-03-cloud-automation/day18_sagemaker_deploy.md

# Day 18: Deploying to SageMaker

Steps:
1. Prepare training script
2. Create SageMaker training job
3. Deploy as endpoint


week-03-cloud-automation/day19_fastapi_demo.py

# Day 19: FastAPI demo
from fastapi import FastAPI
app = FastAPI()

@app.get("/")
def read_root():
    return {"msg": "Hello Generative AI"}


week-03-cloud-automation/day20_lambda_gateway.md

# Day 20: Lambda + API Gateway

1. Write Lambda function in Python
2. Deploy to AWS Lambda
3. Connect with API Gateway
4. Test endpoint


week-03-cloud-automation/day21_pipeline_project.py

# Day 21: Simple ETL pipeline
import pandas as pd

data = {"text": ["Generative AI is powerful", "AWS supports ML workloads"]}
df = pd.DataFrame(data)
df.to_csv("etl_output.csv", index=False)
print("Pipeline complete")


