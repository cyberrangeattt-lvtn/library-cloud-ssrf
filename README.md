# Cloud SSRF & Container Escape

A linear CyberRangeCZ lab implementing the chain:

`SSRF → mock IMDSv1 → IAM credential → MinIO backup → SSH key → docker.sock → host root`

| Host | IP | Purpose |
|---|---:|---|
| kali-attacker | 172.20.0.5 | trainee workstation |
| webapp-vm | 172.20.0.10 | ImageResizer and mock IMDS |
| docker-host | 172.20.0.20 | portainer-lite and Docker 24.0.5 |
| minio-storage | 172.20.0.30 | S3-compatible storage |

Trainee account: `user` / `Password123`.

Provisioning requires outbound Internet access to download container images and MinIO/Docker binaries. Use only in an isolated cyber range.
