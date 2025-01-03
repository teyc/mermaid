# Use Case Diagram (v<MERMAID_RELEASE_VERSION>+)

> In the context of mermaid-js, the Use Case diagram is a powerful tool for visualizing the interactions between actors and use cases within a system. It helps in understanding the functional requirements and the relationships between different components of the system.

## Example

```mermaid-example
usecase-beta
    title Simple Use Case
    systemboundary
        title Acme System
        (Start)
        (Use) as (Use the application)
        (Another use case)
    end
    User -> (Start)
    User --> (Use)
    (Use) --> (Another use case)
```

## Syntax

### Title

The title is a short description of the diagram and it will always render on top of the diagram.

#### Example

```mermaid-example
usecase-beta
    title Arrows in Use Case diagrams
    actor Student
    actor Admin
    service Authentication
    service Grades
    service Courses
    systemboundary
        title Student Management System
        (Login) {
            - Authenticate
        }
        (Submit Assignment) {
            - Upload Assignment
        }
        (View Grades)
        (Manage Users) {
            - Add User
            - Edit User
            - Delete User
        }
        (Manage Courses) {
            - Add Course
            - Edit Course
            - Delete Course
        }
        (Generate Reports) {
            - Generate User Report
            - Generate Course Report
        }
        (View Grades) {
            - View User Grades
            - View Course Grades
        }
    end
    Student -> (Login) -> Authentication
    Student -> (Submit Assignment) -> Courses
    Student -> (View Grades) -> Grades
    Admin -> (Login) -> Authentication
    Admin -> (Manage Users) -> Courses
    Admin -> (Manage Courses) -> Courses
    Admin -> (Generate Reports) -> Courses, Grades
    Admin -> (View Grades) -> Grades
```

### System Boundary

The system boundary groups related use cases together and provides a title for the group.

#### Example

```mermaid-example
usecase-beta
    systemboundary
        title "Acme System"
        (Start)
        (Use) as (Use the application)
        (Another use case)
    end
```

### Actors and Services

Actors and services represent the entities that interact with the use cases.

#### Example

```mermaid-example
usecase-beta
    actor Student
    actor Admin
    service Authentication
    service Grades
    service Courses
```

### Relationships

Relationships define the interactions between actors, services, and use cases.

#### Example

```mermaid-example
usecase-beta
    Student -> (Login) -> Authentication
    Student -> (Submit Assignment) -> Courses
    Student -> (View Grades) -> Grades
    Admin -> (Login) -> Authentication
    Admin -> (Manage Users) -> Courses
    Admin -> (Manage Courses) -> Courses
    Admin -> (Generate Reports) -> Courses, Grades
    Admin -> (View Grades) -> Grades
```