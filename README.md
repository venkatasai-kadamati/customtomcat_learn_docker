````markdown
## Tomcat Dockerfile

This Dockerfile builds an image for Apache Tomcat based on CentOS 7.

### Prerequisites

-   Docker installed and configured on your system.

### Building the Image

1. Navigate to the directory containing the Dockerfile.
2. Run the following command to build the image:

    ```bash
    docker build -t custom-tomcat-image:latest .
    ```

**Use code with caution.**

### Running the Container

Start a container from the image:

```bash
docker run -d -p 8080:8080 --name my-tomcat-server custom-tomcat-image:latest
```
````

**Use code with caution.**

This maps port 8080 on your host machine to port 8080 within the container.

### Accessing the Tomcat Server

Open a web browser and navigate to [http://localhost:8080](http://localhost:8080).

### Customizing the Image

You can customize this Dockerfile by changing the `tomcat_version` ARG to specify a different Tomcat version.

### Explanation of Dockerfile

-   `FROM centos:7`: Specifies the base image for your container.
-   Installs required dependencies and Java.
-   Downloads and extracts Apache Tomcat.
-   Sets permissions and ownership for Tomcat directories.
-   Downloads a sample WAR file for deployment.
-   Exposes port 8080.
-   Starts Tomcat using `catalina.sh`.

```
This README provides instructions for building and running the custom Tomcat Docker image, along with explanations of the Dockerfile's commands.
```
