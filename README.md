# 🛠️ DevShop

## 🚀 Cách chạy dự án

### Clone dự án
```bash
git clone [URL of project]
cd [project name]
```

### Khởi động các dịch vụ Docker

```bash
docker-compose up -d
```

### Reset tài khoản kibana, elaticsearch.

```bash
docker exec -it [elastic contaner name] /usr/share/elasticsearch/bin/elasticsearch-reset-password -u [user name... usually (elastic, kibana,...)]
```

- Token sẽ được generate, sau đó hãy copy vào "elasticsearch.serviceAccountToken" để chạy được service kibana.
