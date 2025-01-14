# cloud-engineer-project
A hands-on project showcasing AWS skills for cloud engineering
# Scalable Web Application on AWS
## Project Purpose
This project demonstrates the deployment of a scalable web application on AWS using Terraform. It is designed to showcase infrastructure-as-code principles and provide a robust, highly available architecture. The application is capable of handling traffic dynamically, stores static assets efficiently, and uses a managed database for persistent data storage.

## AWS Services Used
The following AWS services are utilized in this project:

- **Amazon VPC**: For creating isolated network infrastructure.
- **Amazon EC2**: For hosting the application instances.
- **Elastic Load Balancer (ELB)**: For distributing traffic across multiple EC2 instances.
- **Amazon S3**: For storing static assets and serving them via a public endpoint.
- **Amazon RDS**: For hosting a managed MySQL database.
- **Amazon CloudWatch**: For monitoring and logging.
- **AWS IAM**: For securing resource access with roles and policies.

## Deployment Steps

### Prerequisites
- Install [Terraform](https://www.terraform.io/downloads).
- Configure AWS CLI with appropriate credentials (`aws configure`).
- Have access to a public key for SSH access to EC2 instances.

### Steps

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/aws-web-app-project.git
   cd aws-web-app-project
   ```

2. **Initialize Terraform**
   Run the following command to initialize Terraform and download necessary providers:
   ```bash
   terraform init
   ```

3. **Customize Variables (Optional)**
   Update any variables in the `variables.tf` file to match your requirements (e.g., region, instance types, or database settings).

4. **Plan the Deployment**
   Create a plan to ensure the configuration is correct:
   ```bash
   terraform plan
   ```

5. **Apply the Configuration**
   Deploy the infrastructure:
   ```bash
   terraform apply
   ```
   Confirm the action when prompted.

6. **Access Resources**
   - Obtain the DNS name of the load balancer from the Terraform output.
   - Access the web application in your browser using the provided DNS name.

7. **Clean Up Resources**
   When you are done with the project, destroy the infrastructure to avoid unnecessary costs:
   ```bash
   terraform destroy
   ```

## Additional Notes
- **Security**: The project uses basic security groups to allow HTTP, HTTPS, and SSH traffic. For production, consider implementing stricter rules.
- **Database Credentials**: Replace hardcoded credentials with secrets managed via AWS Secrets Manager for better security.
- **Monitoring**: Leverage CloudWatch metrics and alarms to monitor application performance and resource utilization.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

