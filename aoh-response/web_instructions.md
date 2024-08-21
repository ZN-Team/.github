# AR2 Web Setup Guide

Welcome to the setup guide for the **AR2 Web** project. Follow these instructions to get the project up and running on your local machine.

## Prerequisites

Before you begin, ensure you have the following installed on your system:

- **Node.js** (v16.x or higher)
- **npm** (v8.x or higher)
- **Git** (for version control)

## 1. Clone the Repository

First, clone the repository to your local machine using the following command:

```bash
git clone https://github.com/DS-MSS-MARS/ar2-web.git
cd ar2-web
```

## 2. Checkout the Required Branch

Switch to the `c2box` branch, which is necessary for the project setup:

```bash
git checkout c2box
```

## 3. Install Dependencies

Install the required dependencies using npm:

```bash
npm install
```

This command will install all the packages listed in `package.json`.

## 4. Set Up Environment Variables

You will need to set up environment variables for the project. The necessary environment files will be provided separately. Once you have the `.env` and `.env.development` files, place them in the root directory of the project.

## 5. Generate Schema and Code

If you need to generate the GraphQL schema and related code, run the following commands:

### For macOS:
```bash
npm run getschema:mac
```

### For Windows:
```bash
npm run getschema:env
```

Then, generate the necessary code:

```bash
npm run generate
```

## 6. Run the Development Server

To start the development server, run the following command:

```bash
npm run dev
```

This command will concurrently start the development server and unit tests, allowing you to work on the project in real-time.

### To start the development server without running tests:

```bash
npm run dev:notest
```

## 7. **If You're Feeling Lazy**

If you prefer a more automated setup and you're using macOS, you can simply run:

```bash
npm run lazy-glenn
```

This command will clean up the environment, generate the schema, generate the code, and start the development server all in one go.

## 8. Building the Project

When you are ready to build the project for production, use the following command:

```bash
npm run build
```

This will generate the production-ready files in the `dist` directory.

## 9. Running Tests

The project includes several test scripts:

- **Unit Tests**: 
  ```bash
  npm run test:unit
  ```
- **End-to-End (E2E) Tests**: 
  ```bash
  npm run test:e2e
  ```
- **Component Tests**: 
  ```bash
  npm run test:comp
  ```

To run all tests at once:

```bash
npm run test
```

## 10. Preview the Build

To preview the production build, run:

```bash
npm run preview
```

This will start a local server that serves the built files.

## 11. Clean Up Generated Files

If you need to clean up generated files, you can use:

```bash
npm run clean
```

This command will remove all generated files from the `src/generated` directory.

---

You’re all set! If you encounter any issues or need further assistance, feel free to reach out to the project maintainers.

---

This guide now includes a shortcut for those who prefer to automate the setup process. Let me know if there's anything else you need!