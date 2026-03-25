# Purpose of the image

This is a minimal example for a "production grade" image that passes the follwing requirements:

- Is a multi-stage build
- Uses a non-root user
- Included a health-check
- Is minimal
- Uses pinned image versions, not "latest"
- Includes `LABELS` for OCI metadata
