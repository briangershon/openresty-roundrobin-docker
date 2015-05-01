FROM debian:jessie

# Install python3
RUN     apt-get update
RUN     apt-get install -y python3

# Copy html
ADD static/ /src
WORKDIR /src

CMD ["python3", "-m", "http.server", "80"]

# Run http server on port 80
EXPOSE  80
