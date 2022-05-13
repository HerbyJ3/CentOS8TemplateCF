# CentOS8TemplateCF
Linux CentOS8 CloudFormationTemplate
Project Task:
For this project I was tasked to provision a Linux CentOS8 machine, update it, install nginx web server, enable nginx service, then start nginx service, and change the default page to the webserver.
I decided to challenge myself a bit more and chose to do this WITHOUT using the console.
I created a template for CloudFormation with Visual Studio Code  (YAML format)
Nothing crazy just a few static inputs, no parameters, and a few intrinsic functions
I entered a bash script file in the userdata portion of the template, which you will see.

POWERSHELL
I created an S3 bucket through powershell and copied the yml file to the s3 bucket (AWS CLI ONLY)
I ran the code via AWS CLI :(aws cloudformation create-stack --stack-name firstluitstack --template-url https://test239203920.s3.amazonaws.com/CentOS8.yml)
I was able to check the status by using the following:(aws cloudformation describe-stacks --stack-name firstluitstack) or (aws cloudformation describe-stack-events --stack-name firstluitstack)
FYI- You may notice I created another script file within the userdata. THIS IS NOT NECESSARY AS THE USERDATA IS PRETTY MUCH A BASHSCRIPT WITHIN ITSELF. I just did that for the sake of the project and to show that I understand how to create a script file within bash. If you want you can remove the script files and it will still work

By the way I have some of my favorite online games on the default page, have fun
