# Coffee-and-Cloud-CDK
Takeaway for our Coffee and Cloud CDK edition - **please note this representes general guidance steps and are by no means to be taken as production-ready deployment advice**

Steps for reproduction: <br>

1. Create a directory for your project and go to that directory <br>
    ```mkdir project ``` <br>
    ``` cd project ```
    
2. Install the CDK and create your app : <br>
        ``` npm install -g aws-cdk ``` <br>
        ``` cdk --version ``` (for checking the installation) <br>
        
3. Start codifying your infrastructure! <br>
    In this session, we have added a VPC: <br>
    ``` const fargateVpc = new ec2.Vpc(this, 'VPC'); ``` <br>
    and then built a Fargate service using an ecs-patterns construct referencing this VPC, following [this](https://docs.aws.amazon.com/cdk/api/v2/docs/aws-cdk-lib.aws_ecs_patterns.ApplicationLoadBalancedFargateService.html) guidance.
    
    
Useful resources:
Getting started with the CDK v2: https://docs.aws.amazon.com/cdk/v2/guide/getting_started.html <br>
Your first CDK app: https://docs.aws.amazon.com/cdk/v2/guide/hello_world.html <br>
ECS Patterns Fargate: https://docs.aws.amazon.com/cdk/api/v2/docs/aws-cdk-lib.aws_ecs_patterns.ApplicationLoadBalancedFargateService.html
