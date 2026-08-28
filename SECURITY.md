# Security Policy

## Reporting a Vulnerability

Please do not open a public issue for a suspected security vulnerability.

Report security concerns privately to the repository owner at `a2andwinning@gmail.com`. Include a clear description, affected area, reproduction steps if available, and any relevant impact.

## Security Baseline

eRecall is expected to handle sensitive user memory and conversation data. Future implementation should follow these principles:

- Never commit real secrets, credentials, private keys, tokens, or exported user data.
- Load configuration from environment variables or approved secret-management systems.
- Keep authentication and authorization boundaries explicit.
- Apply least privilege to databases, providers, services, and deployment credentials.
- Treat persistent memory as sensitive user data.
- Provide deletion and correction paths for stored user memory.
- Avoid logging raw sensitive inputs, credentials, provider responses, or private memory records.
- Validate API input and output at service boundaries.
- Review dependencies for security and maintenance risk before adoption.
- Prefer portable, inspectable, self-hostable infrastructure where practical.

## Supported Versions

The project is in pre-release foundation work. Supported versions will be defined once release artifacts exist.
