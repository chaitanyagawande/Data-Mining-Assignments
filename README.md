# Data Mining Assignment 1 & Assignment 2

## Assignment 1
**ChatGPT Conversation Transcript:** The complete transcript of the ChatGPT conversation regarding the Fraud Detection EDA is available at https://chat.openai.com/share/98ef79e7-7430-4d24-8580-ffca14a51a94.

**PDF Version:** The ChatGPT conversation is also available https://github.com/chaitanyagawande/Data-Mining-Assignments/blob/main/Assignment%201/Fraud%20Detection%20EDA.pdf as a PDF for easy reference.

**Medium Blog:** A detailed walk-through of the study is published on Medium. You can read the blog https://medium.com/@cgawande12/a-comprehensive-guide-to-credit-card-fraud-detection-leveraging-data-science-from-start-to-finish-9ba58006d23c.

## Assignment 2 : Event Management REST API
Welcome to the Event Management REST API documentation. This project is a Java and Spring Boot application that allows you to manage events through a set of API endpoints. You can perform actions like adding, updating, listing, and deleting events using these endpoints. The project follows the MVC architecture, with clear separation of concerns among controllers, services, and repositories.

## Prompt for gpt-engineer
I want to create Event Management application using java and spring boot. This application should be able to add upcoming events, update event, list all events and delete event. Actually, I want to expose 4 API endpoints for performing above mentioned actions like adding, updating, deleting and list events. I want you to follow MVC architecture while developing this application: we will segregate our codebase into 3 parts, controller, services and repository respectively. In controller, you should mention API endpoints and call service level business logic, which further makes call to repository. Now, for simplicity repository class will store all events in arrayList. For every event, we need to create Event with fields like name, description, date & time. As this is spring boot application, I want complete directory structure of this project from your side. Main directories and files of any spring boot project are src/main/java, src/test/java, pom.xml, etc. The project should work end-to-end without any changes from my side. 

## gpt-engineer Response
The response given by gpt-engineer is present in https://github.com/chaitanyagawande/Data-Mining-Assignments/blob/main/Assignment%202/all_output.txt file located in Assignment 2 directory. 

## Project Structure

The project follows a typical Spring Boot directory structure:

- `src/main/java`: Contains the Java source code for the project.
- `src/test/java`: Contains test cases for the project.
- `pom.xml`: The project's Maven configuration file.

## Setup and Usage

To run the Event Management application, follow these steps:

1. Clone the repository to your local machine.
2. Make sure you have Java and Maven installed.
3. Navigate to "Assignment 2" directory.
4. Run `mvn spring-boot:run` to start the application.
5. You can now use the provided CURL commands to interact with the API.

## API Endpoints

### List All Events

Endpoint: `GET /event`

Retrieves a list of all events.

**Example CURL Request:**
```bash
curl --location --request GET 'http://localhost:8080/event'
```

### Add Event

Endpoint: `POST /event`

Adds a new event.

**Example CURL Request:**
```bash
curl --location --request POST 'http://localhost:8080/event' \
--header 'Accept: application/json' \
--header 'Content-Type: application/json' \
--data-raw '{
    "name" : "SJSU Job Fair",
    "description" : "SJSU Job Fair",
    "dateTime" : "2023-08-05"
}'
```

### Update Event

Endpoint: `PUT /event/{eventId}`

Updates an existing event.

**Example CURL Request:**
```bash
curl --location --request PUT 'http://localhost:8080/event/1' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json' \
--data-raw '{
    "name" : "SJSU Job Fair (Updated)",
    "description" : "SJSU Job Fair (Updated)",
    "dateTime" : "2023-08-10"
}'
```

### Delete Event

Endpoint: `DELETE /event/{eventId}`

Deletes an event.

**Example CURL Request:**
```bash
curl --location --request DELETE 'http://localhost:8080/event/1' \
--header 'Content-Type: application/json' \
--header 'Accept: application/json'
```

## Screencast

For a visual walkthrough of various use-cases and development steps, please find the recording https://drive.google.com/file/d/1e4JZaTTL0OoD2rzeEa3R86SKr2Qo7fTk/view?usp=drivesdk.

Feel free to reach out if you have any questions or need further assistance. Happy coding!
