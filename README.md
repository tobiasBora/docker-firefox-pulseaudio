# Dockerized Firefox

Run Firefox inside an isolated [Docker](http://www.docker.io) container. This is achieved by sharing a socket for X11 and PulseAudio. This code is based on the terlar code for spotify [docker-spotify-pulseaudio](https://github.com/terlar/docker-spotify-pulseaudio). This version does not get/save the configuration of firefox in the user home, everything stay inside the docker container.


## Instructions

1. Clone this repository and change to the directory:

  ```sh
	  git clone https://github.com/tobiasBora/docker-firefox-pulseaudio.git && cd docker-firefox-pulseaudio
  ```

2. Build the container:

  ```sh
  sudo docker build -t firefox .
  ```

3. Run the provided spotify script:

  ```sh
  ./scripts/firefox
  ```

4. Use Firefox, and enjoy the sound.

If you get an error about impossible display, and if you run Fedora or any other distribution using SELinux, you may want to try to temporary disable SELinux by using:

   ```sh
   sudo setenforce 0
   ```
