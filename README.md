# Packer Templates

[![Packer](https://github.com/hammadhaqqani/packer/actions/workflows/packer.yml/badge.svg)](https://github.com/hammadhaqqani/packer/actions/workflows/packer.yml)
[![GitHub Pages](https://github.com/hammadhaqqani/packer/actions/workflows/pages.yml/badge.svg)](https://hammadhaqqani.github.io/packer/)
[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Packer](https://img.shields.io/badge/Packer-%23009639.svg?logo=packer&logoColor=white)](https://www.packer.io/)
[![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?logo=amazon-aws&logoColor=white)](https://aws.amazon.com/)
[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-ffdd00?style=flat&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/hammadhaqqani)

HashiCorp Packer templates for building AWS AMIs and machine images with automated provisioning.

## Templates

| Template | Description | Provider |
|----------|-------------|----------|
| `ami-aws.json` | Base AWS AMI with custom provisioning | AWS EBS |
| `aws-1.json` | AWS machine image configuration #1 | AWS EBS |
| `aws-2.json` | AWS machine image configuration #2 | AWS EBS |
| `redis-ami.json` | Redis server AMI template | AWS EBS |
| `redis-ami-digitalocean.json` | Redis server image for DigitalOcean | DigitalOcean |

## Prerequisites

- [Packer](https://www.packer.io/downloads) >= 1.7
- AWS CLI configured with appropriate credentials
- An AWS account with EC2 permissions

## Quick Start

```bash
# Clone the repo
git clone https://github.com/hammadhaqqani/packer.git
cd packer

# Validate a template
packer validate ami-aws.json

# Build an AMI
packer build ami-aws.json
```

## Project Structure

```
.
├── ami-aws.json                    # Base AWS AMI template
├── aws-1.json                      # AWS image config #1
├── aws-2.json                      # AWS image config #2
├── redis-ami.json                  # Redis AMI for AWS
├── redis-ami-digitalocean.json     # Redis image for DigitalOcean
├── first.sh                        # Provisioning shell script
├── welcome.txt                     # Welcome message for instances
└── .github/workflows/
    ├── packer.yml                  # CI: packer validate + fmt check
    └── pages.yml                   # GitHub Pages deployment
```

## CI/CD

Every push runs automated validation via GitHub Actions:

- **`packer fmt -check`** — Ensures consistent template formatting.
- **`packer validate`** — Validates template syntax and configuration.

## Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

## License

[MIT](LICENSE)

## Author

**Hammad Haqqani** — DevOps Architect & Cloud Engineer

- Website: [hammadhaqqani.com](https://hammadhaqqani.com)
- LinkedIn: [linkedin.com/in/haqqani](https://www.linkedin.com/in/haqqani)
- Email: phaqqani@gmail.com

---

If you find this useful, consider buying me a coffee!

[![Buy Me A Coffee](https://img.shields.io/badge/Buy%20Me%20A%20Coffee-ffdd00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black)](https://buymeacoffee.com/hammadhaqqani)