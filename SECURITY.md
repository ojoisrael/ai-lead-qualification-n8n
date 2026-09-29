# Security Policy

## Scope

This repository contains a public, sanitized n8n workflow demonstrating AI-assisted lead qualification and automated follow-up.

## Supported Version

The latest version on the default `main` branch is the supported version for security reports.

## Reporting a Security Issue

Please contact me through:

https://ojo-israel-portfolio.lovable.app

Do not include secrets or private customer data in reports.

## Credential and Secret Handling

Never commit:

- API keys
- Access tokens
- Passwords
- Webhook secrets
- Database credentials
- Private customer data

Use n8n's credential manager or environment variables for sensitive values.

## Public Workflow

The workflow JSON is sanitized for portfolio sharing. Credentials, webhook identifiers, internal workflow metadata, and private connection details have been removed or replaced with placeholders.

The public workflow should be treated as a portfolio example. Reconnect services and review all expressions before using it in a live environment.
