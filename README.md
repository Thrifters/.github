# 4Thrifters Market Place System

---

## Overview
The **4Thrifters Market Place System** is a dynamic platform designed to enhance user experience and engagement by recommending relevant products and similar items. It is built with the following technologies:

- **React.js** for the front-end.
- **FastAPI** for the back-end API service.
- **FastAPI-based AI microservice** to provide personalized recommendations and similar product suggestions using collaborative filtering.

This system improves engagement and sales by leveraging AI-driven recommendations.

---

## Project Architecture
### 1. Frontend (React.js)
- Provides a user-friendly interface for interacting with the system.
- Displays product recommendations and similar items.
- Communicates with the back-end API to fetch and render data dynamically.

### 2. Backend (FastAPI)
- Handles client requests and routes them to the AI microservice.
- Manages user interaction logs.

### 3. AI Microservice (FastAPI)
- Implements collaborative filtering using **Singular Value Decomposition (SVD)**.
- Exposes endpoints for generating recommendations and finding similar products.

---

## Technology Stack
### **Frontend**
- **Framework**: React.js
- **Styling**: CSS, Material-UI, or TailwindCSS
- **State Management**: React Context or Redux
- **Tools**: Axios for API calls, React Router for navigation

### **Backend**
- **Framework**: FastAPI
- **Database**: SQLite (development) or PostgreSQL (production)
- **Libraries**: SQLAlchemy (ORM), HTTPX (communication with AI microservice)

### **AI Microservice**
- **Framework**: FastAPI
- **Recommendation Engine**: Collaborative filtering using scikit-learn
- **Data Handling**: Pandas for preprocessing
- **Similarity Metrics**: Cosine similarity from scikit-learn

---

## Endpoints
### 1. AI Microservice
| **Endpoint**              | **Method** | **Description**                                     |
|---------------------------|------------|---------------------------------------------------|
| `/model/recommend/{user id}` | GET        | Returns recommended products for a user.          |
| `/model/similar/{product id}` | GET        | Returns similar products for a given product.     |

### 2. Backend API Service
| **Endpoint**                 | **Method** | **Description**                                   |
|------------------------------|------------|-------------------------------------------------|
| `/api/recommend/user/{user id}` | GET        | Fetches recommendations for a user from the AI service. |
| `/api/recommend/product/{product id}` | GET        | Fetches similar products from the AI service.    |

---

## Frontend Features
1. **User Dashboard**: Displays personalized product recommendations.
2. **Product Details Page**: Shows details of a specific product and lists similar items.
3. **Search and Filtering**: Allows users to search for products and apply filters.
4. **Interaction Tracking**: Logs user actions like adding to wishlist, viewing, or purchasing.

---

## Backend Implementation
### **Setup**
1. Clone the repository:
   ```bash
   git clone https://github.com/username/4thrifters-marketplace-system.git
   cd 4thrifters-marketplace-system
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the backend API service:
   ```bash
   uvicorn api_service:app --host 0.0.0.0 --port 8000 --reload
   ```

---

## AI Microservice Implementation
### **Setup**
1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

2. Run the AI microservice:
   ```bash
   uvicorn model_service:app --host 0.0.0.0 --port 8001 --reload
   ```

---

## Project Structure
```
4thrifters-marketplace-system/
|— backend/
|   |-- api_service.py
|   |-- requirements.txt
|   |-- data/
|— ai_microservice/
|   |-- model_service.py
|   |-- requirements.txt
|   |-- data/
|— frontend/
|   |-- src/
|   |-- public/
|   |-- package.json
|   ...
|— README.md
```

---

## License
This project is open-source and licensed under the **MIT License**.
