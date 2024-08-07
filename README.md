# Restaurant Review App

## Description
This is an Express.js application that uses various middlewares including `express-session`, `helmet`, and `express-validator`. It includes basic routes for rendering a home page and handling form submissions with validation.

## Features
- **Home Route**: Renders the home page.
- **Review Route**: Handles form submissions with validation for email, restaurant name, rating, and review content.

## Installation
1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/your-repo-name.git
    ```
2. Navigate to the project directory:
    ```sh
    cd your-repo-name
    ```
3. Install dependencies:
    ```sh
    npm install
    ```

## Usage
1. Start the server:
    ```sh
    npm start
    ```
2. Open your browser and navigate to `http://localhost:4001` (or the port specified in your environment variables).

## Code Overview
### Middleware
- **express.json()**: Parses incoming JSON requests.
- **express.urlencoded()**: Parses incoming requests with URL-encoded payloads.
- **express.static()**: Serves static files from the "public" directory.
- **helmet()**: Adds security-related HTTP headers.
- **express-session**: Manages user sessions.

### Routes
- **GET /**: Renders the home page using EJS.
- **POST /review**: Validates form data and redirects to either an error or success page based on the validation results.

### Example
#### Home Route
```javascript
app.get("/", (req, res) => {
  res.render("home");
});
