FROM python:3.8

RUN apt-get update && apt-get install -y \
    libgl1-mesa-glx \
    && rm -rf /var/lib/apt/lists/*


# Install torch, torchvision, and Jupyter
RUN pip install torch==1.7.0 torchvision==0.8.1 jupyter


# Set up a working directory
WORKDIR /app

# Expose the Jupyter port
EXPOSE 8888

# Run Jupyter notebook
CMD ["jupyter", "notebook", "--ip=0.0.0.0", "--port=8888", "--no-browser", "--allow-root"]

