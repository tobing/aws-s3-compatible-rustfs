# AWS S3 Compatible Storage with RustFS  

A self-hosted, S3-compatible object storage deployment using RustFS and Docker Compose.  

This project provides an S3-compatible storage environment with support for bucket management, IAM users, access policies.  

Features
- S3 Compatibility – Access object storage using S3-compatible application WinSCP.  
- Docker Compose – Simple containerized deployment.  
- IAM Users – Create separate users for applications and services.  
- Bucket-Level Policies – Configure access permissions for individual buckets.  
- Access Control – Support ReadOnly, ReadWrite, and ReadWriteDelete permission models.  
- Public Access – Configure anonymous read access when required.  

# Start   
Clone this repo
```
git clone https://github.com/tobing/aws-s3-compatible-rustfs.git
cd aws-s3-compatible-rustfs
```

Modify ```RUSTFS_ACCESS_KEY``` and ```RUSTFS_SECRET_KEY``` in [`.env`](.env)
```
RUSTFS_ACCESS_KEY=myadmin
RUSTFS_SECRET_KEY=password123
```

Change permission for [`data`](data) and [`logs`](logs)
```
sudo chown -R 10001:10001 data logs
```

Run with docker compose
```
docker compose up -d
```

Check if any error
```
docker compose logs
```



# Configuration

Access web console from
```
http://127.0.0.1:9001
```

Sign in using ```RUSTFS_ACCESS_KEY``` and ```RUSTFS_SECRET_KEY``` from [`.env`](.env)




https://github.com/user-attachments/assets/48d73294-d796-46bc-a943-d3bf8fc6c0b0


