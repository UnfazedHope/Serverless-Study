First, to use the code in our local desktop, you will need to download AWS CLI from this link - https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html

After that you can check if the aws is properly installed or not using these two commands - <br>
1] aws
2] aws --version

After this step, you will need to create an IAM User such that we can get the access of our local system to the AWS Console.
This can be done using following steps :-
1] Create an IAM user through the AWS Console.
2] After creating user, you will need to explicitly create AWS access key, which will give us two access keys one is public access key and one will be secret access key
3] Next step is to run the aws configure command in your Command Line Prompt and put those access keys to configure your AWS Account.
4] you may leave other fields as default(none) that won't affect your development process.
