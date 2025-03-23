## 📌 Architecture Overview

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
