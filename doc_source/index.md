# AWS Elastic Beanstalk Developer Guide

-----
*****Copyright &copy; 2018 Amazon Web Services, Inc. and/or its affiliates. All rights reserved.*****

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
+ [What Is AWS Elastic Beanstalk?](Welcome.md)
+ [Getting Started Using Elastic Beanstalk](GettingStarted.md)
+ [AWS Elastic Beanstalk Concepts](concepts.md)
   + [Web Server Environments](concepts-webserver.md)
   + [Worker Environments](concepts-worker.md)
   + [Design Considerations](concepts.concepts.design.md)
+ [Service Roles, Instance Profiles, and User Policies](concepts-roles.md)
   + [Elastic Beanstalk Service Role](concepts-roles-service.md)
   + [Elastic Beanstalk Instance Profile](concepts-roles-instance.md)
   + [Elastic Beanstalk User Policy](concepts-roles-user.md)
+ [Elastic Beanstalk Platforms](concepts-all-platforms.md)
   + [Elastic Beanstalk Supported Platforms](concepts.platforms.md)
   + [Custom Platforms](custom-platforms.md)
      + [Platform Definition Archive Contents](custom-platforms-pda.md)
      + [Platform Hooks](custom-platform-hooks.md)
      + [Platform Scripts](custom-platforms-scripts.md)
      + [Packer Instance Cleanup](custom-platforms-packercleanup.md)
      + [Platform.yaml File Format](platform-yaml-format.md)
+ [Tutorials and Samples](tutorials.md)
+ [Managing and Configuring AWS Elastic Beanstalk Applications](applications.md)
   + [The AWS Elastic Beanstalk Application Management Console](applications-console.md)
   + [Managing Application Versions](applications-versions.md)
   + [Configuring Application Version Lifecycle Settings](applications-lifecycle.md)
   + [Create an Application Source Bundle](applications-sourcebundle.md)
+ [Managing Environments](using-features.managing.md)
   + [The AWS Elastic Beanstalk Environment Management Console](environments-console.md)
   + [Creating an AWS Elastic Beanstalk Environment](using-features.environments.md)
      + [The Create New Environment Wizard](environments-create-wizard.md)
         + [The Old New Environment Wizard](environments-create-wizard-old.md)
      + [Clone an Elastic Beanstalk Environment](using-features.managing.clone.md)
      + [Terminate an Elastic Beanstalk Environment](using-features.terminating.md)
      + [Creating Elastic Beanstalk Environments with the AWS CLI](environments-create-awscli.md)
      + [Creating Elastic Beanstalk Environments with the API](environments-create-api.md)
      + [Constructing a Launch Now URL](launch-now-url.md)
      + [Creating and Updating Groups of AWS Elastic Beanstalk Environments](environment-mgmt-compose.md)
   + [Deploying Applications to AWS Elastic Beanstalk Environments](using-features.deploy-existing-version.md)
      + [Deployment Policies and Settings](using-features.rolling-version-deploy.md)
      + [Blue/Green Deployments with AWS Elastic Beanstalk](using-features.CNAMESwap.md)
   + [Configuration Changes](environments-updating.md)
      + [Elastic Beanstalk Rolling Environment Configuration Updates](using-features.rollingupdates.md)
      + [Immutable Environment Updates](environmentmgmt-updates-immutable.md)
   + [Updating Your Elastic Beanstalk Environment's Platform Version](using-features.platform.upgrade.md)
      + [Managed Platform Updates](environment-platform-update-managed.md)
      + [Migrating Your Application from a Legacy Container Type](using-features.migration.md)
   + [Canceling Environment Configuration Updates and Application Deployments](using-features.rollingupdates.cancel.md)
   + [Rebuilding AWS Elastic Beanstalk Environments](environment-management-rebuild.md)
   + [Environment Types](using-features-managing-env-types.md)
   + [AWS Elastic Beanstalk Worker Environments](using-features-managing-env-tiers.md)
   + [Creating Links Between AWS Elastic Beanstalk Environments](environment-cfg-links.md)
+ [AWS Elastic Beanstalk Environment Configuration](customize-containers.md)
   + [Your AWS Elastic Beanstalk Environment's Amazon EC2 Instances](using-features.managing.ec2.md)
   + [Auto Scaling Group for Your AWS Elastic Beanstalk Environment](using-features.managing.as.md)
      + [Auto Scaling Triggers](environments-cfg-autoscaling-triggers.md)
      + [Scheduled Auto Scaling Actions](environments-cfg-autoscaling-scheduledactions.md)
      + [Auto Scaling Health Check Setting](environmentconfig-autoscaling-healthchecktype.md)
   + [Load Balancer for Your AWS Elastic Beanstalk Environment](using-features.managing.elb.md)
      + [Configuring a Classic Load Balancer](environments-cfg-clb.md)
      + [Configuring an Application Load Balancer](environments-cfg-alb.md)
      + [Configuring a Network Load Balancer](environments-cfg-nlb.md)
      + [Configuring Access Logs](environments-cfg-loadbalancer-accesslogs.md)
   + [Adding a Database to Your Elastic Beanstalk Environment](using-features.managing.db.md)
   + [Your AWS Elastic Beanstalk Environment Security](using-features.managing.security.md)
   + [Tagging Resources in Your Elastic Beanstalk Environment](using-features.tagging.md)
   + [Environment Properties and Other Software Settings](environments-cfg-softwaresettings.md)
      + [Configuring AWS X-Ray Debugging](environment-configuration-debugging.md)
      + [Viewing Logs from Your Elastic Beanstalk Environment's Amazon EC2 Instances](environments-cfg-logging.md)
   + [Elastic Beanstalk Environment Notifications with Amazon SNS](using-features.managing.sns.md)
   + [Configuring Amazon Virtual Private Cloud (Amazon VPC) with Elastic Beanstalk](using-features.managing.vpc.md)
   + [Your Elastic Beanstalk Environment's Domain Name](customdomains.md)
+ [Advanced AWS Elastic Beanstalk Environment Configuration](beanstalk-environment-configuration-advanced.md)
   + [Configuration Options](command-options.md)
      + [Setting Configuration Options Before Environment Creation](environment-configuration-methods-before.md)
      + [Setting Configuration Options during Environment Creation](environment-configuration-methods-during.md)
      + [Setting Configuration Options After Environment Creation](environment-configuration-methods-after.md)
      + [General Options for All Environments](command-options-general.md)
      + [Platform Specific Options](command-options-specific.md)
      + [Custom Options](configuration-options-custom.md)
   + [Advanced Environment Customization with Configuration Files (.ebextensions)](ebextensions.md)
      + [Option Settings](ebextensions-optionsettings.md)
      + [Customizing Software on Linux Servers](customize-containers-ec2.md)
         + [Example: Using Custom Amazon CloudWatch Metrics](customize-containers-cw.md)
      + [Customizing Software on Windows Servers](customize-containers-windows-ec2.md)
      + [Adding and Customizing Elastic Beanstalk Environment Resources](environment-resources.md)
         + [Modifying the Resources that Elastic Beanstalk Creates for your Environment](customize-containers-format-resources-eb.md)
         + [Other AWS CloudFormation Template Keys](ebextensions-otherkeys.md)
         + [Functions](ebextensions-functions.md)
         + [Example Snippets](customize-environment-resources-examples.md)
            + [Example Snippets: ElastiCache](customize-environment-resources-elasticache.md)
            + [Example Snippet: SQS, CloudWatch, and SNS](customize-environment-resources-sqs.md)
            + [Example: DynamoDB, CloudWatch, and SNS](customize-environment-resources-dynamodb.md)
   + [Using Elastic Beanstalk Saved Configurations](environment-configuration-savedconfig.md)
   + [Environment Manifest (env.yaml)](environment-cfg-manifest.md)
   + [Creating a Custom Amazon Machine Image (AMI)](using-features.customenv.md)
   + [Configuring HTTPS for your Elastic Beanstalk Environment](configuring-https.md)
      + [Create and Sign an X509 Certificate](configuring-https-ssl.md)
      + [Upload a Certificate to IAM](configuring-https-ssl-upload.md)
      + [Configuring Your Elastic Beanstalk Environment's Load Balancer to Terminate HTTPS](configuring-https-elb.md)
      + [Configuring Your Application to Terminate HTTPS Connections at the Instance](https-singleinstance.md)
         + [Terminating HTTPS on EC2 Instances Running Docker](https-singleinstance-docker.md)
         + [Terminating HTTPS on EC2 Instances Running Go](https-singleinstance-go.md)
         + [Terminating HTTPS on EC2 Instances Running Java SE](https-singleinstance-java.md)
         + [Terminating HTTPS on EC2 Instances Running Node.js](https-singleinstance-nodejs.md)
         + [Terminating HTTPS on EC2 Instances Running PHP](https-singleinstance-php.md)
         + [Terminating HTTPS on EC2 Instances Running Python](https-singleinstance-python.md)
         + [Terminating HTTPS on EC2 Instances Running Ruby](https-singleinstance-ruby.md)
         + [Terminating HTTPS on EC2 Instances Running Tomcat](https-singleinstance-tomcat.md)
         + [Terminating HTTPS on Amazon EC2 Instances Running .NET](SSLNET.SingleInstance.md)
      + [Configuring End-to-End Encryption in a Load Balanced Elastic Beanstalk Environment](configuring-https-endtoend.md)
      + [Configuring Your Environment's Load Balancer for TCP Passthrough](https-tcp-passthrough.md)
      + [Storing Private Keys Securely in Amazon S3](https-storingprivatekeys.md)
+ [Monitoring an Environment](environments-health.md)
   + [Monitoring Environment Health in the AWS Management Console](environment-health-console.md)
   + [Basic Health Reporting](using-features.healthstatus.md)
   + [Enhanced Health Reporting and Monitoring](health-enhanced.md)
      + [Enabling AWS Elastic Beanstalk Enhanced Health Reporting](health-enhanced-enable.md)
      + [Enhanced Health Monitoring with the Environment Management Console](health-enhanced-console.md)
      + [Health Colors and Statuses](health-enhanced-status.md)
      + [Instance Metrics](health-enhanced-metrics.md)
      + [Publishing Amazon CloudWatch Custom Metrics for an Environment](health-enhanced-cloudwatch.md)
      + [Using Enhanced Health Reporting with the AWS Elastic Beanstalk API](health-enhanced-api.md)
      + [Enhanced Health Log Format](health-enhanced-serverlogs.md)
      + [Notifications and Troubleshooting](environments-health-enhanced-notifications.md)
   + [Manage Alarms](using-features.alarms.md)
   + [Viewing an Elastic Beanstalk Environment's Event Stream](using-features.events.md)
   + [Listing and Connecting to Server Instances](using-features.ec2connect.md)
   + [Viewing Logs from Your Elastic Beanstalk Environment's Amazon EC2 Instances](using-features.logging.md)
+ [Using Elastic Beanstalk with Other AWS Services](AWSHowTo.md)
   + [Using Elastic Beanstalk with Amazon CloudFront](AWSHowTo.cloudfront.md)
   + [Logging Elastic Beanstalk API Calls with AWS CloudTrail](AWSHowTo.cloudtrail.md)
   + [Using Elastic Beanstalk with Amazon CloudWatch](AWSHowTo.cloudwatch.md)
   + [Using Elastic Beanstalk with Amazon CloudWatch Logs](AWSHowTo.cloudwatchlogs.md)
   + [Using Elastic Beanstalk with DynamoDB](AWSHowTo.dynamoDB.md)
   + [Using Elastic Beanstalk with Amazon ElastiCache](AWSHowTo.ElastiCache.md)
   + [Using Elastic Beanstalk with Amazon Elastic File System](services-efs.md)
   + [Using Elastic Beanstalk with AWS Identity and Access Management](AWSHowTo.iam.md)
      + [Managing Elastic Beanstalk Instance Profiles](iam-instanceprofile.md)
      + [Managing Elastic Beanstalk Service Roles](iam-servicerole.md)
         + [Using Service-Linked Roles for Elastic Beanstalk](using-service-linked-roles.md)
      + [Controlling Access to Elastic Beanstalk](AWSHowTo.iam.managed-policies.md)
      + [Amazon Resource Name Format for Elastic Beanstalk](AWSHowTo.iam.policies.arn.md)
      + [Resources and Conditions for Elastic Beanstalk Actions](AWSHowTo.iam.policies.actions.md)
      + [Example Policies Based on Managed Policies](ExamplePolicies_AEB.md)
      + [Example Policies Based on Resource Permissions](AWSHowTo.iam.example.resource.md)
   + [Using Elastic Beanstalk with Amazon Relational Database Service](AWSHowTo.RDS.md)
   + [Using Elastic Beanstalk with Amazon Simple Storage Service](AWSHowTo.S3.md)
   + [Using Elastic Beanstalk with Amazon Virtual Private Cloud](vpc.md)
      + [Example: Launching an Elastic Beanstalk Application in a VPC with Bastion Hosts](vpc-bastion-host.md)
      + [Example: Launching an Elastic Beanstalk in a VPC with Amazon RDS](vpc-rds.md)
+ [Configuring your development environment for use with AWS Elastic Beanstalk](chapter-devenv.md)
+ [The Elastic Beanstalk Command Line Interface (EB CLI)](eb-cli3.md)
   + [Install the Elastic Beanstalk Command Line Interface (EB CLI)](eb-cli3-install.md)
      + [Install Python, pip, and the EB CLI on Linux](eb-cli3-install-linux.md)
      + [Install Python, pip, and the EB CLI on Windows](eb-cli3-install-windows.md)
      + [Install the EB CLI on macOS](eb-cli3-install-osx.md)
      + [Install the EB CLI in a Virtual Environment](eb-cli3-install-virtualenv.md)
   + [Configure the EB CLI](eb-cli3-configuration.md)
   + [Managing Elastic Beanstalk Environments with the EB CLI](eb-cli3-getting-started.md)
   + [Using the EB CLI with AWS CodeBuild](eb-cli-codebuild.md)
   + [Using the EB CLI with Git](eb3-cli-git.md)
   + [Using the EB CLI with AWS CodeCommit](eb-cli-codecommit.md)
   + [Using the EB CLI to Monitor Environment Health](health-enhanced-ebcli.md)
   + [Managing Multiple AWS Elastic Beanstalk Environments as a Group with the EB CLI](ebcli-compose.md)
   + [Troubleshooting issues with the EB CLI](eb-cli-troubleshooting.md)
   + [EB CLI Command Reference](eb3-cmd-commands.md)
      + [eb abort](eb3-abort.md)
      + [eb appversion](eb3-appversion.md)
      + [eb clone](eb3-clone.md)
      + [eb codesource](eb3-codesource.md)
      + [eb config](eb3-config.md)
      + [eb console](eb3-console.md)
      + [eb create](eb3-create.md)
      + [eb deploy](eb3-deploy.md)
      + [eb events](eb3-events.md)
      + [eb health](eb3-health.md)
      + [eb init](eb3-init.md)
      + [eb labs](eb3-labs.md)
      + [eb list](eb3-list.md)
      + [eb local](eb3-local.md)
      + [eb logs](eb3-logs.md)
      + [eb open](eb3-open.md)
      + [eb platform](eb3-platform.md)
      + [eb printenv](eb3-printenv.md)
      + [eb restore](eb3-restore.md)
      + [eb scale](eb3-scale.md)
      + [eb setenv](eb3-setenv.md)
      + [eb ssh](eb3-ssh.md)
      + [eb status](eb3-status.md)
      + [eb swap](eb3-swap.md)
      + [eb tags](eb3-tags.md)
      + [eb terminate](eb3-terminate.md)
      + [eb upgrade](eb3-upgrade.md)
      + [eb use](eb3-use.md)
      + [Common Options](eb3-cmd-options.md)
   + [EB CLI 2.6 (Deprecated)](eb-cli.md)
      + [Getting Started with Eb](command-reference-get-started.md)
      + [Deploying a Git Branch to a Specific Environment](command-reference-branch-environment.md)
      + [Eb Common Options](eb-cmd-options.md)
      + [EB CLI 2 Commands](eb-cmd-commands.md)
         + [branch](branch.md)
         + [delete](delete.md)
         + [events](eb-events.md)
         + [init](init.md)
         + [logs](logs.md)
         + [push](push.md)
         + [start](start.md)
         + [status](status.md)
         + [stop](stop.md)
         + [update](update.md)
   + [Elastic Beanstalk API Command Line Interface (deprecated)](using-api-cli.md)
      + [Getting Set Up](usingCLI.md)
      + [Common Options](CLTRG-common-args-api.md)
      + [Operations](OperationList-cmd.md)
+ [Deploying Elastic Beanstalk Applications from Docker Containers](create_deploy_docker.md)
   + [Single Container Docker Environments](docker-singlecontainer-deploy.md)
      + [Single Container Docker Configuration](create_deploy_docker_image.md)
   + [Multicontainer Docker Environments](create_deploy_docker_ecs.md)
      + [Multicontainer Docker Configuration](create_deploy_docker_v2config.md)
      + [Multicontainer Docker Environments with the AWS Management Console](create_deploy_docker_ecstutorial.md)
   + [Preconfigured Docker Containers](create_deploy_dockerpreconfig.md)
      + [Getting Started with Preconfigured Docker Containers](create_deploy_dockerpreconfig.walkthrough.md)
      + [Example: Using a Dockerfile to Customize and Configure a Preconfigured Docker Platform](create_deploy_dockerpreconfig.dockerfile.md)
   + [Configuring Docker Environments](create_deploy_docker.container.console.md)
   + [Running a Docker Environment Locally with the EB CLI](create_deploy_docker-eblocal.md)
+ [Deploying Go Applications to Elastic Beanstalk Applications](create_deploy_go.md)
   + [Using the AWS Elastic Beanstalk Go Platform](go-environment.md)
      + [Configuring the Application Process with a Procfile](go-procfile.md)
      + [Building Executable On-Server with a Buildfile](go-buildfile.md)
      + [Configuring the Reverse Proxy](go-nginx.md)
   + [Using the Elastic Beanstalk Docker-based Go Platform](go_docker_platform.md)
+ [Creating and Deploying Java Applications on AWS Elastic Beanstalk](create_deploy_Java.md)
   + [Getting Started with Java on Elastic Beanstalk](java-getstarted.md)
   + [Setting Up your Java Development Environment](java-development-environment.md)
   + [Using the AWS Elastic Beanstalk Tomcat Platform](java-tomcat-platform.md)
      + [Bundling Multiple WAR Files for Tomcat Environments](java-tomcat-multiple-war-files.md)
      + [Structuring your Project Folder](java-tomcat-platform-directorystructure.md)
      + [Configuring Your Tomcat Environment's Proxy Server](java-tomcat-proxy.md)
   + [Using the AWS Elastic Beanstalk Java SE Platform](java-se-platform.md)
      + [Configuring the Application Process with a Procfile](java-se-procfile.md)
      + [Building JARs On-Server with a Buildfile](java-se-buildfile.md)
      + [Configuring the Reverse Proxy](java-se-nginx.md)
   + [Adding an Amazon RDS DB Instance to Your Java Application Environment](java-rds.md)
   + [Using the AWS Toolkit for Eclipse](java-eclipsetoolkit.md)
      + [Managing Elastic Beanstalk Application Environments](create_deploy_Java.managingappenv.md)
         + [Changing Environment Type](create_deploy_Java.managingappenv.envtype.md)
         + [Configuring EC2 Server Instances Using AWS Toolkit for Eclipse](create_deploy_Java.managingappenv.ec2.md)
         + [Configuring Elastic Load Balancing Using AWS Toolkit for Eclipse](create_deploy_Java.managingappenv.elb.md)
         + [Configuring Auto Scaling Using AWS Toolkit for Eclipse](create_deploy_Java.managingappenv.as.md)
         + [Configuring Notifications Using AWS Toolkit for Eclipse](create_deploy_Java.managingappenv.sns.md)
         + [Configuring Java Containers Using AWS Toolkit for Eclipse](create_deploy_Java.container.md)
      + [Managing Multiple AWS Accounts](create_deploy_Java.accounts.md)
      + [Viewing Events](create_deploy_Java.events.md)
      + [Listing and Connecting to Server Instances](create_deploy_Java.ec2connect.md)
      + [Terminating an Environment](create_deploy_Java.terminating.md)
   + [Resources](create_deploy_Java.resources.md)
+ [Creating and Deploying Elastic Beanstalk Applications in .NET Using AWS Toolkit for Visual Studio](create_deploy_NET.md)
   + [Getting Started with .NET on Elastic Beanstalk](dotnet-getstarted.md)
   + [Setting Up your .NET Development Environment](dotnet-devenv.md)
   + [Using the AWS Elastic Beanstalk .NET Platform](create_deploy_NET.container.console.md)
      + [Migrating to v1 Elastic Beanstalk Windows Server Platforms](dotnet-v2migration.md)
      + [Running Multiple Applications and ASP.NET Core Applications with a Deployment Manifest](dotnet-manifest.md)
   + [Tutorial: How to Deploy a .NET Sample Application Using AWS Elastic Beanstalk](create_deploy_NET.quickstart.md)
   + [Deploying an ASP.NET Core Application with AWS Elastic Beanstalk](dotnet-core-tutorial.md)
   + [Adding an Amazon RDS DB Instance to Your .NET Application Environment](create_deploy_NET.rds.md)
   + [The AWS Toolkit for Visual Studio](dotnet-toolkit.md)
      + [Deploying to Your Environment](create_deploy_NET.sdlc.create.edit.md)
      + [Managing Your Elastic Beanstalk Application Environments](create_deploy_NET.managing.md)
         + [Configuring EC2 Server Instances Using the AWS Toolkit for Visual Studio](create_deploy_NET.managing.ec2.md)
         + [Configuring Elastic Load Balancing Using the AWS Toolkit for Visual Studio](create_deploy_NET.managing.elb.md)
         + [Configuring Auto Scaling Using the AWS Toolkit for Visual Studio](create_deploy_NET.managing.as.md)
         + [Configuring Notifications Using AWS Toolkit for Visual Studio](create_deploy_NET.container.sns.md)
         + [Configuring .NET Containers Using the AWS Toolkit for Visual Studio](create_deploy_NET.container.md)
      + [Managing Accounts](create_deploy_NET.accounts.md)
      + [Listing and Connecting to Server Instances](create_deploy_NET.ec2connect.md)
      + [Monitoring Application Health](create_deploy_NET.healthstatus.md)
      + [Deploying Elastic Beanstalk Applications in .NET Using the Deployment Tool](deploy_NET_standalone_tool.md)
   + [Resources](create_deploy_NET.resources.md)
+ [Deploying Node.js Applications to AWS Elastic Beanstalk](create_deploy_nodejs.md)
   + [Getting Started with Node.js on Elastic Beanstalk](nodejs-getstarted.md)
   + [Setting Up your Node.js Development Environment](nodejs-devenv.md)
   + [Using the AWS Elastic Beanstalk Node.js Platform](create_deploy_nodejs.container.md)
      + [Installing Packages with a Package.json File](nodejs-platform-packagejson.md)
      + [Locking Dependencies with npm shrinkwrap](nodejs-platform-shrinkwrap.md)
      + [Configuring the Proxy Server](nodejs-platform-proxy.md)
   + [Deploying an Express Application to Elastic Beanstalk](create_deploy_nodejs_express.md)
   + [Deploying a Node.js Application with DynamoDB to Elastic Beanstalk](nodejs-dynamodb-tutorial.md)
   + [Deploying a Geddy Application with Clustering to Elastic Beanstalk](create_deploy_nodejs_geddy_elasticache.md)
   + [Adding an Amazon RDS DB Instance to your Node.js Application Environment](create-deploy-nodejs.rds.md)
   + [Resources](create_deploy_nodejs.resources.md)
+ [Creating and Deploying PHP Applications on AWS Elastic Beanstalk](create_deploy_PHP_eb.md)
   + [Setting Up your PHP Development Environment](php-development-environment.md)
   + [Using the AWS Elastic Beanstalk PHP Platform](create_deploy_PHP.container.md)
      + [Composer File](php-configuration-composer.md)
      + [Update Composer](php-configuration-composerupdate.md)
      + [Extending php.ini](php-configuration-phpini.md)
   + [Deploying a Laravel Application to Elastic Beanstalk](php-laravel-tutorial.md)
   + [Deploying a CakePHP Application to Elastic Beanstalk](php-cakephp-tutorial.md)
   + [Deploying a Symfony Application to Elastic Beanstalk](php-symfony-tutorial.md)
   + [Deploying a High-Availability PHP Application with an External Amazon RDS Database to Elastic Beanstalk](php-ha-tutorial.md)
   + [Deploying a High-Availability WordPress Website with an External Amazon RDS Database to Elastic Beanstalk](php-hawordpress-tutorial.md)
   + [Deploying a High-Availability Drupal Website with an External Amazon RDS Database to Elastic Beanstalk](php-hadrupal-tutorial.md)
   + [Adding an Amazon RDS DB Instance to Your PHP Application Environment](create_deploy_PHP.rds.md)
+ [Working with Python](create-deploy-python-apps.md)
   + [Setting Up Your Python Development Environment](create-deploy-python-common-steps.md)
   + [Using the AWS Elastic Beanstalk Python Platform](create-deploy-python-container.md)
      + [Requirements File](python-configuration-requirements.md)
   + [Deploying a Flask Application to AWS Elastic Beanstalk](create-deploy-python-flask.md)
   + [Deploying a Django Application to Elastic Beanstalk](create-deploy-python-django.md)
   + [Adding an Amazon RDS DB Instance to Your Python Application Environment](create-deploy-python-rds.md)
   + [Python Tools and Resources](create-deploy-python-tools-resources.md)
+ [Deploying Elastic Beanstalk Applications in Ruby Using EB CLI and Git](create_deploy_Ruby.md)
   + [Using the AWS Elastic Beanstalk Ruby Platform](create_deploy_Ruby.container.md)
      + [Installing Packages with a Gemfile](ruby-platform-gemfile.md)
   + [Deploying a Rails Application to Elastic Beanstalk](create_deploy_Ruby_rails.md)
   + [Deploying a Sinatra Application to AWS Elastic Beanstalk](create_deploy_Ruby_sinatra.md)
   + [Adding an Amazon RDS DB Instance to Your Ruby Application Environment](create_deploy_Ruby.rds.md)
   + [Tools](create_deploy_Ruby.tools.md)
   + [Resources](create_deploy_Ruby.resources.md)
+ [Troubleshooting](troubleshooting.md)
   + [Connectivity](troubleshooting-connectivity.md)
   + [Environment Creation and Instance Launches](troubleshooting-envcreate.md)
   + [Deployments](troubleshooting-deployments.md)
   + [Health](troubleshooting-health.md)
   + [Configuration](troubleshooting-configuration.md)
   + [Troubleshooting Docker Containers](troubleshooting-docker.md)
   + [FAQ](troubleshooting-faq.md)
+ [Elastic Beanstalk Resources](RelatedResources.md)
+ [Platform History](platform-history.md)
   + [Packer Platform History](platform-history-packer.md)
   + [Single Container Docker Platform History](platform-history-docker-single.md)
   + [Multicontainer Docker Platform History](platform-history-docker-multi.md)
   + [Docker Platform Earlier History](platform-history-docker.md)
   + [Preconfigured Docker Platform History](platform-history-preconfigureddocker.md)
   + [Go Platform History](platform-history-go.md)
   + [Tomcat Platform History](platform-history-java.md)
   + [Java SE Platform History](platform-history-javase.md)
   + [.NET on Windows Server with IIS Platform History](platform-history-dotnet.md)
   + [Node.js Platform History](platform-history-nodejs.md)
   + [PHP Platform History](platform-history-php.md)
   + [Python Platform History](platform-history-python.md)
   + [Ruby Platform History](platform-history-ruby.md)