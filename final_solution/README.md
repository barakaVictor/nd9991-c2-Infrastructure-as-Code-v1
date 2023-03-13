### Project Title - Deploy a high-availability web app using CloudFormation
This folder provides the final solution for the "ND9991 - C2- Infrastructure as Code - Deploy a high-availability web app using CloudFormation" project. This folder contains the following files:


#### final-solution.yml
The Yaml file containing code to be exceuted by AWS CloudFormation to provision the desired resources.

#### parameters-file.json
The JSON file for increasing the generic nature of the YAML code. For example, the JSON file contains a "ParameterKey" as "EnvironmentName" and "ParameterValue" as "UdacityProject".

In YAML code, the `${EnvironmentName}` would be substituted with `UdacityProject` accordingly.

### Instructions before calling create.sh to do the actual deployment
If you have named profiles in the AWS config and credentials files located in your home directory .aws/ directory,
be sure to explicitly included the profile name associated with the AWS account being used for the project by explicitly setting the --profile option of the aws command as has been done in create.sh and update.sh. Otherwise, remove the explicit --profile configuration to use the default profile.

Once that is done, you can proceed and execute `./create.sh <stack-name> final-solution.yml parameters-file.json` without any issues.

To tear down the infrastructure, execute `./delete.sh <stack-name>`