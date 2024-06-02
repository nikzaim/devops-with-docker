FROM ubuntu:22.04

WORKDIR /usr/src/app

COPY script.sh .

# Install curl
RUN apt-get update && apt-get install -y curl

# CMD ./script.sh
ENTRYPOINT [ "./script.sh" ]