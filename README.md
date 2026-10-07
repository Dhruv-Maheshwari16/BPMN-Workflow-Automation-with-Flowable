# Flowable Spring Boot Application

This repository contains a Spring Boot application integrated with the Flowable BPMN engine. The application demonstrates the use of Call Activities within Flowable processes and provides REST API endpoints to create, deploy, and complete tasks.

## Features

- **Flowable BPMN Engine Integration**: Leveraging Flowable for business process management and workflow automation.
- **Call Activity**: Demonstrates the use of Call Activity to invoke subprocesses within the main process.
- **REST API Endpoints**: Provides endpoints to interact with Flowable processes, including creating, deploying, and completing tasks.
- **Spring Boot**: Utilizes Spring Boot to simplify setup and configuration, making the application easy to run and maintain.

## Prerequisites

- Java 17 or higher
- Gradle / Gradle Wrapper
- MySQL Database

## Getting Started

### Clone the Repository

```bash
git clone https://github.com/Dhruv-Maheshwari16/BPMN-Workflow-Automation-with-Flowable.git
cd BPMN-Workflow-Automation-with-Flowable/demo
```

### Build and Run

Use the Gradle wrapper to build and run the application:

```bash
cd demo
./gradlew bootRun
```

On Windows:

```cmd
cd demo
gradlew.bat bootRun
```

## API Endpoints

The application exposes REST API endpoints to interact with Flowable processes:

### Create Process
Start a new process instance.
- **POST** `/api/process/start`
- **Request Body**: JSON containing the process definition key and initial variables.

### Deploy Process
Deploy a BPMN process definition.
- **POST** `/api/process/deploy`
- **Request Body**: JSON containing the BPMN XML or file path.

### Complete Task
Complete a user task with provided variables.
- **POST** `/api/task/complete`
- **Request Body**: JSON containing the task ID and variables:
```json
{
    "taskId": "12345",
    "variables": {
        "loanAmount": 10000,
        "accountBalance": 5000
    }
}
```

## Key Components

- **Flowable Configuration**: Configured to integrate with Flowable for managing process definitions and instances.
- **Service Tasks**: Demonstrates the use of `JavaDelegate` to handle service tasks within processes.
- **Call Activities**: Shows how to invoke subprocesses using Call Activity, allowing modular and reusable process components.

## Usage Scenarios

- **Loan Approval Workflow**: Demonstrates a loan approval process where subprocesses handle stages such as eligibility check and document verification.
- **Task Automation**: Automates repetitive tasks through Flowable processes with REST API integration for task management.

## Acknowledgements

This project is adapted from the open-source repository [Flowable-With-Springboot](https://github.com/Chirran-CR/Flowable-With-Springboot) by [Chirran-CR](https://github.com/Chirran-CR).

## License

This project is licensed under the MIT License.

## Author

- **Dhruv Maheshwari**  
  GitHub: [@Dhruv-Maheshwari16](https://github.com/Dhruv-Maheshwari16)  
  Email: maheshwaridhruv504@gmail.com
