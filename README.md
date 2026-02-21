PRESTASHOP DEPLOYMENT ON AWS FREE TIER
 PROJECT OVERVIEW 
 This project documents the deployment of a PrestaShop e-commerce application on AWS Free Tier using a separate database architecture.

The objective was to:

 • Launch a cloud-based server
 • Deploy and configure the application
 • Host the database separately from the application server
 • Ensure public accessibility
 • Clean up cloud resources to avoid unnecessary billing

This project required extensive troubleshooting, persistence, and infrastructure understanding.

ARCHITECTURE 
 • Application Server: Amazon EC2 (Ubuntu)
 • Database Server: Amazon RDS (MySQL)
 • Application: PrestaShop
 • File Transfer Tool: FileZilla
 • Access Method: SSH (PowerShell)

The database was intentionally hosted separately from the application server to follow better architectural and security practices.

IMPLEMENTATION STEPS
 EC2 Setup
 • Launched Ubuntu EC2 instance (Free Tier)
 • Configured Security Group:
   Port 22 (SSH)
   Port 80 (HTTP)
 • Connected securely using SSH key pair
  Screenshot:

Application Deployment
 • Downloaded PrestaShop ZIP file
 • Uploaded to /var/www/html/
 • Extracted and configured files
 • Resolved file permission issues
 • Completed browser-based installation
 • Removed install directory for security
 📸 Screenshot:

Database Configuration 
 • Created MySQL database using RDS
 • Configured:
   Database name
   Username
   Password
 • Connected PrestaShop to RDS endpoint
 • Verified successful database connection
 📸 Screenshot:

Networking & Public Access
 • Assigned and managed Elastic IP
 • Verified public accessibility via instance public IP
 • Confirmed admin panel functionality
 • Troubleshot network interface and IP release issues
 📸 Screenshot:

TROUBLESHOOTING HIGHLIGHTS 
 This deployment required:
 • Several hours resolving ZIP extraction challenges
 • Multiple SSH and PowerShell commands
 • File permission debugging
 • Network interface and Elastic IP troubleshooting
 • Persistent reconfiguration before successful deployment

The extraction and configuration stage was the most time-consuming part of the project.

RESOURCE CLEANUP
 To prevent unexpected billing:

 • EC2 instance terminated
 • RDS database deleted
 • Elastic IP released
 • Custom security groups removed
 • Default security group retained (standard AWS behavior)

KEY SKILLS STRENGTHED
 • Cloud infrastructure setup
 • Linux file and permission management
 • Secure network configuration
 • Separate database architecture
 • Troubleshooting under pressure
 • Cost-aware cloud resource management

SECURITY OPERATIONS PERSPECTIVE 
 Although this was a cloud deployment project, it strengthened my understanding of how systems are built and configured in cloud environments.

Understanding infrastructure from a deployment perspective improves the ability to monitor, detect, and respond effectively within a SOC environment.
