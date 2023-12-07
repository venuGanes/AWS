## Task 1: Launching Your EC2 Instance

- **Purpose**: Launch an EC2 instance with termination protection and a User Data script for a simple web server.
- **Steps**:
  1. Go to AWS Management Console > EC2 > Launch instance.
  2. Name instance: `Web Server`.
  3. Choose default Amazon Linux 2 AMI.
  4. Select instance type: `t3.micro`.
  5. Configure without a key pair.
  6. Set VPC to `Lab VPC` and create a security group for web server.
  7. Remove SSH access.
  8. Keep default storage.
  9. Enable termination protection and add User Data script.

## Task 2: Monitoring Your Instance

- **Purpose**: Monitor instance status and view CloudWatch metrics.
- **Steps**:
  1. Check instance status: Running with 2/2 checks passed.
  2. Review CloudWatch metrics.
  3. Monitor and troubleshoot with Get Instance Screenshot.

## Task 3: Accessing the Web Server

- **Purpose**: Update security group to allow HTTP traffic and access the web server.
- **Steps**:
  1. Copy instance's Public IPv4 address.
  2. Attempt to access the web server (will fail due to security group).
  3. Modify security group inbound rules to allow HTTP traffic (port 80).
  4. Refresh web page to view "Hello From Your Web Server!".

## Task 4: Resizing Your Instance

- **Purpose**: Resize instance type and EBS volume for better resources.
- **Steps**:
  1. Stop instance.
  2. Change instance type to `t3.small`.
  3. Modify EBS volume size from 8 GiB to 10 GiB.
  4. Start the resized instance.

## Task 5: Testing Termination Protection

- **Purpose**: Test termination protection and termination of the instance.
- **Steps**:
  1. Attempt to terminate instance (fails due to termination protection).
  2. Disable termination protection.
  3. Terminate instance successfully.
