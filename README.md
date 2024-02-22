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
