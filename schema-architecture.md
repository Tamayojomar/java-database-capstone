This Spring Boot application uses both MVC and REST. The Admin and Doctor dashboards are built with Thymeleaf templates, while other features use REST APIs. 
The application works with two databases: MySQL stores structured data like patients, doctors, appointments, and admins, and MongoDB stores prescription data. 
All requests go through a service layer, which handles the business logic and communicates with the databases through repositories. 
This structure keeps the code organized and easy to maintain.

1. User Interface Layer
Users interact with the application either through Thymeleaf-based dashboards (Admin and Doctor) or via REST API clients (mobile apps or frontend modules like Appointments and PatientDashboard). This allows both web-based and API-based access.
2. Controller Layer
Requests from users are routed to backend controllers. Thymeleaf Controllers handle server-rendered HTML pages, while REST Controllers process API requests and return JSON responses. Controllers validate requests and coordinate the initial processing.
3. Service Layer
Controllers delegate business logic to the Service Layer, which applies rules, validates inputs, and coordinates workflows, such as checking doctor availability before scheduling appointments. This keeps business logic separate from controllers.
4. Repository Layer
The Service Layer communicates with repositories to access data. MySQL repositories manage structured relational data, while MongoDB repositories handle flexible document-based data like prescriptions. Repositories simplify database interactions.
5. Database Access
Repositories interface with the actual databases. MySQL stores structured entities like patients, doctors, and appointments, while MongoDB stores unstructured or nested data such as prescriptions, allowing schema flexibility.
6. Model Binding
Retrieved data is converted into Java objects. MySQL data is mapped into JPA entities, and MongoDB data is mapped into document objects. These model classes provide a consistent way to work with data in the application.
7. Application Models in Use
The models are used to generate responses. In MVC flows, they populate Thymeleaf templates for dynamic HTML. In REST flows, they are serialized into JSON and sent to clients, completing the request-response cycle.
