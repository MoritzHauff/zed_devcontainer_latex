# Use the official TeX Live image as a base image
FROM docker.io/texlive/texlive:latest

# Add a non-root user for development
# RUN useradd -ms /bin/bash dev

# Switch to the non-root user included in the TeX Live image
# UID 1000 is the default UID for the texlive user in the official TeX Live image
# This UID **must** match the UID of the user on the host system to avoid permission issues with mounted volumes
USER texlive

# Set the working directory
WORKDIR /home/texlive/work/
