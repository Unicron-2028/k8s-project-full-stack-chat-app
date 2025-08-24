# k8s-full-stack-chat-app

A **full-stack real-time chat application** deployed on **Kubernetes** via Minikube. This repo includes the original frontend and backend app by Iem Afzal Hassan, with **added Kubernetes deployment, Ingress, and environment configuration** by Gaurav Saini.

---

## Features
- Real-time chat with persistent storage
- User authentication (JWT)
- Scalable backend & frontend services
- Kubernetes deployment with Ingress
- Docker containerization for local testing
- Easy setup for Minikube and cloud deployment

---

## Tech Stack
- **Frontend:** React, TailwindCSS  
- **Backend:** Node.js, Express, Socket.io  
- **Database:** MongoDB  
- **Containerization:** Docker  
- **Orchestration:** Kubernetes  
- **Web Server:** Nginx  

---

## Screenshots

### Login Page
![Login Page](images/login.png)

### Initial Interface
![Initial Interface](images/interface.png)

### Live Chat Example
![Live Chat](images/live-chat.png)

> Place all screenshots in an `images` folder in your repo root.

---

## Environment Variables

Set the following in your **backend deployment**:

```yaml
env:
  - name: MONGODB_URI
    value: "mongodb://mongoadmin:secret@mongodb:27017/chatApp?authSource=admin"
  - name: JWT_SECRET
    value: "your_jwt_secret_here"

MONGODB_URI: MongoDB connection string (replace dbname if needed).

JWT_SECRET: JWT secret key (use a strong secret).

For local Docker setup, you can use .env with the same values.
```

## Kubernetes Deployment

Clone the repo:

```yaml
git clone https://github.com/your-username/k8s-full-stack-chat-app.git
cd k8s-full-stack-chat-app
```

## Apply Kubernetes resources:
kubectl apply -f .