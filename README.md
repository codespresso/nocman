# Nocman - Digital Signage for the Raspberry Pi

The best way for installing Nocman on [Raspbian](https://www.raspberrypi.org/downloads/raspbian/) Jessie is:

```
$ bash <(curl -sL https://raw.githubusercontent.com/codespresso/nocman/production/bin/install.sh)
```

(The installation will take 15-20 minutes or so depending on your connectivity and the speed of your SD card.)

Screenly OSE works on all Raspberry Pi versions, including Raspberry Pi Zero and Raspberry Pi 3 Model B.

## Dockerized Development Environment

To simplify development of the server module of Screenly OSE, we've created a Docker container. This is intended to run on your local machine with the Screenly OSE repository mounted as a volume.

Assuming you're in the source code repository, simply run:

```
$ docker run --rm -ti \
  -p 8080:8080 \
  -v $(pwd):/home/pi/screenly \
  wireload/screenly-ose-server
```

## Running the Unit Tests

    nosetests --with-doctest

## Credits
Nocman is a fork of [Screenly OSE](https://www.screenly.io/ose/).