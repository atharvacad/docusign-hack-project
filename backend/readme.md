# Docusign Hack Project Backend

This is the backend API for the Docusign Hack Project. It allows you to create agreements by uploading PDF files and retrieve all agreements stored in the MongoDB database.

## Prerequisites

- Node.js (v14 or higher)
- MongoDB (local or cloud instance)

## Installation

1. **Clone the repository:**

    ```sh
    git clone https://github.com/your-username/docusign-hack-project-back.git
    cd docusign-hack-project-back
    ```

2. **Install dependencies:**

    ```sh
    npm install
    ```

3. **Create a `.env` file:**

    Create a `.env` file in the root directory of the backend project with the following content:

    ```properties
    MONGODB_URL=mongodb+srv://<username>:<password>@<cluster-url>
    DATABASE_NAME=docusign-hack-project
    COLLECTION_NAME=agreements
    PORT=3000
    OPENAI_API_KEY=your_openai_api_key
    ACCESS_TOKEN=your_docusign_access_token
    ACCOUNT_ID=your_docusign_account_id
    ```

    Replace `<username>`, `<password>`, and `<cluster-url>` with your MongoDB credentials and  URLcluster. Replace `your_openai_api_key` with your actual OpenAI API key.

4. **Start MongoDB:**

    Ensure that MongoDB is running on your local machine or in a Docker container, or ensure that your MongoDB cloud instance is accessible.

5. **Run the backend application:**

    ```sh
    node src/app.js
    ```

    The server will start on the port specified in the `.env` file (default is 3000).

## Libraries and APIs Used

### Backend Libraries

- **Express**: A minimal and flexible Node.js web application framework.
- **Mongoose**: An ODM (Object Data Modeling) library for MongoDB and Node.js.
- **Multer**: A middleware for handling `multipart/form-data`, which is primarily used for uploading files.
- **Axios**: A promise-based HTTP client for the browser and Node.js.
- **dotenv**: A module that loads environment variables from a `.env` file into `process.env`.
- **crypto**: A module that provides cryptographic functionality.
- **jsonwebtoken**: A library to work with JSON Web Tokens (JWT).
- **bcrypt**: A library to help hash passwords.
- **pg**: PostgreSQL client for Node.js.

### APIs

- **OpenAI API**: Used for interacting with the GPT-3.5-turbo model to generate AI insights and responses.

## License

This project is licensed under the MIT License.