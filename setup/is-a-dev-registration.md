# is-a.dev Custom Domain Registration Setup for Outbound Email

## Objective
Register a custom subdomain on is-a.dev and configure it as the verified Resend sending domain to unblock external outbound emails.

## Steps
1. Fork https://github.com/is-a-dev/register
2. Create `domains/paperclip.json`:
```json
{
  "owner": {
    "username": "your-github-username",
    "email": "your-email@example.com"
  },
  "record": {
    "CNAME": "paperclip-ai.pages.dev"
  }
}
```
3. Submit PR and wait for merge.
4. Add domain in Resend dashboard (resend.com/domains), copy DNS TXT/MX records, and verify DNS.
5. Update `CORS_ORIGIN` and `WORKER_URL` in `wrangler.toml` if the domain changes.
6. After DNS verification, update the 'from' address in `worker/src/tools/comms.ts`.

## Status
Awaiting manual approval for domain registration and DNS setup.

## Deliverables
- Validated, DNS-verified custom domain registered and configured in Resend
- Updated code referencing the new domain for outbound emails

---
This file documents the actionable registration and setup instructions for the custom domain email configuration.