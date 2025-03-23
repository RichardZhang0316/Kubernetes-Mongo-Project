## Architecture Overview

The deployment follows this architecture: 

Mongo Express UI  
   ↓  
Mongo Express External Service → (Exposes Mongo Express outside the cluster)  
   ↓  
Mongo Express Pod → (Runs Mongo Express)  
   ↓  
MongoDB Internal Service → (Allows Mongo Express to communicate with MongoDB)  
   ↓  
MongoDB Pod → (Runs the MongoDB database)

---

## Setups

```bash
# Apply Secrets
kubectl apply -f mongodb-secret.yaml

# Deploy MongoDB
kubectl apply -f mongodb-deployment.yaml
kubectl apply -f mongodb-service.yaml

# Apply ConfigMap
kubectl apply -f mongodb-configmap.yaml

# Deploy Mongo Express
kubectl apply -f mongo-express-deployment.yaml
kubectl apply -f mongo-express-service.yaml
```

---
## Run
If using Minikube, expose the service:
minikube service mongo-express-service
