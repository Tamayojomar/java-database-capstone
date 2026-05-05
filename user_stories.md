|name              | about	                                                               |title	                        |  labels       |	assignees |
|------------------|-----------------------------------------------------------------------|------------------------------|---------------|-----------|
|User User Stories |	Functional user stories for the user role in the Smart Clinic system |	"[STORY] User User Stories"	| user-stories	|           |

>[!IMPORTANT]
>Ensure each user story defines system goals clearly and reflects realistic user workflows.
>Validate features support data privacy, usability, and secure access.

## **Role: User**

As a user
I need core capabilities to manage my account and appointments
So that I can بسهولة access healthcare services and track my medical interactions.


### User Story 1 – User Registration

As a user, I want to create an account, so that I can access the system and book appointments.

User can fill out a registration form with valid details
System validates input and prevents duplicate accounts
Account is successfully created and stored in the database

Include email validation and password rules
Optionally add email verification

###  User Story 2 – User Login

As a user, I want to log into my account, so that I can manage my appointments.

User can enter valid login credentials
System authenticates and redirects to the dashboard
Invalid credentials show an error message
Secure password handling
Add session timeout for security

### User Story 3 – Book Appointment

As a user, I want to book an appointment with a doctor, so that I can receive medical consultation.

User can select a doctor and available time slot
System checks doctor availability
Appointment is saved and confirmed

Prevent double booking
Show confirmation after booking

### User Story 4 – View Appointments

As a user, I want to view my appointments, so that I can keep track of my schedule.

User can see a list of all upcoming and past appointments
Appointment details are displayed clearly
Data is retrieved correctly from the database

Sort by date (upcoming first)
Allow filtering if needed

### User Story 5 – Cancel Appointment

As a user, I want to cancel an appointment, so that I can manage changes in my schedule.

User can select an appointment to cancel
System updates the appointment status
Cancelled appointment is removed or marked appropriately

Add cancellation rules (e.g., not allowed last minute)
Notify doctor if cancelled
