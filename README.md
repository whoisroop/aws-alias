# 🚀 AWS CLI Custom Aliases (EC2 & VPC Pack)

A curated collection of powerful, time-saving AWS CLI aliases for managing **EC2 compute resources**, **storage/AMIs**, and **VPC networking**. 

These aliases use custom JMESPath queries to output clean, human-readable summary tables directly in your terminal, minimizing the need to parse raw JSON responses.

---

## 📥 Installation

You can install and append these aliases directly to your local AWS CLI configuration file (`~/.aws/config`) by running the following command in your terminal:

```bash
curl -sSL https://raw.githubusercontent.com/whoisroop/aws-alias/main/aliases >> ~/.aws/config
```

### Manual Installation
If you prefer to add them manually:
1. Open your AWS CLI configuration file: `nano ~/.aws/config`
2. Ensure you have a `[toplevel]` section defined.
3. Copy and paste the contents of the `aliases` file into that section.

---

## 📋 Available Aliases & Quick Reference

### 🖥️ Core EC2 Operations Pack

| Command | Description | Example Usage |
| :--- | :--- | :--- |
| `aws ec2-list` | Lists all instances with ID, Name, Type, State, and IPs. | `aws ec2-list` |
| `aws ec2-running` | Filters and lists only currently running EC2 instances. | `aws ec2-running` |
| `aws ec2-types` | Displays instance types, vCPUs, and memory sizes. | `aws ec2-types` |
| `aws ec2-start` | Starts a specific EC2 instance. | `aws ec2-start i-0123456789abcdef0` |
| `aws ec2-stop` | Stops a specific EC2 instance. | `aws ec2-stop i-0123456789abcdef0` |
| `aws ec2-reboot` | Reboots a specific EC2 instance. | `aws ec2-reboot i-0123456789abcdef0` |
| `aws ec2-terminate`| Terminates a specific EC2 instance. | `aws ec2-terminate i-0123456789abcdef0` |
| `aws ebs-list` | Lists all EBS volumes, sizes, states, and encryption status.| `aws ebs-list` |
| `aws ami-list` | Lists available AMIs and creation dates. | `aws ami-list` |
| `aws ec2-ip` | Retrieves the Public IP of a specific instance ID. | `aws ec2-ip i-0123456789abcdef0` |
| `aws ec2-ssh-ready`| Generates ready-to-copy SSH strings for running instances.| `aws ec2-ssh-ready` |
| `aws keypair-list` | Lists available EC2 key pairs. | `aws keypair-list` |

---

### 🌐 Core VPC & Networking Pack

| Command | Description | Example Usage |
| :--- | :--- | :--- |
| `aws vpc-list` | Lists all VPCs, CIDRs, states, and default flags. | `aws vpc-list` |
| `aws subnet-list` | Lists all subnets across all VPCs. | `aws subnet-list` |
| `aws subnet-vpc` | Filters and lists subnets belonging to a specific VPC. | `aws subnet-vpc vpc-0123456789...` |
| `aws sg-list` | Lists all security groups with descriptions and VPC IDs. | `aws sg-list` |
| `aws sg-rules` | Inspects inbound rules for a specific security group. | `aws sg-rules sg-0123456789...` |
| `aws nacl-list` | Lists Network ACLs and their associated VPCs. | `aws nacl-list` |
| `aws igw-list` | Lists Internet Gateways and attachment states. | `aws igw-list` |
| `aws nat-list` | Lists NAT Gateways, public IPs, and states. | `aws nat-list` |
| `aws route-list` | Lists Route Tables and the number of active routes. | `aws route-list` |
| `aws eip-list` | Tracks Elastic IP allocations and attached instances. | `aws eip-list` |

---

## 💡 Requirements

* **AWS CLI v2**: Ensure you have the AWS CLI installed and configured (`aws configure`).
* **Permissions**: Ensure your active IAM user/role has standard read/write permissions for EC2 and VPC services.
