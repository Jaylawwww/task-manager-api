*Task Manager API Setup Instructions*

1. *Clone the repository*
   First, get the project from GitHub by cloning the repository to your computer. Navigate into the main project folder once it is downloaded.

2. *Locate the Symfony project folder*
   Inside the cloned folder, go into the api folder. This is where the Symfony application and all its files are located. Make sure you see folders like bin, config, public, src, vendor, and a file called .env.

3. *Start Docker and the database*
   Make sure Docker Desktop is running on your computer. Then, start the MySQL database container using the Docker Compose setup provided with the project. Wait until the container is running and verify that it is active. The database container is named task_manager_db and it will use port 3307.

4. *Install PHP dependencies*
   In the project folder, install all necessary PHP dependencies using Composer. This will download Symfony components, API Platform, and other required packages.

5. *Check database configuration*
   Open the .env file and confirm that the database connection URL is set correctly. The username should be root, the password root, the database name task_manager_api, and the port should match the Docker container, which is 3307.

6. *Create the database tables*
   Run the Doctrine migrations to create the tables needed for the project. If the database already exists, this step will simply ensure the tables are up to date.

7. *Start the Symfony server*
   Start the Symfony development server. Once it is running, you should be able to open your browser and go to http://localhost:8000 to see the Symfony welcome page.

8. *Access API Platform documentation*
   API Platform provides interactive API documentation automatically. Open your browser at http://localhost:8000/api to view all endpoints and test the API.

9. *Basic API usage*
   To create a task, send a POST request to /api/tasks with a title and description. To update a task, use a PATCH request to /api/tasks/{id}. To mark a task as completed, send a PATCH request with the isCompleted field set to true. These operations demonstrate how to create, update, and complete tasks in the system.

10. *Verify the database*
    The database is running inside Docker and stores all tasks. You can connect using any MySQL client to see the tables, or use Symfony commands to verify that the schema is correct.

11. *Submission checklist*
    Make sure the Docker container is running, the API documentation is visible at /api, tasks can be created and updated, and this README with setup instructions is included in your submission.
