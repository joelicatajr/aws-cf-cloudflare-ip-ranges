# AWS CloudFormation Template for Cloudflare IP Ranges

This repository contains a CloudFormation template designed to create a security group in your AWS environment. This security group allows inbound traffic from all Cloudflare IP ranges on ports 80 and 443, and allows all outbound traffic. The template is specifically set up for the AWS `us-west-2` region but can be adapted to other regions by changing the region settings in AWS CloudFormation.

## Purpose

The sole purpose of this repository is to host a CloudFormation template that automates the creation of a security group configured to the IP ranges used by Cloudflare. This can be particularly useful for applications hosted in AWS that utilize Cloudflare as their content delivery network.

## Usage Instructions

To deploy this CloudFormation template using the AWS Management Console, follow these steps:

1. Login to your AWS account and navigate to the AWS CloudFormation console.
2. Click on 'Create stack' > 'With new resources (standard)'.
3. In the 'Specify template' section, select 'Upload a template file'.
4. Click on 'Choose file' and upload the `cloudflare_security_group.yaml` file from this repository.
5. Click 'Next'.
6. Enter a stack name, e.g., `CloudflareSecurityGroupSetup`.
7. Under 'Parameters', provide the VPC ID where you want the security group to be created.
8. Click 'Next', configure any stack options as necessary, and then click 'Next' again.
9. Review your settings, acknowledge that AWS CloudFormation might create IAM resources (if applicable), and click 'Create stack'.
10. Wait for the stack creation to complete, which will be indicated by the status 'CREATE_COMPLETE'.

You can now navigate to the EC2 console to verify that the security group has been created with the specified configurations.

## Requirements

- An AWS account is necessary to deploy the template.
- Ensure you have the necessary permissions to create resources in AWS CloudFormation and AWS EC2.

## Contributing

Contributions are welcome! If you have improvements or corrections to the template, please feel free to fork the repository and submit a pull request. Ensure your changes are thoroughly tested in an AWS environment before submitting.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contact Information

For any questions or feedback related to this repository, please contact me on Twitter: [@joelicatajr](https://twitter.com/joelicatajr).

You can also open an issue in the repository if you encounter any problems or have suggestions for enhancements.

## Copyright

Copyright © 2024 Joseph Licata. All rights reserved.