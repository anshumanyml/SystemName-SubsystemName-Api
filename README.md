# SystemName SubsystemName API


## Introduction

Microservice responsible for holding users data and settings.

## Getting Started

The configuration is defined in the file [appsettings](src/CompanyName.SystemName.SubsystemName.Api/appsettings.json) but you can use environment variables *(just use double underscores `__` instead of `:` for hierarchy)* that has priority.

### Dependencies

- Postgres Database
- APIs

### API Reference


## Build and Test

### Building

To build the project it's simple: just run `dotnet restore` and then `dotnet build` in the root of the project (same directory of the solution file `*.sln`).

PS: The project depends of some private NuGets from the Stone's artifactory. So you need that configured in your machine.

### Testing

Now the project has three major types of testing:

- **UnitTesting:** simplest type of test, focused on an unique aspect of the code with any dependency
- **IntegrationTesting:** responsible for testing the integration between layers and with dependencies (mainly database)
- **FunctionalTesting:** our functional requirements based tests, black box with a running instance of the application

All tests are marked with categories: `Unit`, `Integration` and `Functional`.

#### Unit Testing

Unit tests doesn't depend of anything, so just run them with:

```sh
dotnet test --filter Category=Unit
```

or

```sh
dotnet test --filter "Category!=Integration & Category!=Functional
```

#### Integration Testing


```sh
dotnet test --filter Category=Integration
```

#### Functional Testing

Same of the Integration Testing, but with the command:

```sh
dotnet test --filter Category=Functional
```

## Settings

### Supported Settings
These operations are supported by the current system.

### Foreseen Settings
These operations can be expected to be supported in future releases of the system.
