
<h1 align="center">TNodeAPI</h1>



TNodeAPI is a simple Node.js API with authentication using JSON Web Tokens (JWT). It provides endpoints to access server files data with token authentication.

## Table of Contents
1. [Introduction](#introduction)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Endpoints](#endpoints)
5. [Integration](#integration)
6. [Dependencies](#dependencies)
7. [License](#license)

## Introduction

TNodeAPI is designed to provide a secure way to access server files data through HTTP requests. It implements token-based authentication using JSON Web Tokens, ensuring that only authorized users can access the server files.

## Installation

To install and run TNodeAPI, follow these steps:

1. **Clone this repository:**
   ```bash
   git clone <repository_url>
   ```

2. **Navigate to the project directory:**
   ```bash
   cd TNodeAPI
   ```

3. **Install dependencies:**
   ```bash
   npm install
   ```

4. **Start the server:**
   ```bash
   npm start
   ```

## Usage

1. **Access server files data:**
   - Make a GET request to `/api/serverfiles` with a valid token as a query parameter `token`.

## Endpoints

| Endpoint          | Description                               |
| ----------------- | ----------------------------------------- |
| `/api/serverfiles` | Retrieves server files data with token authentication. |

## Integration

To integrate TNodeAPI into your website, follow these steps:

1. **Install axios:**
   ```bash
   npm install axios
   ```

2. **Make HTTP requests to TNodeAPI endpoints:**
   - Use axios (or any other HTTP client) to make requests to TNodeAPI endpoints. For example:
   ```javascript
   const axios = require('axios');

   // Make a GET request to retrieve server files data
   axios.get('http://localhost:3000/api/serverfiles?token=<your_token>')
     .then(response => {
       console.log(response.data);
     })
     .catch(error => {
       console.error('Error:', error.response.data);
     });
   ```

## Dependencies

- [express](https://www.npmjs.com/package/express): Fast, unopinionated, minimalist web framework for Node.js.
- [jsonwebtoken](https://www.npmjs.com/package/jsonwebtoken): JSON Web Token implementation (symmetric and asymmetric).
- [axios](https://www.npmjs.com/package/axios): Promise based HTTP client for the browser and node.js.

## License

This project is licensed under the ISC License.
