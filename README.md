# my-wallet-infra


|-- my-wallet/api/              # Backend (Spring Boot)
|-- my-wallet-front/             # Frontend (React)
|-- my-wallet-infra/             # Infraestrutura (Kubernetes)
    |-- k8s/
        |-- postgres/            # Configurações do PostgreSQL
            |-- deployment.yml
            |-- service.yml
            |-- secret.yml
        |-- backend/             # Configurações do Backend
            |-- deployment.yml
            |-- service.yml
            |-- secret.yml
        |-- frontend/            # Configurações do Frontend
            |-- deployment.yml
            |-- service.yml
        |-- ingress.yml          # Configuração do Ingress (opcional)


Aplique os Secrets:


```bash
kubectl apply -f my-wallet-infra/k8s/postgres/secret.yml
kubectl apply -f my-wallet-infra/k8s/backend/secret.yml
```

```bash
kubectl apply -f my-wallet-infra/k8s/postgres/deployment.yml
kubectl apply -f my-wallet-infra/k8s/postgres/service.yml
```

```bash
kubectl apply -f my-wallet-infra/k8s/backend/deployment.yml
kubectl apply -f my-wallet-infra/k8s/backend/service.yml
```


```bash
kubectl apply -f my-wallet-infra/k8s/frontend/deployment.yml
kubectl apply -f my-wallet-infra/k8s/frontend/service.yml
```

```bash
Copy
kubectl apply -f my-wallet-infra/k8s/ingress.yml
```
