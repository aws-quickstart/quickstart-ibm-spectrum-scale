## IBM Spectrum Scale on the AWS Cloud
Spectrum Scale version 4.2.3-1

### Deployment options:
* Deployment of IBM Spectrum Scale into a new VPC (end-to-end deployment) builds a new VPC with public and private subnets, and then deploys IBM Spectrum Scale into that infrastructure.
* Deployment of IBM Spectrum Scale into an existing VPC provisions IBM Spectrum Scale into your existing infrastructure. 

### Template Changes
* Added Master template (Create VPC and Bastion Enviornment)
  * Creates VPC using QuickStart Scaleable VPC template https://github.com/aws-quickstart/quickstart-aws-vpc
  * Creates Bastion host enviornment using QuickStart template as dependency https://github.com/aws-quickstart/quickstart-linux-bastion

* Workload Template
 * Added CloudWatch logs and alerts for Spectrum Scale server and compute nodes recovery.
 * Added Spectrum Scale SNS Topic
 
###Deployment steps:

* Sign up for an AWS account at http://aws.amazon.com, select a region, and create a key pair and one S3 bucket.
* In the AWS CloudFormation console, launch one of the following templates from the S3 URL to build a new stack:
  - [ibm-spectrum-scale-master.template](https://s3.amazonaws.com/quickstart-reference/ibm/spectrumscale/latest/templates/ibm-spectrum-scale-master.template) (to deploy and configure Spectrum Scale cluster into a new VPC)
  - [ibm-spectrum-scale.template](https://s3.amazonaws.com/quickstart-reference/ibm/spectrumscale/latest/templates/ibm-spectrum-scale-master.template) (to deploy and configure spectrum scale cluster into your existing VPC)

  For detailed deployment and configuration instructions, see the [Quick Start deployment guide](https://s3.amazonaws.com/quickstart-reference/ibm/spectrumscale/latest/doc/ibm-spectrumscale-on-the-aws-cloud.pdf).
