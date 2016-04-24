# Run qtCreator in a docker container

* Change the user and group id in the Dockerfile

* Build the image with
```
docker build -t qtcreator .
```

* Run on the current display with
```
docker run -it --rm -e DISPLAY=$DISPLAY -v /tmp/.X11-unix:/tmp/.X11-unix qtcreator
```

### Credits

Inspired by http://fabiorehm.com/blog/2014/09/11/running-gui-apps-with-docker/
