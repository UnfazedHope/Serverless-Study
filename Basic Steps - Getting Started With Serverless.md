
# Steps to create our Serverless Environment

First, to use the code in our local desktop, you will need to download AWS CLI from this link - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html
<br>
After that you can check if the aws is properly installed or not using these two commands - <br>
1] aws <br>
2] aws --version <br>
<br>
After this step, you will need to create an IAM User such that we can get the access of our local system to the AWS Console.<br>
This can be done using following steps :-<br>
1] Create an IAM user through the AWS Console.<br>
2] After creating user, you will need to explicitly create AWS access key, which will give us two access keys one is public access key and one will be secret access key<br>
3] Next step is to run the aws configure command in your Command Line Prompt and put those access keys to configure your AWS Account.<br>
4] you may leave other fields as default(none) that won't affect your development process.<br>

After that, you will need to setup the serverless framework in your system. You can install this using the command "npm install -g serverless" 

Now you can create your serverless application(It will work as Infrastructure-as-a-Service) using following steps :-

1] put "serverless" command in cmd<br>
2] After that it will show variety of option which will mention the type of the project you need to create :-
<br>
  AWS - Node.js - Starter<br>
  AWS - Node.js - HTTP API<br>
  AWS - Node.js - Scheduled Task<br>
  AWS - Node.js - SQS Worker<br>
  AWS - Node.js - Express API<br>
  AWS - Node.js - Express API with DynamoDB<br>
  AWS - Python - Starter<br>
  AWS - Python - HTTP API<br>
  AWS - Python - Scheduled Task<br>
  AWS - Python - SQS Worker<br>
  AWS - Python - Flask API<br>
  AWS - Python - Flask API with DynamoDB<br>
  Other<br>
 3] Let's go ahead with AWS - Node.js - HTTP API<br>
 4] Now it will create our project folder<br>
 
 
# Default Code & Files of our Serverless Folder :- 

1] index.js 

Code -
```js
module.exports.handler = async (event) => {
  return {
    statusCode: 200,
    body: JSON.stringify(
      {
        message: "Go Serverless v3.0! Your function executed successfully!",
        input: event,
      },
      null,
      2
    ),
  };
};
```
2] .gitignore

Code-
```.gitignore
##package directories
node_modules
jspm_packages

##Serverless directories
.serverless
```
3] serverless.yaml (Important File)

Code-
```yaml
service: aws-node-http-api-project
frameworkVersion: '3'

provider:
  name: aws
  runtime: nodejs18.x

functions:
  api:
    handler: index.handler
    events:
      - httpApi:
          path: /
          method: get
```



