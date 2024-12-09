# NEST JS ❤️

## Some basic commands 😀

- Installing Nest CLI globally for helping you use Nest commands more easily:

  ```bash
  npm i -g @nestjs/cli
  ```

- Creating a new Nest project:

  ```bash
  nest new project-name
  ```

- Generating a module:

  ```bash
  nest generate module module_name
  ```

  The module generator creates a new module in your Nest project. Modules are used to organize the application structure and manage dependencies between different parts of the application.

- Generating a controller:

  ```bash
  nest generate controller controller_name
  ```

  Controllers handle incoming requests and return responses to the client. They are responsible for defining routes and request handling logic.

- Generating a service:

  ```bash
  nest generate service service_name
  ```

  Services contain the business logic of the application. They are used to encapsulate reusable code and separate concerns within the application.

- Generating a resource:

  ```bash
  nest generate resource resource_name
  ```

  Resources are similar to controllers but provide a more RESTful approach to handling requests. They automatically generate CRUD (Create, Read, Update, Delete) endpoints for a given resource.

- Running the project:

  ```bash
  npm run start:dev
  ```

  This command starts the Nest project in development mode, allowing you to test and debug your application locally.

## Architecture 🧬

### Main

- **main.ts**: This file is the entry point of the application. It initializes the Nest application instance and microservice instance. Here, you can configure global settings and bootstrap the application.

- **app.module.ts**: The root module of the application. It imports other modules, declares controllers, and provides services. Modules help organize the application into cohesive blocks of functionality.

- **app.controller.ts**: Root controller of the application. Controllers define routes and request handling logic. They use decorators like `@Get()`, `@Post()`, etc., to specify HTTP methods and route paths.

- **app.service.ts**: Root service of the application. Services contain the business logic of the application. They encapsulate reusable code and separate concerns within the application.

### Module

- Modules help organize the application into cohesive blocks of functionality. They encapsulate related components, such as controllers, services, and providers.

### Controllers

- Controllers handle incoming requests and return responses to the client. They define routes using decorators like `@Get()`, `@Post()`, etc., and request handling logic.

### Providers (Services)

- Providers, such as services, contain the business logic of the application. They encapsulate reusable code and separate concerns within the application. Providers can be injected into controllers, services, and other providers.

### Good resources

- [NestJS Documentation](https://docs.nestjs.com/): Official documentation for NestJS, providing detailed guides and API references.

- [Bulletproof node.js project architecture 🛡️](https://dev.to/santypk4/bulletproof-node-js-project-architecture-4epf): A helpful resource for understanding project architecture in Node.js applications.