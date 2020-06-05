FROM ubuntu:latest

RUN apt-get update && apt-get install -y firefox x11vnc xvfb

CMD xvfb-run -f /.xauth_vnc -s ':99 -screen 0 1024x768x24' firefox & sleep 2 && x11vnc -auth /.xauth_vnc -display :99 -forever -passwd password
