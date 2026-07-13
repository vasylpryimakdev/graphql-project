# GraphQL Workshop

A simple GraphQL server example using `graphql-yoga`, `Prisma`, and `Apollo` tooling.

## Overview

This repository contains a minimal GraphQL application with:

- `graphql-yoga` server setup
- Prisma binding for CRUD access to a GraphQL database
- resolver files for `Query`, `Mutation`, `Subscription`, `User`, `Post`, and `Comment`
- environment-based scripts for development and testing
- Jest tests for core GraphQL operations

## Project Structure

- `src/` - application source code
  - `index.js` - app bootstrap and server startup
  - `server.js` - GraphQL server configuration
  - `prisma.js` - Prisma client binding
  - `db.js` - in-memory / database helpers
  - `schema.graphql` - GraphQL schema definitions
  - `resolvers/` - resolver implementations
  - `generated/` - generated Prisma schema output
- `prisma/` - Prisma service configuration
- `config/` - environment files for development, test, and production
- `tests/` - Jest integration tests and test helpers

## Requirements

- Node.js (supported versions for Babel 6 / GraphQL Yoga era)
- npm
- Prisma service configured and running if using the `prisma` endpoint

## Setup

1. Install dependencies:

```bash
npm install
```

2. Verify or configure Prisma and environment variables in `config/dev.env`.

3. Start the app in development mode:

```bash
npm run dev
```

4. Run tests:

```bash
npm test
```

## Available Scripts

- `npm run dev` - start the server with `env-cmd`, `nodemon`, and `babel-node`
- `npm start` - run the compiled app from `dist/index.js`
- `npm test` - run Jest tests with the test environment loaded
- `npm run get-schema` - fetch the GraphQL schema from the Prisma service using `graphql-cli`

## Notes

- The repository appears to be a learning/demo project, not a full production app.
- If you delete the unrelated `prisma-review-website/` folder, it should not affect this project.

## License

This project currently uses the `ISC` license.
