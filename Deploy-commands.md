There are only few deploy commands, but it's good to create seperate file so that there won't be any confusion later regarding the specific commands needed to be used for
the deployment of the serverless application.

The usual deploy command in the new version of serverless is <b>serverless deploy</b> OR <b>sls deploy</b>.

If you want to deploy any specific function only without deploying the rest of the application you can use <b>serverless deploy -f <function_name></b> OR <b>sls deploy -f <function_name></b>. After running this command
the desired output on the terminal should look like as below :-
  
✔ Function code deployed 
Configuration did not change. Configuration update skipped. 
