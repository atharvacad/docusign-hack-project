# Docusign Hack Project

This project consists of a backend API and a frontend application for managing agreements. The backend is built with Node.js and MongoDB, while the frontend is built with React.

## Project Structure

```markdown
## Project Structure

The project is divided into two main directories:

- `docusign-hack-project-back`: Contains the backend API built with Node.js and MongoDB.
- `docusign-hack-project-front`: Contains the frontend application built with React.

### Backend Directory Structure

```
docusign-hack-project-back/
├── src/
│   ├── controllers/
│   ├── models/
│   ├── routes/
│   ├── app.js
│   └── config.js
├── .env
├── package.json
└── README.md
```

### Frontend Directory Structure

```
docusign-hack-project-front/
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── App.js
│   ├── index.js
│   └── setupProxy.js
├── .env
├── package.json
└── README.md
```
```
## Prerequisites

- Node.js (v22 or higher)
- MongoDB (local or cloud instance)

## Setup Instructions

### Backend

1. Navigate to the backend directory:

    ```sh
    cd docusign-hack-project/docusign-hack-project-back
    ```

2. Install dependencies:

    ```sh
    npm install
    ```

3. Create a `.env` file:

    Create a `.env` file in the root directory of the backend project with the following content:

    ```properties
    MONGODB_URL=mongodb+srv://<username>:<password>@<cluster-url>
    DATABASE_NAME=docusign-hack-project
    COLLECTION_NAME=agreements
    PORT=3000
    ```

    Replace `<username>`, `<password>`, and `<cluster-url>` with your MongoDB credentials and cluster URL.

4. Start MongoDB:

    Ensure that MongoDB is running on your local machine or in a Docker container, or ensure that your MongoDB cloud instance is accessible.

5. Run the backend application:

    ```sh
    node src/app.js
    ```

    The server will start on the port specified in the `.env` file (default is 3000).

### Frontend

1. Navigate to the frontend directory:

    ```sh
    cd docusign-hack-project/docusign-hack-project-front
    ```

2. Install dependencies:

    ```sh
    npm install
    ```

3. Create a `.env` file:

    Create a `.env` file in the root directory of the frontend project with the following content:

    ```properties
    REACT_APP_BACKEND_URL=http://localhost:3000
    ```

    Replace `http://localhost:3000` with the URL of your backend server if it's different.

4. Run the frontend application:

    ```sh
    npm start
    ```

    The application will start on `http://localhost:3001`.

## License

This project is licensed under the MIT License.