# Bookstore-on-AWS-Fullstack

## Overview

The **Bookstore-on-AWS-Fullstack** project is a full-stack web application that provides an online platform for users to browse, search, and purchase books. This application is built using modern web technologies and is deployed on Amazon Web Services (AWS) to ensure scalability and reliability.

## Features

- **Browse Books**: Users can explore a wide range of books categorized by genres.
- **Search Functionality**: Quickly find books by title, author, or keywords.
- **User Authentication**: Secure login and registration system.
- **Shopping Cart**: Add books to the cart and manage quantities.
- **Order Management**: Review past orders and track current purchases.
- **Responsive Design**: Accessible on both desktop and mobile devices.

## Technologies Used

### Frontend

- **React.js**: JavaScript library for building user interfaces.
- **HTML5 & CSS3**: Markup and styling.
- **Bootstrap**: Responsive design framework.

### Backend

- **Spring Boot**: Java-based framework for building web applications.
- **RESTful API**: Handles client-server communication.

### Database

- **AWS RDS (Relational Database Service)**: Managed PostgreSQL database.

### Deployment

- **AWS EC2**: Virtual servers to host the application.
- **AWS S3**: Storage for static assets.
- **AWS Elastic Load Balancer (ELB)**: Distributes incoming traffic across multiple EC2 instances.
- **AWS CloudFormation**: Infrastructure as code for resource provisioning.

## Architecture

![Architecture Diagram](path_to_architecture_diagram.png)

The application follows a microservices architecture with the frontend and backend decoupled for independent development and deployment. AWS services are utilized to manage infrastructure, ensuring high availability and scalability.

## Getting Started

### Prerequisites

- **Node.js** (v14.x or later)
- **Java** (JDK 11 or later)
- **AWS CLI** configured with appropriate permissions
- **PostgreSQL** database instance

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/manankathrecha/Bookstore-on-AWS-Fullstack.git
   cd Bookstore-on-AWS-Fullstack

2. Backend Setup:
- Navigate to the backend directory:
  ```bash
  cd bookstore
  ```
- Update `application.properties` with your database configuration.
- Build the backend application:
  ```bash
  ./mvnw clean install
  ```
- Run the backend server:
  ```bash
  ./mvnw spring-boot:run
  ```

### 3. Frontend Setup:
- Navigate to the frontend directory:
  ```bash
  cd ../fullstack-frontend
  ```
- Install dependencies:
  ```bash
  npm install
  ```
- Start the frontend application:
  ```bash
  npm start
  ```
- The frontend should now be running on **[http://localhost:3000](http://localhost:3000)**
- The backend will be available on **[http://localhost:8080](http://localhost:8080)**

## Deployment (AWS)

### **Provision Infrastructure:**
- Utilize the provided **CloudFormation template** (`master-fullstack.yaml`) to set up AWS resources.
- Navigate to the **AWS CloudFormation console** and create a new stack using the template.

### **Deploy Backend:**
- Package the Spring Boot application as a JAR file.
- Upload it to an **S3 bucket**.
- Launch an **EC2 instance** and deploy the application.
- Ensure it's configured to connect to the **RDS instance**.

### **Deploy Frontend:**
- Build the React application:
  ```bash
  npm run build
  ```
- Upload the contents of the `build` directory to an **S3 bucket** configured for static website hosting.
- Optionally, set up **CloudFront** for CDN capabilities.

### **Configure Load Balancer:**
- Set up an **Elastic Load Balancer (ELB)** to distribute traffic between multiple backend instances.
- Ensure **security groups** and **network configurations** allow communication between components.

## Contributing
Contributions are welcome! Please fork the repository and submit a pull request for any enhancements or bug fixes.

## License
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

## Acknowledgements
Inspired by the AWS Bookstore Demo App. Thanks to all contributors and the open-source community.

