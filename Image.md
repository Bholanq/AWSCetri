![[Pasted image 20260526094103.png|372]]
### A **Dockerfile** is a **text file containing instructions** to build a Docker image.

It defines:

- Which base image to use
- What dependencies to install
- Which files to copy
- What command to run when the container starts

### A **base image** is the **starting image** used in a Dockerfile.

```
# pull base image for python
FROM python:3.8-slim

# set working directory in the image
WORKDIR /app
COPY . /app

# Run the application - this is just for the container
CMD ["python","app.py"]
```

- When we pull the base image we're essentially getting everything we need to run basic python scripts.
