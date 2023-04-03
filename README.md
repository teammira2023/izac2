# Capstone Project (Cloud DevOps TeamMiRA - Modern Infrastructure Robotic Automation)

Capstone project for  CMU - TalentSprint Dev-Ops for Executives : Automate the infrastructure with  CI/CD pipeline 
for the Pythn Based  applications for improved Deployment and Infra changes.

## InfraStructure as a Code using Terraform - Provisioning Infrastrucre : MIRA # izac is the MIRA's infra Robot.

The CI CD pipeline is as follows for this project. For initial set up:

- Set up jenkins ( Jenkins is installed Zeepipe Host).
- Install dependencies for local development
- Create AWS infrastructure
- Instal Terraform , Promoted, GitHUb, Blue Ocean Plugin in the Jenkins.

## Configuration Management using Ansible : MIRA

The CI CD pipeline is as follows for this project. For initial set up:

- Set up jenkins
- Install dependencies for local development
- Create AWS infrastructure

For application development: We will use the python Application easy-school provided to our team.

- Make development change ( COming soon to comin soon - Demo)
- Commit to git
- Update  commands listed below if required
- Push to repository
- Jenkins build automatically runs based on triggers ( The pipeline is called easy-school pipeline)
- Docker image build and docker compose up are in the runtime.sh of the pipeline.
 
  
## CI CD Pipeline using Jenkins : MIRA

The CI CD pipeline is as follows for this project. For initial set up:

- Set up jenkins - Setup users , Approver/Reviewer 
- Add  the IAC Agent in Jenkins. Create the JAgent.sh to run the agent in the Harbor Host.
- At the End of the pipeline execution the IZAC2 pipeline delivers based on the commited code change.
- It has capability to make a smal change like in Network Infrastructre ( MIRA VPC and its associated componets) in AWS Cloude infrastructure or 
   create a new instance and you can choose if you would liek to make it part of public subnet or private Subnet.
- It chooses a availablility Zone on its own.And Automation has been intorduced as it has not been hardcoded.If tomorrow AWS comes with a new AWS for the region 
   it can pick automatically a new availiabilit zone
 - Based on the requirement , it can create based on instance count parameter in the root code.
 - 

## Running the stuff

The terraform codes are pulled to "HARBOR" the infrastructure server of the MIRA.You can simply fork it an run it in an AWS linux AMI.
When the comit is executed and the code is pushed to GitHUb , th epipeline kicks off in the TeamMIRA's Jenkins.


## Sonarcube  set up

Sonarcube is running in the Zeepipe Host using Docker.
