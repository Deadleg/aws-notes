# API Gateway

{api-id}.execute-api.{region}.amazonaws.com

## Types

Edge: runs on POP nodes. Global presence.
Regional: Only deployed in region, better connection throughput.
Private: Only accessable through VPC.

## Authentication

- `CUSTOM`
- `COGNITO_USER_POOLS`
- `AWS_IAM`

## Lambda backend

- Proxy integration
- Custom (non-proxy integration
- Async integration: `x-amz-invocation-type: Event`
