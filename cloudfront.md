# Cloudfront

## Billing

Charged for

- Data out from pop
- Data in from origin

## Configuration

### Origin

Must delete cache behaviours before deletion.

Types of origins

- S3 bucket
- S3 website
- MediaStore container
- MediaPackage endoint
- EC2 instance (plain DNS)
- ELB

When using S3, do not use transfer acceleration domain name.

Can only use HTTP Only for S3 websites.

Default origin response timeout is 30 seconds.

Default origin keep-alive timeout: 5s.

Can add custom headers.

### Cache

Specify path pattern.

Allowed HTTP options:

- GET, HEAD
- GET, HEAD, OPTIONS
- GET, HEAD, OPTIONS, PUT, POST, PATCH, DELETE]

Only GET, HEAD, (optionally) OPTIONS are cached.

Can cache based on object headers:

- None
- Whitelist
- All (no caching)

Can use `Cache-Control` header to control TTL of cached objects. Can specify max, min, and default cache even if `cache-control` is present.

Querying string forwards & cache:

- None (Improves caching)
- Forward all, cache based on whitelist
- Forward all, cache based on all

### Distribution

Can enable IPv6 unless you are using signed URLs or signed cookies, or if using a custom policy using `IpAddress`.

## Signed URLs & cookies

Can specify

- End datetime for URL validity
- (optional) Start datetime for URL validity
- (optional) Valid IP addresses

Must use RSA-SHA1.

Recommended to rotate every 90 days.

Use signed URLs when:

- Want to use RTMP.
- Want to restrict individual files.
- Users use a client that does not support cookies.

Signed cookies when:

- Want to provide access to multiple files.
- Don't want to change URLs.

Cannot use signed cookies/URLs if the following query string parameters are present:

- Expires
- Policy
- Signature
- Key-Pair-Id
