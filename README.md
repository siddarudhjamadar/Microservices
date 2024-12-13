🚀 Hotel Review Microservices Project
This project implements a Hotel Review System using a microservices architecture. It enables users to search for hotels, leave reviews, and view aggregated reviews for hotels via different microservices. It uses Spring Boot, Eureka for service discovery, MongoDB for data persistence, and REST APIs for communication between services.

📜 Table of Contents
Overview
Technologies Used
Architecture Diagram
Microservices Overview
Setup Instructions
API Documentation
Database Configuration
Contributing
License
🏆 Overview
This project simulates a hotel review system composed of multiple microservices. The services handle core functionalities like hotel management, user management, and reviews, adhering to the microservices pattern for scalability, modularity, and fault tolerance.

🛠️ Technologies Used
The following technologies and frameworks were utilized in building this project:

Backend Framework: Spring Boot
Service Discovery: Eureka
Database: MongoDB
Communication Protocol: REST API
🏗️ Architecture Diagram
Below is an example architecture for this microservices application:

sql
Copy code
          +----------------------------------+  
          |            Eureka Server        |  
          |       (Service Discovery)      |  
          +----------------------------------+  
                       |      |      |  
           +-----------+      |      +------------+  
           |                      Hotel Service |  
           |         (CRUD Operations & Reviews)|  
           |                                  |  
           +-----------------+  +----------------+  
           |   Review Service  |  |   User Service |  
           |   (Post/View/Update/Delete Reviews) |  
           |   (User Authentication & Management)|  
           +-----------------+  +----------------+  
🛠️ Microservices Overview
1. Eureka Service
Responsibilities:
Act as a service discovery server.
Register all microservices dynamically.
Enables microservices to find and communicate with each other.
Tech Stack: Spring Boot, Eureka
2. Hotel Service
Responsibilities:
Manage hotel CRUD operations (create, read, update, delete).
Aggregate hotel review data.
Tech Stack: Spring Boot + MongoDB
3. Review Service
Responsibilities:
Manage user reviews on hotels (add, edit, delete, search reviews).
Tech Stack: Spring Boot + MongoDB
4. User Service
 user can register himself and can provide reviews.
Tech Stack: Spring Boot + Java

bash
Copy code
cd eureka-service
./mvnw spring-boot:run
Eureka dashboard should be accessible at:
http://localhost:8761




📊 Database Configuration
This application uses MongoDB as its database. Ensure MongoDB is up and running on your local machine or configure the database URI in the respective application.properties:

properties
Copy code
spring.data.mongodb.uri=mongodb://localhost:27017/<database_name>
🤝 Contributing
Contributions are welcome! If you find any issues or have feature requests, feel free to fork this repository and submit a pull request.
