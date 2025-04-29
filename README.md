# My Node.js Application

This is a Node.js application that connects to a MySQL database. It uses Docker for easy deployment.

## Deployment

1. Clone the repository:

   git clone https://github.com/ashokee18/Faculty-Recruitment-Portal.git


2. Build and start the containers: docker-compose up -d

   This will build the Node.js application image and start the MySQL and Node.js containers in detached mode.


3. Check the logs to ensure both containers are running: docker-compose logs -f

   You should see the MySQL container initializing and the Node.js application starting up.


4. The Node.js application will be available at `http://localhost:8000`.


## Configuration

The MySQL database credentials and other configuration settings are defined in the `docker-compose.yml` file. You can modify these values as needed.

## Cleanup

To stop and remove the containers, run: docker-compose down
This will stop and remove the containers, but it will preserve the MySQL data volume.

To also remove the MySQL data volume, run: docker-compose down -v

## Notes

- The Node.js application code is expected to be in the same directory as the `Dockerfile` and `docker-compose.yml` files.
- The MySQL data is persisted in a named volume (`mysqldb_data`), which will be created if it doesn't exist.
- The Node.js application expects the MySQL database to be available at `mysqldb:3306`.
