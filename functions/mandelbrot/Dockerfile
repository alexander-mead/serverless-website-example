# Base image (specifying OS/Python etc.)
FROM public.ecr.aws/lambda/python:3.9

# Commands to run when creating the image
# NOTE: The order matters here, as the layers are built up
COPY requirements.txt ./
RUN python3.9 -m pip install -r requirements.txt -t .
COPY mandelbrot.py lambda.py ./

# What is actually run (entry point)
CMD ["lambda.handler"]