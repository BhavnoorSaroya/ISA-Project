# ISA Microservices Architecture Project

## Overview
This project demonstrates a microservices architecture for a modern application, leveraging the benefits of modularity, scalability, and maintainability. The architecture consists of **7 distinct microservices**, each hosted across different origins and unified through a **custom Node.js API Gateway**.

The primary goal of this project is to showcase the potential of microservices to manage complex systems by dividing them into smaller, manageable services while ensuring seamless communication and integration.

## Architecture
### Key Components
1. **Auth Service**
   - Manages user authentication and authorization.
   - Implements JWT-based authentication with secure cookies.

2. **User Service**
   - Handles user profile management and stores user-related data in a database.

3. **Frontend Service**
   - A web-based UI for interacting with the application.

4. **AI Service**
   - Can live inference video files to output a live feed with drawn bounding boxes
   - Processes user-uploaded images using YOLO for object detection and annotation.
   - Tracks API usage and stores both original and processed images into the db service

6. **Notification Service**
   - Sends real-time updates and notifications to users.

8. **Analytics Service**
   - Gathers and analyzes usage data for insights and reporting via the gateway, since all traffic is routed through it

### API Gateway
The **Node.js API Gateway** consolidates these services under a single entry point, enabling seamless communication between the frontend and backend services. It handles:
- Routing requests to appropriate services.
- Centralized tracking thanks to the analytics service.
- Simplified service discovery for the frontend.


## Benefits of Microservices Architecture
- **Scalability:** Each service can be scaled independently based on its load.
- **Flexibility:** Easy to use different technologies and frameworks for different services.
- **Fault Isolation:** Failures in one service do not affect the others.
- **Ease of Deployment:** Individual services can be deployed and updated without impacting the entire system.
- **Team Autonomy:** Teams can own and manage specific services, promoting agility and faster development cycles.

## How to Run the Project
1. Clone the repositories for each microservice:
   - [Auth Service](https://github.com/BhavnoorSaroya/Auth-microservice)
   - [AI Service](https://github.com/BhavnoorSaroya/ai-microservice)
   - [User Service](https://github.com/BhavnoorSaroya/isa-database-microservice)
   - [Frontend service](https://github.com/BhavnoorSaroya/mock-frontend)
   - [Analytics Service](https://github.com/BhavnoorSaroya/isa-gateway-micrsoservice)
   - [Testing Front-End](https://github.com/BhavnoorSaroya/mock-frontend)
2. Set up the Node.js API Gateway:
   - Clone the [API Gateway repository](https://github.com/BhavnoorSaroya/isa-gateway-micrsoservice).
   - Install dependencies and start the gateway
3. Deploy the services on their respective origins.
4. Access the application via the API Gateway.

## Technologies Used
- **Backend:** Flask, Node.js, Python
- **Frontend:** React.js, Tailwind CSS, SvelteKit, PicoCss
- **Database:** PostgreSQL, SQLite
- **AI video inference:** YOLOv11, CUDA optimization
- **AI image inference:** YOLOv8 for object detection quickly in images
- **Gateway:** Node.js with `node-http-proxy-middleware`

## Future Enhancements
- **Service Mesh Integration:** Use a service mesh (e.g., Istio) for advanced traffic control and security.
- **CI/CD Pipeline:** Automate testing for all services, deployment is automatic with github actions. 
- **Advanced Analytics:** Enhance the analytics service with predictive modeling.

## Contributors
- [Ruben Gill](https://github.com/RubenGill)
- [Marvin Sio](https://github.com/Martxian/)
- [Yorick Aban](https://github.com/DaGunther)
- [Bhavnoor Saroya](https://github.com/BhavnoorSaroya)

## License


This project is licensed under the **GNU General Public License v3.0**.  
You can view the full license text in the [LICENSE](LICENSE) file.

[Learn more about the GPLv3.0](https://www.gnu.org/licenses/gpl-3.0.en.html).

