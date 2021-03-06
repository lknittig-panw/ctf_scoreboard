# Packer

## Validate AMI Configuration

- Update the file /scoreboard.json as needed.
- Update the ansible files in /playbooks as needed.
- Run the command `packer validate scoreboard.json`

## Build AMI

- Run `packer build scoreboard.json` to build
- Note the AMI ID at the end of the output when packer build completes successfully.
- Update the "default value of the variable "fw_ami" in the file /aws/variables.tf

## Remove

- Avoid charges to AWS account

- Remove the AMI by first deregistering it on the AWS AMI management page. 
  - https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Images:sort=name
- Next, delete the associated snapshot on the AWS snapshot management page.
