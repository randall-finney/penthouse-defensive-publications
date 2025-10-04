# Defensive Publication: OTP MEMORY WORKING CONDITION

**Snapshot time (server local)**: 2025-10-04 11:56:25 CT  
**Publication time (UTC)**: 2025-10-04T17:12:07Z

## Purpose

This defensive publication establishes prior art for the OTP-based authentication flow integrated with Supabase session management and Row Level Security (RLS) policies.

## What's Included

- Sanitized code snapshot (no secrets, no build artifacts)
- SHA256/SHA512 checksums of original snapshot
- Manifest with technical details
- Documentation of working system state

## Verified Behavior

- ✅ OTP request/verify flow (email-based 6-digit codes)
- ✅ Supabase session creation (sb-access-token, sb-refresh-token cookies)
- ✅ Owner-only RLS policy (`auth.uid()` matching)
- ✅ Chat interface loads with proper authentication
- ✅ Memory retrieval accessible with owner context

## Technical Stack

- Next.js 14.1.0 (App Router + Pages API)
- Supabase (PostgreSQL + PostgREST + Auth)
- TypeScript middleware for auth flow
- Service role for RLS-bypassed operations

## Files

- `payload-sanitized.tar.gz` - Sanitized code snapshot
- `SHA256SUMS.txt` - SHA256 checksum of original archive
- `SHA512SUMS.txt` - SHA512 checksum of original archive
- `MANIFEST.json` - Technical manifest

## License

This publication is made available for defensive purposes to establish prior art.
No license is granted for use, modification, or distribution.

---

**Published by**: Alaric Thatcher (Operator)  
**Environment**: Penthouse-2 Staging
