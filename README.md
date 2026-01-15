 - do not over-simplify
 - do not repeat tools (provided in [CNCF](https://landscape.cncf.io) or [Adopters](https://github.com/cncf/landscape2/blob/main/ADOPTERS.md))

# Unified Cloud Landscape

A comprehensive, unified landscape of major cloud providers (AWS, Azure, GCP, OCI) and their services, with cross-cloud capabilities highlighted.

## Quick Start

### Installation

```bash
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/cncf/landscape2/releases/download/v1.1.0/landscape2-installer.sh | sh
```

### Build the Landscape

```bash
cd unified-cloud-landscape
landscape2 build \
  --data-file data.yml \
  --settings-file settings.yml \
  --guide-file guide.yml \
  --logos-path logos \
  --output-dir build
```

### View the Landscape

```bash
landscape2 serve --landscape-dir build
```

Then open your browser to `http://localhost:8000`

## Structure

This unified landscape is designed for easy expansion with additional cloud providers.

### Adding a New Cloud Provider

To add a new cloud provider (e.g., IBM Cloud, Alibaba Cloud):

1. **Update `data.yml`**: Add a new category with the provider's name
2. **Add subcategories** for major service areas:
   - Compute Services
   - Storage Services
   - Database Services
   - Networking Services (optional)
   - Analytics & Big Data (optional)
3. **List key services** in each subcategory with descriptions and links

### Example Format for New Provider

```yaml
- name: New Cloud Provider
  subcategories:
    - name: Compute Services
      items:
        - name: Service Name
          description: Service description
          homepage_url: https://example.com
          logo: provider.svg
          project: graduated
```

## Categories

### Cloud Providers
- **AWS** - Amazon Web Services with 200+ services
- **Microsoft Azure** - Enterprise cloud with Microsoft integration
- **Google Cloud Platform** - Innovation-focused with strong data/ML
- **Oracle Cloud Infrastructure** - Enterprise databases and compute

### Cross-Cloud Services
- **Multi-Cloud Networking** - VPCs, Load Balancing, DNS/CDN
- **Multi-Cloud Security** - IAM, Encryption, Compliance
- **Multi-Cloud Analytics** - Data Warehousing, Streaming, ML
- **Integration & DevOps** - CI/CD, IaC, Monitoring

## Features

✅ **Comprehensive Coverage** - Major services from each cloud provider
✅ **Easy Expansion** - Add new providers by extending data.yml
✅ **Cross-Cloud View** - Highlights services available across platforms
✅ **Interactive Visualization** - Landscape2 provides filtering and search
✅ **Documentation** - Detailed guide for each category and service

## Design Philosophy

This unified landscape serves several purposes:

1. **Cloud Provider Comparison** - Understand available services across major clouds
2. **Multi-Cloud Strategy** - Identify services with consistent patterns across providers
3. **Migration Planning** - See equivalent services when moving between clouds
4. **Cost Optimization** - Compare offerings to choose the best provider per workload
5. **Extensibility** - Easily add new providers as cloud market evolves

## Resources

- [Landscape2 Documentation](https://github.com/cncf/landscape2)
- [AWS Services](https://aws.amazon.com/products/)
- [Azure Services](https://azure.microsoft.com/en-us/services/)
- [GCP Services](https://cloud.google.com/products)
- [OCI Services](https://www.oracle.com/cloud/services/)
