Here's the revised README with TypeScript set to ES2022:

---

# Express-Typescript-Prisma Boilerplate 2024

This repository is a boilerplate setup for an application using Express, TypeScript, and Prisma. The project is managed using pnpm, and it uses the latest TypeScript features with ES2022.

## Features

- **Express**: A minimal and flexible Node.js web application framework.
- **TypeScript**: Superset of JavaScript that adds static types, enhancing code quality and developer experience.
- **Prisma**: Next-generation ORM for Node.js and TypeScript.
- **pnpm**: Fast, disk space efficient package manager.
- **dotenv**: Loads environment variables from a .env file into process.env.

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v14 or later)
- [pnpm](https://pnpm.io/)

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/your-repo.git
   cd your-repo
   ```

2. Install dependencies:
   ```bash
   pnpm install
   ```

### Scripts

- **Build**: Compiles TypeScript files.

  ```bash
  pnpm run build
  ```

- **Start**: Runs the compiled JavaScript files.

  ```bash
  pnpm start
  ```

- **Dev**: Runs the application in development mode, watching for file changes.
  ```bash
  pnpm dev
  ```

### TypeScript Configuration

The project uses the latest TypeScript features with `ES2022`. You can find the TypeScript configuration in `tsconfig.json`.

### Prisma Setup

1. Initialize Prisma:

   ```bash
   npx prisma init
   ```

2. Set up your database connection in the `.env` file.

3. Deploy the Prisma schema:
   ```bash
   npx prisma migrate dev --name init
   ```

### Project Structure

- **src/**: Contains the source code.
  - **index.ts**: The entry point of the application.

### Example Code

```typescript
import express from "express";
import { PrismaClient } from "@prisma/client";

const app = express();
const prisma = new PrismaClient();

app.use(express.json());

app.get("/", (req, res) => {
  res.send("Hello World!");
});

const PORT = process.env.PORT || 3000;
app.listen(PORT, () => {
  console.log(`Server is running on port ${PORT}`);
});
```

### Contributing

Contributions are welcome! Please open an issue or submit a pull request.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

Replace `yourusername/your-repo` with your actual GitHub username and repository name. This README provides an overview, setup instructions, and example code to get users started with your boilerplate.
