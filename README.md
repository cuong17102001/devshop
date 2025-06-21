# 🛠️ DevShop

## 🚀 Cách chạy dự án

### Clone dự án các service storage
```bash
git clone [URL of project]
cd [project name]
```

### Khởi động các dịch vụ Docker

```bash
docker-compose up -d
```

### Reset tài khoản kibana, elaticsearch hoặc lấy token.

```bash
#reset password
docker exec -it [elastic contaner name] /usr/share/elasticsearch/bin/elasticsearch-reset-password -u [user name... usually (elastic, kibana,...)]

#lấy token
docker exec -it [elastic contaner name] /bin/bash
bin/elasticsearch-service-tokens create elastic/kibana kibana-server-token
```


- Token sẽ được generate, sau đó hãy copy vào "elasticsearch.serviceAccountToken" để chạy được service kibana.

##### 🥸 Note: chỉ được dùng tài khoản kibana_system để dịch vụ kibana có quyền đọc ghi elastic search