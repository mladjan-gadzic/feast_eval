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

In order to use `utils.py` set next env variables
```
export AWS_ACCESS_KEY_ID=user
export AWS_SECRET_ACCESS_KEY=password
export FEAST_S3_ENDPOINT_URL=http://127.0.0.1:9000
```