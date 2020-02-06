# WAF

Associated with API Gateway, Cloudfront, and ALB.

- Allow all requests except ones specified.
- Block all requests except ones specified.
- Count requests matching properties specified.

- Web ACLs: Protection strategy for a set of *rules*.
- Rules: Individual statement with actions evalauated per request.
- Rule group: Reusable rules.

## Web ACL

Maximum capacity is 1,500.

If WAF has an internal error, CloudFront typically allows the request while API gateway and ALB will deny the request.

## Rules

- Allow
- Block
- Count

Statements:

- AND
- Geographic
- IP Set
- Managed Rule Group
- NOT
- OR
- Rate based
- Regex pattern-set
- Rule group
- Size constraint
- SQLi Attack
- String match
- XSS script

Components

- Header
- HTTP method
- Query string
- Body
- Single query parameter
- All query parameters (recommended)
- URI (path)

Text transforms

10 WCU

- None
- to lowercase
- HTML decode
- Normalize whitespace
- Simplifiy command line
- URL decode
