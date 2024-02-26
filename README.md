# Lecture-Lab


#  API Documentation

This repository contains an Express.js API for managing courses, lectures, and instructors.

## Installation

To install the dependencies, run:

```
npm install
```

## Usage

This API provides endpoints for user authentication, course management, lecture management, and instructor management.

## API Endpoints

### User API

- `POST /api/users/login`: Login a user.

### Course Controller API

- `POST /api/courses/addCourse`: Add a new course.
- `GET /api/courses/getAllCourses`: Get all courses.
- `POST /api/courses/getCourseDetailsById`: Get course details by ID.

### Lecture API

- `POST /api/courses/assignBatchToCourse`: Assign a batch to a course.
- `POST /api/courses/getAllAssigned`: Get all assigned lectures.
- `POST /api/courses/assignBatch`: Assign batches to an instructor.
- `POST /api/courses/getBatchByCourseId`: Get batches by course ID.

### Instructor API

- `POST /api/instructor/register`: Register a new instructor.
- `GET /api/instructor/getAllInstructor`: Get all instructors.
- `POST /api/instructor/deactivateInstructor`: Deactivate an instructor.

## Middleware

- `multer`: Middleware for handling file uploads.
- `validateTokenHandler`: Middleware for validating authentication tokens.

## Controllers

- `courseController`: Controller for course-related operations.
- `instructorController`: Controller for instructor-related operations.

## Sample Requests

### Example: Adding a Course

```javascript
POST /api/courses/addCourse
{
  "name": "Introduction to Express.js",
  "description": "A beginner-friendly course on Express.js"
}
```

Response:
```json
{
  "success": true,
  "message": "Course added successfully",
  "course": {
    "name": "Introduction to Express.js",
    "description": "A beginner-friendly course on Express.js",
    "createdAt": "2024-02-26T12:00:00Z"
  }
}
```

## Authentication

Token-based authentication is used for accessing protected endpoints. Include the token in the request headers.

## Error Handling

Errors are returned with appropriate HTTP status codes and error messages in the response body.

## Deployment

Deployed  the application to a hosting service or server.

## Contributing

Feel free to contribute by opening issues or pull requests.

## License

This project is licensed under the [MIT License](LICENSE).

---

Ensure to update the README.md file with relevant information and keep it up-to-date as the project evolves.
