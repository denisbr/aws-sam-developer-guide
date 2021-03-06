# AWS Serverless Application Model Developer Guide

-----
*****Copyright &copy; 2020 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

-----
Amazon's trademarks and trade dress may not be used in 
     connection with any product or service that is not Amazon's, 
     in any manner that is likely to cause confusion among customers, 
     or in any manner that disparages or discredits Amazon. All other 
     trademarks not owned by Amazon are the property of their respective
     owners, who may or may not be affiliated with, connected to, or 
     sponsored by Amazon.

-----
## Contents
+ [What Is the AWS Serverless Application Model (AWS SAM)?](what-is-sam.md)
+ [Getting Started with AWS SAM](serverless-getting-started.md)
   + [Installing the AWS SAM CLI](serverless-sam-cli-install.md)
      + [Installing the AWS SAM CLI on Linux](serverless-sam-cli-install-linux.md)
      + [Installing the AWS SAM CLI on Windows](serverless-sam-cli-install-windows.md)
      + [Installing the AWS SAM CLI on macOS](serverless-sam-cli-install-mac.md)
   + [Setting Up AWS Credentials](serverless-getting-started-set-up-credentials.md)
   + [Tutorial: Deploying a Hello World Application](serverless-getting-started-hello-world.md)
+ [AWS Serverless Application Model (AWS SAM) Specification](sam-specification.md)
   + [AWS SAM Template Anatomy](sam-specification-template-anatomy.md)
      + [Globals Section of the Template](sam-specification-template-anatomy-globals.md)
   + [AWS SAM Resource and Property Reference](sam-specification-resources-and-properties.md)
      + [AWS::Serverless::Api](sam-resource-api.md)
         + [ApiAuth](sam-property-api-apiauth.md)
            + [ApiUsagePlan](sam-property-api-apiusageplan.md)
            + [CognitoAuthorizer](sam-property-api-cognitoauthorizer.md)
               + [CognitoAuthorizationIdentity](sam-property-api-cognitoauthorizationidentity.md)
            + [LambdaRequestAuthorizer](sam-property-api-lambdarequestauthorizer.md)
               + [LambdaRequestAuthorizationIdentity](sam-property-api-lambdarequestauthorizationidentity.md)
            + [LambdaTokenAuthorizer](sam-property-api-lambdatokenauthorizer.md)
               + [LambdaTokenAuthorizationIdentity](sam-property-api-lambdatokenauthorizationidentity.md)
            + [ResourcePolicyStatement](sam-property-api-resourcepolicystatement.md)
         + [ApiDefinition](sam-property-api-apidefinition.md)
         + [CorsConfiguration](sam-property-api-corsconfiguration.md)
         + [DomainConfiguration](sam-property-api-domainconfiguration.md)
            + [Route53Configuration](sam-property-api-route53configuration.md)
      + [AWS::Serverless::Application](sam-resource-application.md)
         + [ApplicationLocationObject](sam-property-application-applicationlocationobject.md)
      + [AWS::Serverless::Function](sam-resource-function.md)
         + [DeadLetterQueue](sam-property-function-deadletterqueue.md)
         + [DeploymentPreference](sam-property-function-deploymentpreference.md)
            + [Hooks](sam-property-function-hooks.md)
         + [EventInvokeConfiguration](sam-property-function-eventinvokeconfiguration.md)
            + [EventInvokeDestinationConfiguration](sam-property-function-eventinvokedestinationconfiguration.md)
               + [OnFailure](sam-property-function-onfailure.md)
               + [OnSuccess](sam-property-function-onsuccess.md)
         + [EventSource](sam-property-function-eventsource.md)
            + [AlexaSkill](sam-property-function-alexaskill.md)
            + [Api](sam-property-function-api.md)
               + [ApiFunctionAuth](sam-property-function-apifunctionauth.md)
                  + [ResourcePolicyStatement](sam-property-function-resourcepolicystatement.md)
               + [RequestModel](sam-property-function-requestmodel.md)
               + [RequestParameter](sam-property-function-requestparameter.md)
            + [CloudWatchEvent](sam-property-function-cloudwatchevent.md)
            + [CloudWatchLogs](sam-property-function-cloudwatchlogs.md)
            + [Cognito](sam-property-function-cognito.md)
            + [DynamoDB](sam-property-function-dynamodb.md)
            + [EventBridgeRule](sam-property-function-eventbridgerule.md)
            + [HttpApi](sam-property-function-httpapi.md)
               + [HttpApiFunctionAuth](sam-property-function-httpapifunctionauth.md)
            + [IoTRule](sam-property-function-iotrule.md)
            + [Kinesis](sam-property-function-kinesis.md)
            + [S3](sam-property-function-s3.md)
            + [Schedule](sam-property-function-schedule.md)
            + [SNS](sam-property-function-sns.md)
               + [SqsSubscriptionObject](sam-property-function-sqssubscriptionobject.md)
            + [SQS](sam-property-function-sqs.md)
         + [FunctionCode](sam-property-function-functioncode.md)
      + [AWS::Serverless::HttpApi](sam-resource-httpapi.md)
         + [HttpApiAuth](sam-property-httpapi-httpapiauth.md)
            + [OAuth2Authorizer](sam-property-httpapi-oauth2authorizer.md)
         + [HttpApiCorsConfiguration](sam-property-httpapi-httpapicorsconfiguration.md)
         + [HttpApiDefinition](sam-property-httpapi-httpapidefinition.md)
         + [HttpApiDomainConfiguration](sam-property-httpapi-httpapidomainconfiguration.md)
            + [Route53Configuration](sam-property-httpapi-route53configuration.md)
      + [AWS::Serverless::LayerVersion](sam-resource-layerversion.md)
         + [LayerContent](sam-property-layerversion-layercontent.md)
      + [AWS::Serverless::SimpleTable](sam-resource-simpletable.md)
         + [PrimaryKeyObject](sam-property-simpletable-primarykeyobject.md)
   + [Resource Attributes](sam-specification-resource-attributes.md)
   + [Intrinsic Functions](sam-specification-intrinsic-functions.md)
   + [Generated AWS CloudFormation Resources](sam-specification-generated-resources.md)
      + [AWS CloudFormation Resources Generated When AWS::Serverless::Api Is Specified](sam-specification-generated-resources-api.md)
      + [AWS CloudFormation Resources Generated When AWS::Serverless::Function Is Specified](sam-specification-generated-resources-function.md)
      + [AWS CloudFormation Resources Generated When AWS::Serverless::HttpApi Is Specified](sam-specification-generated-resources-httpapi.md)
   + [API Gateway Extensions](sam-specification-api-gateway-extensions.md)
+ [Authoring Serverless Applications](serverless-authoring.md)
   + [Validating AWS SAM Template Files](serverless-sam-cli-using-validate.md)
   + [Working with Layers](serverless-sam-cli-layers.md)
   + [Using Nested Applications](serverless-sam-template-nested-applications.md)
   + [Controlling Access to API Gateway APIs](serverless-controlling-access-to-apis.md)
+ [Building Serverless Applications](serverless-building.md)
   + [Building Applications](serverless-sam-cli-using-build.md)
   + [Building Layers](building-layers.md)
   + [Building Custom Runtimes](building-custom-runtimes.md)
+ [Testing and Debugging Serverless Applications](serverless-test-and-debug.md)
   + [Invoking Functions Locally](serverless-sam-cli-using-invoke.md)
   + [Running API Gateway Locally](serverless-sam-cli-using-start-api.md)
   + [Integrating with Automated Tests](serverless-sam-cli-using-automated-tests.md)
   + [Generating Sample Event Payloads](serverless-sam-cli-using-generate-event.md)
   + [Step-Through Debugging Lambda Functions Locally](serverless-sam-cli-using-debugging.md)
      + [Step-Through Debugging Node.js Functions Locally](serverless-sam-cli-using-debugging-nodejs.md)
      + [Step-Through Debugging Python Functions Locally](serverless-sam-cli-using-debugging-python.md)
      + [Step-Through Debugging Golang Functions Locally](serverless-sam-cli-using-debugging-golang.md)
   + [Passing Additional Runtime Debug Arguments](serverless-sam-cli-using-debugging-additional-arguments.md)
+ [Deploying Serverless Applications](serverless-deploying.md)
   + [Deploying Serverless Applications Gradually](automating-updates-to-serverless-apps.md)
+ [Monitoring Serverless Applications](serverless-monitoring.md)
   + [Working with Logs](serverless-sam-cli-logging.md)
+ [Publishing Serverless Applications Using the AWS SAM CLI](serverless-sam-template-publishing-applications.md)
   + [AWS SAM Template Metadata Section Properties](serverless-sam-template-publishing-applications-metadata-properties.md)
+ [Example Serverless Applications](serverless-example-applications.md)
   + [Process DynamoDB Events](serverless-example-ddb.md)
   + [Process Amazon S3 Events](serverless-example-s3.md)
+ [AWS SAM Reference](serverless-sam-reference.md)
   + [AWS SAM CLI Command Reference](serverless-sam-cli-command-reference.md)
      + [sam build](sam-cli-command-reference-sam-build.md)
      + [sam deploy](sam-cli-command-reference-sam-deploy.md)
      + [sam init](sam-cli-command-reference-sam-init.md)
      + [sam local generate-event](sam-cli-command-reference-sam-local-generate-event.md)
      + [sam local invoke](sam-cli-command-reference-sam-local-invoke.md)
      + [sam local start-api](sam-cli-command-reference-sam-local-start-api.md)
      + [sam local start-lambda](sam-cli-command-reference-sam-local-start-lambda.md)
      + [sam logs](sam-cli-command-reference-sam-logs.md)
      + [sam package](sam-cli-command-reference-sam-package.md)
      + [sam publish](sam-cli-command-reference-sam-publish.md)
      + [sam validate](sam-cli-command-reference-sam-validate.md)
   + [AWS SAM CLI Config](serverless-sam-cli-config.md)
   + [AWS SAM Policy Templates](serverless-policy-templates.md)
      + [Policy Template List](serverless-policy-template-list.md)
   + [Telemetry in the AWS SAM CLI](serverless-sam-telemetry.md)
+ [Document History for AWS Serverless Application Model](doc-history.md)