Run MinIO instance with command 
```
docker run \
   -p 9000:9000 \
   -p 9001:9001 \
   --name minio \
   -v data:/data \
   -e "MINIO_ROOT_USER=user" \
   -e "MINIO_ROOT_PASSWORD=password" \
   quay.io/minio/minio server /data --console-address ":9001"
```

Create `my-bucket` bucket