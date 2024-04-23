# NestJS JWT Authentication TypeORM PostgreSQL

## Description
This project is focused on building a RESTful API using Nest.js. It includes features such as managing cat profiles, user authentication, and favorites functionality. The backend is powered by a PostgreSQL database managed with TypeORM. User authentication is implemented using Passport.js with JWT tokens. Input validation and serialization are handled using class-validator and class-transformer.

To ensure code quality and prevent committing bad coding practices, Husky library has been configured. This setup includes formatting checks with Prettier and test case execution. Any commit attempt with formatting issues or failing test cases will be prevented.

## Features
- **Cat Profiles**: CRUD operations for managing cat profiles available for adoption.
- **User Authentication**: Secure registration and login functionality for users.
- **Favorites**: Authenticated users can mark cats as favorites.

## Technical Specifications
- **Database**: PostgreSQL database with TypeORM.
- **Authentication**: Passport.js with JWT tokens.
- **Validation and Serialization**: class-validator and class-transformer.

## Endpoints

- **POST /auth/register**: Register a new user.
- **POST /auth/login**: Authenticate a user and return a JWT.
- **GET /cats**: Retrieve a list of all cats.
- **POST /cats**: Create a new cat profile (admin only).
- **GET /cats/{id}**: Retrieve a cat profile by ID.
- **PUT /cats/{id}**: Update a cat profile by ID (admin only).
- **DELETE /cats/{id}**: Delete a cat profile by ID (admin only).

## Installation
1. Clone the repository: `git clone https://github.com/clown0000/NestJS-JWT-TypeORM-PostgreSQL`
2. Navigate to the project directory: `cd nest-test-assignment`
3. Install dependencies: `npm install`

## Configuration
1. Ensure you have PostgreSQL installed and running.
2. Configure the database connection in the `src/config/typeorm.ts` file.
3. Set environment variables as needed (e.g., JWT secret, database credentials) using a `.env` file.

### Additionally, to manage database migrations and seed data, utilize the following CLI commands:
- **Migration Creation**: Create a new migration file.
  ```bash
  npm run migration:create --name=mymigration
- **Generate Migration**: Generate SQL migration scripts based on changes in entities.
  ```bash
  npm run migration:generate --name=mymigration
- **Run Migrations**: Execute pending migrations to update the database schema.
  ```bash
  npm run migration:run
- **Revert Migrations**: Revert the last executed migration.
  ```bash
  npm run migration:revert
- **Seed Database:**: Create seed data, such as an admin user, in the database.
  ```bash
  npm run seed

## Usage
- **Development**: `npm run start:dev`
- **Production**: `npm run start:prod`

## Testing
- **Run tests**: `npm test`
- **Run tests with coverage**: `npm run test:cov`

## Additional Notes
- Ensure proper setup of environment variables for sensitive information like database credentials and JWT secret.
- Consider securing endpoints requiring admin privileges properly.
- Always handle errors gracefully and provide appropriate error responses.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
Special thanks to the Nest.js community and contributors for providing an excellent framework for building scalable and maintainable applications.
