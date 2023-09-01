# Event Management REST API - README

Welcome to the Event Management REST API documentation. This project is a Java and Spring Boot application that allows you to manage events through a set of API endpoints. You can perform actions like adding, updating, listing, and deleting events using these endpoints. The project follows the MVC architecture, with clear separation of concerns among controllers, services, and repositories.

## Table of Contents

- [API Endpoints](#api-endpoints)
  - [List All Events](#list-all-events)
  - [Add Event](#add-event)
  - [Update Event](#update-event)
  - [Delete Event](#delete-event)
- [Project Structure](#project-structure)
- [Setup and Usage](#setup-and-usage)
- [Screencast](#screencast)
- [Contributing](#contributing)
- [License](#license)

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

## Project Structure

The project follows a typical Spring Boot directory structure:

- `src/main/java`: Contains the Java source code for the project.
- `src/test/java`: Contains test cases for the project.
- `pom.xml`: The project's Maven configuration file.

## Setup and Usage

To run the Event Management application, follow these steps:

1. Clone the repository to your local machine.
2. Make sure you have Java and Maven installed.
3. Navigate to the project directory.
4. Run `mvn spring-boot:run` to start the application.
5. You can now use the provided CURL commands to interact with the API.

## Screencast

For a visual walkthrough of various use-cases and development steps, please refer to the provided screencast.

## Contributing

Contributions to this project are welcome. Feel free to open issues or submit pull requests for improvements or bug fixes.

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to reach out if you have any questions or need further assistance. Happy coding!
